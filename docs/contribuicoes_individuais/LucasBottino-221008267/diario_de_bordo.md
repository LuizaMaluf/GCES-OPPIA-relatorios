# Diário de Bordo – \[Lucas Gama De Araujo Bottino]

**Disciplina:** \[Gestão da Configuração e Evolução de Software]
**Equipe:** \[Oppia]
**Comunidade/Projeto de Software Livre:** \[Oppia]

---

## Sprint 0 – \[25/08 – 10/09]

### Resumo da Sprint

A equipe na Sprint 0 focou em organizar os integrantes em subgrupos, criar o fork do projeto e o repositorio de docuimentação, além de estudar as políticas de contribuição e práticas de gestão e configuração de software da comunidade mantenedora do Oppia. A configuração do ambiente local foi o principal tópico, documentando todos os problemas e aprendizados encontrados.

### Atividades Realizadas

| Data  | Atividade                                         | Tipo (Código/Doc/Discussão/Outro) | Link/Referência                                                                      | Status    |
| ----- | ------------------------------------------------- | --------------------------------- | ------------------------------------------------------------------------------------ | --------- |
| 25/08 | Criar fork do projeto                             | Código                            | [Link](https://github.com/bottinolucas/oppia)                                        | Concluído |
| 25/08 | Leitura e estudo da documentação do projeto       | Estudo                            | [Link](https://github.com/oppia/oppia/wiki/Overview-of-the-Oppia-codebase)           | Concluído |
| 25/08 | Mapeamento das políticas de contribuição do Oppia | Estudo                            | [Link](https://github.com/oppia/oppia/wiki)                                          | Concluído |
| 25/08 | Configurar ambiente de desenvolvimento no Linux   | Código                            | [Link](https://github.com/oppia/oppia/wiki/Installing-Oppia-%28Linux%3B-Python-3%29) | Concluído |
| 25/08 | Definir linhas de trabalho                        | Discussão                         | [Link](https://github.com/oppia/oppia/wiki)                                          | Concluído |
| 09/09 | Preenchimento do formulário de contribuição       | Formulário                        | [Link]()                                                                             | Concluído |
| 10/09 | Contribuição no repositório de documentação       | Discussão                         | [Link](https://github.com/oppia/oppia/wiki)                                          | Concluído |

### Maiores Avanços

- Preenchi o formulário requerido pelo projeto com as regras para contribuição.
- Consegui rodar o projeto Oppia localmente no ambiente linux após a configuração
- Compreendi as políticas de contribuição, qualidade e comunicação da comunidade mantenedora do Oppia

### Maiores Dificuldades

- Utilizando o WSL no Windows, dependências do front-end travam a instalação, então tornou-se necessário retirar a pasta node_modules (gerada pelo build) e refazer o build.
- O tempo de build inicial tanto para a instalação local, como para a instalação via Docker é extremamente longo, com difícil conhecimento sobre possíveis erros e demora para validação.
- O Dockerfile.frontend apontou para fonte inexistente no build. Dessa forma, tornou-se necessário intervenção no arquivo para que as dependências fossem instaladas
- Ao auxiliar o integrante João Paulo na instalação das dependências e configuração do projeto no MacOS X, encontramos problemas de configuração com a dependência typed-ast, o qual não conseguimos resolver.

### Aprendizados

- Entendi que nem sempre todos os ambientes de configuração são exatamente iguais para todos os usuários.
- Aprendi a lidar com complicações que apareciam durante o processo de configuração de software.
- Diferentes sistemas operacionais geram diferentes resultados. Nesse caso, torna-se extremamente importante conhecer ao menos o básico de cada S.O.

### Plano Pessoal para a Próxima Sprint

- [ ] Buscar issues relacionadas a CI e erros na parte de DevOps do Oppia.
- [ ] Trabalhar em conjunto com Luiza Maluf para resolver problemas identificados.
- [ ] Consolidar aprendizados sobre pipelines e integração contínua.
- [ ] Conseguir fazer a instalação correta no ambiente MacOS X.
---

## Sprint 1 – \[10/09 – 24/09]

### Resumo da Sprint

Essa sprint foi dedicada à contribuição efetiva no código da comunidade Oppia. Em conjunto com minha colega Luiza Maluf, trabalhamos na issue [#22915](https://github.com/oppia/oppia/issues/22915), que consistia em adicionar um link para a página de Contributors no menu suspenso About da barra de navegação superior.

O trabalho envolveu identificar os arquivos responsáveis pelo componente de navegação, realizar as alterações necessárias, validar a solução localmente e preparar a submissão do PR.

### Atividades Realizadas

| Data          | Atividade                                              | Tipo (Código/Doc/Discussão/Outro) | Link/Referência                                                        | Status       |
| ------------- | ------------------------------------------------------ | --------------------------------- | ---------------------------------------------------------------------- | ------------ |
| 15/09         | Estudo da issue e histórico de PRs relacionados        | Estudo                            | [Issue #22915](https://github.com/oppia/oppia/issues/22915)            | Concluído    |
| 23/09         | Identificação dos arquivos relevantes para a alteração | Código                            | `top-navigation-bar.component.html`, `top-navigation-bar.component.ts` | Concluído    |
| 23/09         | Implementação da adição do link no menu                | Código                            | -                                                                      | Concluído    |
| 23/09         | Inclusão de suporte a i18n e constantes                | Código                            | `en.json`, `app.constants.ts`                                          | Concluído    |
| 04/10         | Testes locais da navegação                             | Código                            | -                                                                      | Incompleto   |
| 23/10 - 24/10 | Discussão e interação com o maintainer @mon4our        | Discussão                         | [Issue #22915](https://github.com/oppia/oppia/issues/22915)            | Em andamento |
| 24/10         | Assigne da issue para subir o PR                       | Outro                             | Aguardando maintainer                                                  | Pendente     |

### Maiores Avanços

- Conseguimos implementar a feature de forma limpa e alinhada com a issue.
- Identificamos rapidamente os arquivos certos a modificar graças ao estudo do PR anterior (#22560).
- Trabalhamos em colaboração para dividir tarefas e revisar mutuamente o código.

![#22915](./assets/issue_22915.png)

### Maiores Dificuldades

- Foi necessário entender o fluxo de internacionalização (i18n) do Oppia para inserir a nova chave.
- A navegação exigiu atualização também no **tracking de GA**, o que não estava descrito na issue.
- Dependência da validação dos maintainers para confirmar se a solução segue o padrão esperado.

### Aprendizados

- Ganhamos experiência em **trabalhar com componentes Angular** dentro de um projeto grande como o Oppia.
- Entendemos melhor o processo de contribuição e interação com maintainers (apresentar mudanças, aguardar validação e fornecer evidências).
- Aprendi a importância de manter a consistência entre o **footer** e o **top navigation bar** em termos de UX.

### Plano Pessoal para a Próxima Sprint

- [ ] Finalizar a submissão do PR com o vídeo de demonstração solicitado.
- [ ] Explorar novas issues relacionadas à **CI/CD** e **testes automatizados** no Oppia.

## Sprint 2 – [25/09 – 08/10]

### Resumo da Sprint

Nesta sprint, o foco foi eu e a [Luiza Maluf](https://github.com/luizamaluf) trabalharmos na issue relacionada à **remoção do parâmetro `SERVER_CAN_SEND_EMAILS`**, garantindo que a funcionalidade de envio de emails permanecesse operacional sem depender de uma plataforma condicional. A atividade envolveu identificar todos os trechos do código que utilizavam o parâmetro, modificar os arquivos necessários e atualizar ou remover os testes que dependiam dele.

### Atividades Realizadas

| Data           | Atividade                                                   | Tipo (Código/Doc/Discussão/Outro) | Link/Referência | Status        |
| -------------- | ----------------------------------------------------------- | --------------------------------- | --------------- | ------------- |
| 25/09          | Estudo da issue e análise do uso de `SERVER_CAN_SEND_EMAILS` | Estudo | [Issue link](https://github.com/oppia/oppia/issues/22727) | Concluído     |
| 26/09          | Identificação dos arquivos a serem modificados             | Código | `admin.py`, `cron.py`, `topic_viewer.py`, `topic_editor.py`, `email_manager.py`, entre outros | Concluído     |
| 27/09 – 30/09  | Remoção do parâmetro e ajustes no código                   | Código | - | Concluído     |
| 01/10 – 03/10  | Atualização de testes relacionados a envio de email        | Código | `email_manager_test.py` | Concluído     |
| 04/10 – 06/10  | Testes locais do backend e validação do envio de emails    | Código | - | Concluído     |
| 07/10 – 08/10  | Discussão com maintainers e ajustes finais                 | Discussão | [Issue link](https://github.com/oppia/oppia/issues/22727) | Em andamento  |

### Maiores Avanços

* Remoção completa do parâmetro `SERVER_CAN_SEND_EMAILS` e ajustes correspondentes no código.  
* Atualização dos testes de email para refletir o comportamento sem condicional.  
* Garantia de que a funcionalidade de envio de email continua funcionando corretamente em todas as partes do sistema.  

### Maiores Dificuldades

* Identificação de todos os pontos do código que dependiam do parâmetro antigo.  
* Ajuste dos testes para não quebrar com a remoção do parâmetro.  
* Necessidade de validar com maintainers antes de submeter o PR.  

### Aprendizados

* Experiência prática em **remover parâmetros de plataforma e refatorar código dependente**.  
* Entendimento da importância de testes para manter estabilidade do backend durante alterações globais.  
* Aprendizado sobre **comunicação com maintainers** e documentação de mudanças em PRs complexos.  

### Plano Pessoal para a Próxima Sprint

* [ ] Submeter o PR com todas as alterações e evidências de testes passando.  
* [ ] Monitorar feedback dos maintainers e aplicar ajustes finais se necessário.  
* [ ] Explorar novas issues de backend que envolvam **remoção de parâmetros ou simplificação de lógica**.


---

## Sprint 3 – [09/10 – 21/10]

### Resumo da Sprint

Nesta sprint, o foco foi eu e a [Luiza Maluf](https://github.com/luizamaluf) tentarmos submeter o PR referente à issue #22727 – remoção do parâmetro SERVER_CAN_SEND_EMAILS. Durante o processo, enfrentamos problemas técnicos que impediram o push direto, incluindo erros de backend, falhas de pre-push, problemas de permissões no WSL e conflitos de versões no Docker.

### Atividades Realizadas

| Data           | Atividade                                                   | Tipo (Código/Doc/Discussão/Outro) | Link/Referência | Status        |
| -------------- | ----------------------------------------------------------- | --------------------------------- | --------------- | ------------- |
| 09/10 – 21/10  | Investigação e tentativa de pre-push após alterações no backend` | Código | [Issue link](https://github.com/oppia/oppia/issues/22727) | Concluído    |
| 20/10         | Registro das dificuldades no Discussions do Oppia            | Discurssão | [#23646](https://github.com/oppia/oppia/discussions/23646), [#23633](https://github.com/oppia/oppia/discussions/23633), [#23631](https://github.com/oppia/oppia/discussions/23631) | Aguardando resposta     |
| 21/09  | Documentação do fluxo de problemas e próximos passos                 | Doc | Diário de Bordo | Concluído     |


### Maiores Avanços

- Remoção do parâmetro SERVER_CAN_SEND_EMAILS implementada no código e nos testes locais.

- Identificação dos principais erros bloqueando o pre-push e possíveis causas:

    -   Backend: testes falhando (ImportError, too many positional arguments, unused variables).

    -   WSL: problemas de permissão no node_modules.

    -   Docker: build quebrando devido ao Debian Buster descontinuado.

- Discussões abertas no repositório oficial para suporte e orientação dos maintainers.

### Maiores Dificuldades

- Falhas no pre-push que impediram a submissão do PR.

- Dependência dos maintainers para definir como corrigir erros de backend e CI/CD.

- Problemas de ambiente (WSL e Docker) que atrasaram o fluxo de contribuição.  

### Aprendizados

- Compreensão mais profunda do pipeline de testes, linting e CI/CD do Oppia.

- Experiência em documentar e comunicar problemas técnicos complexos à comunidade.

- Aprendizado prático em lidar com erros de integração em ambientes variados.

- Encontramos muitos erros fazendo testes manuais da plataforma, que estão sendo anotados para relatar para os mantenedores do Oppia

### Plano Pessoal para a Próxima Sprint

* [ ] Acompanhar a resposta dos maintainers sobre os bloqueios no pre-push. 
* [ ] Corrigir erros de linting e testes backend conforme orientação.
* [ ] Submeter finalmente o PR da issue #22727.