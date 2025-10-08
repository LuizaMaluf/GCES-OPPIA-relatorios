# Diário de Bordo – Gabriel Moura dos Santos

**Disciplina:** Gestão da Configuração e Evolução de Software
**Equipe:** Oppia
**Comunidade/Projeto de Software Livre:** Oppia

---

## Sprint 2 – [25/09 – 08/10]

### Resumo da Sprint

Nesta sprint, foquei no estudo da issue #16640, um E2E flake relacionado à visibilidade do campo de entrada de nome de usuário que vem ocorrendo desde novembro de 2022. O problema envolve um erro "Username input is not visible" em testes de wipeout (exclusão de conta). Infelizmente, enfrentei sérias dificuldades técnicas com meu ambiente de desenvolvimento após atualizar pacotes do Ubuntu, o que quebrou completamente minha configuração local. Tentativas de usar Windows e WSL também falharam, limitando minha capacidade de implementar soluções práticas.

### Atividades Realizadas

| Data | Atividade | Tipo (Código/Doc/Discussão/Outro) | Link/Referência | Status |
| :--- | :--- | :--- | :--- | :--- |
| 26/09 | Análise detalhada da issue #16640 e histórico de ocorrências | Estudo | [Issue #16640](https://github.com/oppia/oppia/issues/16640) | Concluído |
| 28/09 | Estudo do código de wipeout.js e workflow de testes | Código | `/core/tests/webdriverio_desktop/wipeout.js` | Concluído |
| 30/09 | Investigação da função _addExplorationRole no workflow.js | Código | `/core/tests/webdriverio_utils/workflow.js:272` | Concluído |
| 02/10 | Tentativa de reconfiguração do ambiente após atualização do Ubuntu | Código | - | Falhou |
| 04/10 | Tentativas de configuração no Windows | Código | - | Falhou |
| 06/10 | Tentativas de configuração via WSL | Código | - | Falhou |

### Maiores Avanços

* Compreensão do problema de visibilidade em elementos de interface em testes E2E.
* Estudo detalhado do fluxo de wipeout (exclusão de contas) e seus testes associados.
* Análise do histórico de ocorrências do flake desde 2022, identificando padrões de falha.
* Entendimento de como elementos dinâmicos podem causar flakes em testes automatizados.

### Maiores Dificuldades

* Quebra completa do ambiente de desenvolvimento após atualização de pacotes do Ubuntu.
* Impossibilidade de testar soluções localmente devido aos problemas de configuração.
* Falhas nas tentativas de reconfiguração em diferentes plataformas (Windows, WSL).
* Limitação para contribuições práticas devido aos problemas técnicos de ambiente.

### Aprendizados

* A importância de manter backups ou snapshots do ambiente de desenvolvimento.
* Como atualizações de sistema podem quebrar configurações complexas de desenvolvimento.
* A necessidade de ambientes containerizados para projetos com muitas dependências.
* Como analisar flakes relacionados à visibilidade de elementos em testes E2E.
* A importância de ter múltiplas opções de ambiente de desenvolvimento.

### Plano Pessoal para a Próxima Sprint

* Priorizar a resolução dos problemas de ambiente de desenvolvimento.
* Considerar uso de containers Docker para isolar o ambiente do Oppia.
* Buscar issues que possam ser trabalhadas sem necessidade de execução local.
* Documentar problemas de configuração para ajudar outros desenvolvedores.
* Explorar contribuições em documentação enquanto resolvo questões técnicas.
