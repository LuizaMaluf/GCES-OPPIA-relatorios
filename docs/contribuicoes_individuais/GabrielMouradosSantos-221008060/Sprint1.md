# Diário de Bordo – Gabriel Moura dos Santos

**Disciplina:** Gestão da Configuração e Evolução de Software
**Equipe:** Oppia
**Comunidade/Projeto de Software Livre:** Oppia

---

## Sprint 1 – [11/09 – 24/09]

### Resumo da Sprint

Nesta sprint, foquei em trabalhar com uma issue real do projeto Oppia, especificamente a issue #16097, que se trata de um CI flake que vem ocorrendo desde setembro de 2022. O problema envolve um teste end-to-end que falha intermitentemente, onde o texto esperado "You must be feeling great?" não é encontrado, retornando uma string vazia. Dediquei tempo significativo estudando o código de testes, tentando reproduzir o problema localmente e investigando possíveis soluções, mas não consegui identificar a causa raiz do flake.

### Atividades Realizadas

| Data | Atividade | Tipo (Código/Doc/Discussão/Outro) | Link/Referência | Status |
| :--- | :--- | :--- | :--- | :--- |
| 12/09 | Análise detalhada da issue #16097 e histórico de falhas | Estudo | [Issue #16097](https://github.com/oppia/oppia/issues/16097) | Concluído |
| 14/09 | Estudo do código de testes webdriverio e estrutura E2E | Código | `/core/tests/webdriverio_desktop/additionalEditorFeaturesModals.js` | Concluído |
| 16/09 | Tentativa de reprodução local do teste que falha | Código | - | Parcial |
| 18/09 | Investigação do código de forms.js e função readPlainText | Código | `/core/tests/webdriverio_utils/forms.js:571` | Concluído |
| 20/09 | Análise de logs do GitHub Actions para identificar padrões | Estudo | [GitHub Actions logs](https://github.com/oppia/oppia/actions/runs/8408651198/job/23025372490) | Concluído |
| 22/09 | Tentativas de implementação de delays e guards adicionais | Código | - | Em progresso |

### Maiores Avanços

* Compreensão profunda da estrutura de testes E2E do Oppia usando WebDriverIO.
* Identificação de que o problema está relacionado a timing issues no carregamento de elementos da interface.
* Familiarização com o fluxo de CI/CD do projeto e como analisar falhas em GitHub Actions.
* Entendimento de como flakes podem impactar a produtividade de uma equipe de desenvolvimento.

### Maiores Dificuldades

* A natureza intermitente do bug torna muito difícil reproduzi-lo localmente de forma consistente.
* O código de testes é complexo e envolve múltiplas camadas de abstração (WebDriverIO, Jasmine, etc.).
* Mesmo com várias tentativas de implementar delays e verificações adicionais, não consegui identificar a causa raiz.
* A issue é antiga (setembro 2022) e já teve várias tentativas de correção, sugerindo alta complexidade.

### Aprendizados

* Como funciona a estrutura de testes end-to-end em projetos de grande escala.
* A importância de testes estáveis para manter a produtividade da equipe de desenvolvimento.
* Técnicas de debugging em ambientes de CI/CD e análise de logs de falhas.
* A complexidade de resolver flakes em testes automatizados, especialmente quando envolvem timing.
* Como analisar histórico de issues e entender o contexto de problemas recorrentes.

### Plano Pessoal para a Próxima Sprint

* Buscar outras issues mais adequadas ao meu nível de experiência atual no projeto.
* Focar em contribuições que envolvam código mais direto, evitando inicialmente problemas de flakes complexos.
* Continuar estudando a arquitetura do projeto para futuras contribuições mais efetivas.
* Documentar os aprendizados sobre debugging de testes para ajudar outros contributors.
