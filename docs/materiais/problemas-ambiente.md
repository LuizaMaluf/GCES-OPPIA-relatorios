# Problema: `make run-devserver` do Oppia Trava no Windows (WSL)

Este documento descreve um problema comum ao tentar rodar o `make run-devserver` do Oppia no Windows com WSL 2, e como resolvê-lo manualmente, incluindo correções para problemas de `pre-commit`.

## Descrição

Ao executar o `make run-devserver`, o processo parece travar indefinidamente após a instalação do `yarn`, na etapa `docker cp`:

```bash
make run-devserver
docker compose up angular-build -d
[...]
success Already up-to-date.
Done in 2.13s.
make[1]: Leaving directory '...'
docker cp oppia-angular-build:/app/oppia/node_modules .
```
O terminal fica parado nesse ponto por muitos minutos (ou horas) e não continua a execução, impedindo que o servidor web (oppia-dev-server) seja iniciado.

## Causa Raiz
O Makefile do Oppia é dividido em 7 etapas principais para o run-devserver.

```bash
docker compose up angular-build -d #Liga o contêiner de build

make update.package #Roda yarn install dentro dele

docker cp oppia-angular-build:/app/oppia/node_modules . #copia a pasta node_modules 

docker compose stop angular-build #Desliga o contêiner de build

docker compose up dev-server -d #Liga o servidor web

make update.requirements #Roda pip install no servidor web

make start-devserver #Espera o servidor ficar online
```

O comando docker cp é o causador do erro. Ele tenta copiar a pasta node_modules (que contém dezenas de milhares de arquivos pequenos) de dentro do contêiner (Linux) para a sua pasta de projeto no Windows (/mnt/c/...).

A "ponte" de sistema de arquivos entre o WSL 2 e o Windows (NTFS) é extremamente lenta para esse tipo de operação, o que faz com que o comando docker cp trave ou demore um tempo inaceitável.

## Solução

Cancele o script travado e execute os passos restantes manualmente

No seu terminal (na pasta do projeto), execute os comandos a seguir, um de cada vez.

```bash
# Garante que o contêiner de build pare
docker compose stop angular-build

# Inicia o servidor web (o que faltava!)
docker compose up dev-server -d --no-deps

# Instala as dependências Python no servidor
make update.requirements

# Monitora o servidor até ele ficar online
make start-devserver
```

O último comando (make start-devserver) deve mostrar uma barra de progresso e, em seguida, a mensagem de sucesso:

```bash
Please wait while the development server starts...

Please visit http://localhost:8181 to access the development server.
Check dev-server logs using "make logs.dev-server"
Stop the development server using "make stop"
Agora você pode acessar http://localhost:8181 no seu navegador.
```

## Execuções posteriores
Essa lentidão toda é apenas da primeira configuração. No entanto, a solução manual acima cria dois novos problemas.

Problema A: Ligar e Desligar o Servidor
Para DESLIGAR o servidor:

```bash
make stop
```

Para LIGAR o servidor (apenas o backend), use:

```bash
make start-devserver
```

Problema B: Frontend (Hot-Reload) Não Atualiza

 O comando make start-devserver (da solução acima) liga apenas o backend (dev-server). Ele não liga o contêiner angular-build, que é responsável por "assistir" (watch) seus arquivos de frontend e recompilá-los.

É preciso ligar os dois contêineres (dev-server e angular-build) e forçar o Angular a usar "polling" para detectar mudanças no WSL.

Pare tudo:

```bash
make stop
```
Edite o docker-compose.yml: Abra o docker-compose.yml na raiz do projeto. Encontre o serviço angular-build e adicione a flag --poll=1000 ao command.

Procure por:

```bash
command: ["yarn", "start"]
```
Mude para:

```bash
command: ["yarn", "start", "--", "--poll=1000"]
```

Use este novo comando para LIGAR o servidor (Frontend + Backend):

```bash
docker compose up -d dev-server angular-build
```
---

# Problema: Erro de pre-commit ao tentar commitar

## Descrição
Ao tentar fazer um commit (especialmente pela interface gráfica do VS Code), você recebe o erro: ```cannot spawn .git/hooks/pre-commit: No such file or directory```

Isso ocorre por dois motivos:

- Os "hooks" do Git, que rodam os testes, não foram instalados localmente.

- Está tentando commitar pela GUI do VS Code. A GUI usa o Git do Windows, mas seus hooks estão (ou deveriam estar) instalados no Git do Linux (WSL). O Git do Windows não consegue achar os scripts do WSL.

## Solução:

Instale os Hooks: No seu terminal WSL, na pasta do projeto, rode:

```bash
pre-commit install
```

Usar o terminal garante que você está usando o Git do Linux, que sabe onde os hooks estão.

```bash
git add .

git commit -m "fix(scope): my awesome change"
```

Ao fazer isso, os testes do pre-commit (lint, mypy, etc.) serão executados. Se eles passarem, seu commit será concluído. Se falharem, corrija os erros que o terminal apontar e tente o commit novamente.