# Sprint 1 - Carla Clementino

## Configuração do Ambiente de Desenvolvimento - Oppia

Durante esta sprint, enfrentei alguns desafios na configuração inicial do projeto Oppia, seguindo a [documentação oficial de instalação para Linux com Python 3](https://github.com/oppia/oppia/wiki/Installing-Oppia-%28Linux%3B-Python-3%29). Apesar dos problemas, consegui rodar o projeto localmente no Pop!OS.

### Problemas Encontrados

- **Versão específica do Python**: O Oppia requer Python 3.10.16 especificamente. Tive que instalar o `pyenv` para gerenciar essa versão, pois o Pop!OS vem com Python 3.11 por padrão.

- **Configuração do pyenv e direnv**: A configuração inicial do `pyenv` e `direnv` foi um pouco confusa, especialmente na criação dos arquivos `.direnvrc` e `.envrc`. Precisei consultar a documentação algumas vezes para entender o funcionamento correto.

- **Dependências do sistema**: Faltavam alguns pacotes essenciais como `openjdk-11-jre` e `unzip` que precisaram ser instalados manualmente via `apt`.

- **Primeira execução lenta**: O primeiro `python -m scripts.start` demorou cerca de 8-10 minutos para completar, pois baixa e configura todas as dependências do projeto (Node.js, pacotes npm, bibliotecas Python, etc.).

### Soluções Aplicadas

1. **Instalação de dependências do sistema**:
   ```bash
   sudo apt-get update
   sudo apt-get install curl git unzip openjdk-11-jre
   ```

2. **Configuração do pyenv**:
   - Instalei o pyenv seguindo a documentação
   - Instalei Python 3.10.16: `pyenv install 3.10.16`
   - Configurei o pyenv global

3. **Configuração do direnv**:
   - Instalei o direnv: `sudo apt install direnv`
   - Criei os arquivos `.direnvrc` e `.envrc` conforme a documentação
   - Configurei o hook no shell

4. **Clone e setup do repositório**:
   - Fiz fork do repositório no GitHub
   - Clonei localmente: `git clone https://github.com/[meu-usuario]/oppia.git`
   - Instalei dependências Python: `pip install pyyaml setuptools coverage configparser`

5. **Primeira execução**:
   - Executei `python -m scripts.start`
   - Aguardei o download e configuração de todas as dependências
   - Servidor iniciou com sucesso em `http://localhost:8181`

### Resultado

Após resolver os problemas de configuração, consegui rodar o projeto Oppia localmente no Pop!OS com sucesso. O ambiente de desenvolvimento está funcional e o servidor local responde corretamente.

### Aprendizados

- A importância de seguir exatamente as versões especificadas na documentação
- Como usar `pyenv` e `direnv` para gerenciamento de ambientes Python
- O processo de build inicial do Oppia é demorado, mas isso é esperado
- O Pop!OS funcionou bem para desenvolvimento, sendo compatível com as instruções para Ubuntu/Debian

## Próximos Passos
 
- Explorar a interface do Oppia localmente
- Carregar explorações demo via página de admin
- Estudar a arquitetura do projeto
- Familiarizar-me com o fluxo de contribuição e boas práticas do projeto
