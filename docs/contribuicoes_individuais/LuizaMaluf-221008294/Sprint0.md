# Diário de Bordo – \[Luiza Maluf Amorim]

**Disciplina:** \[Gestão da Configuração e Evolução de Software]
**Equipe:** \[Oppia]
**Comunidade/Projeto de Software Livre:** \[Oppia]

---

## Sprint 0 – \[25/08 – 10/09]

### Resumo da Sprint

Essa sprint foi focada em organizar a equipe, criar o fork e o repositório de documentação, além de estudar as políticas de contribuição e práticas de GCES do Oppia. Também realizamos a configuração do ambiente local, documentando os problemas e aprendizados.

### Atividades Realizadas

| Data  | Atividade | Tipo (Código/Doc/Discussão/Outro) | Link/Referência | Status |
| ----- | --------- | --------------------------------- | --------------- | ------ |
| 25/08 | Criação do fork | Código | [Link](https://github.com/LuizaMaluf/oppia) | Concluído |
| 25/08 | Leitura e estudo da documentação do projeto | Estudo                            | [Link](https://github.com/oppia/oppia/wiki/Overview-of-the-Oppia-codebase) | Concluído |
| 01/09 | Mapeamento das políticas de contribuição do Oppia | Estudo | [Link](https://github.com/oppia/oppia/wiki) | Concluído |
| 08/09 | Configuração do ambiente linux | Código | [Link](https://github.com/oppia/oppia/wiki/Installing-Oppia-%28Linux%3B-Python-3%29)   | Concluído |
| 08/09 | Definição de linha de trabalaho | Discussção | - | Concluido | 
| 09/09 | Criação do repositório de documentação dos relatórios | Doc |  [Link](https://github.com/LuizaMaluf/GCES-OPPIA-relatorios) | Concluído |
| 09/09 | Preenchimento do formulário de contribuição | Formulário |  [Link]([https://github.com/LuizaMaluf/GCES-OPPIA-relatorios](https://docs.google.com/forms/d/e/1FAIpQLSfoFLKT4BlNH2937mSMJATVaWq-yBSrq8p3jjrPwcMw3gaGcg/viewform?c=0&w=1)) | Concluído |

### Maiores Avanços

* Preenchi o formulário requerido concordando com as regras de contribuição para o projeto.

* Consegui rodar o projeto Oppia localmente após configuração.

* Compreensão das políticas de contribuição, qualidade e comunicação da comunidade Oppia.

* Organização inicial da equipe e do repositório acadêmico.

### Maiores Dificuldades

* Foi minha primeira vez usando WSL e configurei de forma incorreta.

* Precisei reinstalar o WSL para prosseguir com a configuração do ambiente.

* O tempo de build inicial também foi longo, o que atrasou a validação do setup.


### Aprendizados

* Ganhei experiência na instalação e uso do WSL para desenvolvimento.

* Entendi melhor a importância de seguir passo a passo a documentação oficial para evitar erros de configuração.

* Aprendi a lidar com reinstalação e reconfiguração do ambiente como parte do processo de GCES.

### Plano Pessoal para a Próxima Sprint

* [ ] Buscar issues relacionadas a CI e erros na parte de DevOps do Oppia.
* [ ] Trabalhar em conjunto com Lucas Bottino para resolver problemas identificados.
* [ ] Consolidar aprendizados sobre pipelines e integração contínua.

---

## Sprint 1 – \[10/09 – 24/09]

### Resumo da Sprint

Essa sprint foi dedicada à contribuição efetiva no código da comunidade Oppia. Em conjunto com meu colega Lucas Bottino, trabalhamos na issue [#22915](https://github.com/oppia/oppia/issues/22915), que consistia em adicionar um link para a página de Contributors no menu suspenso About da barra de navegação superior.

O trabalho envolveu identificar os arquivos responsáveis pelo componente de navegação, realizar as alterações necessárias, validar a solução localmente e preparar a submissão do PR.

### Atividades Realizadas

| Data           | Atividade                                  | Tipo (Código/Doc/Discussão/Outro) | Link/Referência | Status        |
| -------------- | ------------------------------------------ | --------------------------------- | --------------- | ------------- |
| 15/09          | Estudo da issue e histórico de PRs relacionados | Estudo | [Issue #22915](https://github.com/oppia/oppia/issues/22915) | Concluído     |
| 23/09          | Identificação dos arquivos relevantes para a alteração | Código | `top-navigation-bar.component.html`, `top-navigation-bar.component.ts` | Concluído     |
| 23/09          | Implementação da adição do link no menu    | Código | - | Concluído     |
| 23/09          | Inclusão de suporte a i18n e constantes    | Código | `en.json`, `app.constants.ts` | Concluído     |
| 04/10          | Testes locais da navegação                 | Código | - | Incompleto    |
| 23/10 - 24/10  | Discussão e interação com o maintainer @mon4our | Discussão | [Issue #22915](https://github.com/oppia/oppia/issues/22915) | Em andamento  |
| 24/10          | Assigne da issue para subir o PR           | Outro | Aguardando maintainer | Pendente      |


### Maiores Avanços


* Conseguimos implementar a feature de forma limpa e alinhada com a issue.  
* Identificamos rapidamente os arquivos certos a modificar graças ao estudo do PR anterior (#22560).  
* Trabalhamos em colaboração para dividir tarefas e revisar mutuamente o código.  

![#22915](./assets/issue_22915.png)


### Maiores Dificuldades

* Foi necessário entender o fluxo de internacionalização (i18n) do Oppia para inserir a nova chave.  
* A navegação exigiu atualização também no **tracking de GA**, o que não estava descrito na issue.  
* Dependência da validação dos maintainers para confirmar se a solução segue o padrão esperado.  



### Aprendizados

* Ganhamos experiência em **trabalhar com componentes Angular** dentro de um projeto grande como o Oppia.  
* Entendemos melhor o processo de contribuição e interação com maintainers (apresentar mudanças, aguardar validação e fornecer evidências).  
* Aprendi a importância de manter a consistência entre o **footer** e o **top navigation bar** em termos de UX.  


### Plano Pessoal para a Próxima Sprint


* [ ] Finalizar a submissão do PR com o vídeo de demonstração solicitado.  
* [ ] Explorar novas issues relacionadas à **CI/CD** e **testes automatizados** no Oppia.   

---

## Sprint 2 – [25/09 – 08/10]

### Resumo da Sprint

Nesta sprint, o foco foi eu e o [Lucas Bottino](https://github.com/bottinolucas) trabalharmos na issue relacionada à **remoção do parâmetro `SERVER_CAN_SEND_EMAILS`**, garantindo que a funcionalidade de envio de emails permanecesse operacional sem depender de uma plataforma condicional. A atividade envolveu identificar todos os trechos do código que utilizavam o parâmetro, modificar os arquivos necessários e atualizar ou remover os testes que dependiam dele.

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
* [ ] Explorar novas issues de backend que envolvam **remoção de parâmetros ou simplificação de lógica**.]


---

## Sprint 3 – [09/10 – 21/10]

### Resumo da Sprint

Nesta sprint, o foco foi eu e o [Lucas Bottino](https://github.com/bottinolucas) tentarmos submeter o PR referente à issue #22727 – remoção do parâmetro SERVER_CAN_SEND_EMAILS. Durante o processo, enfrentamos problemas técnicos que impediram o push direto, incluindo erros de backend, falhas de pre-push, problemas de permissões no WSL e conflitos de versões no Docker.

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

### Plano Pessoal para a Próxima Sprint

* [ ] Acompanhar a resposta dos maintainers sobre os bloqueios no pre-push. 
* [ ] Corrigir erros de linting e testes backend conforme orientação.
* [ ] Submeter finalmente o PR da issue #22727.