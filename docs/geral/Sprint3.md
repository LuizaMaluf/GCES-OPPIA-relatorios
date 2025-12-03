# 📝 Relatório de Contribuição – Sprint 3

**Disciplina:** Gestão de Configuração e Evolução de Software

**Equipe:** \[Oppia]

**Comunidade/Projeto de Software Livre:** \[Oppia]

**Período da Sprint:** \[09/10 – 21/10]

---

## 1. Objetivos da Sprint


- Submeter o PR da issue #22727 – remoção do parâmetro SERVER_CAN_SEND_EMAILS.
- Resolver bloqueios de backend, linting e testes que impedem o pre-push.
- Documentar problemas enfrentados e buscar suporte junto à comunidade e maintainers.
- Garantir a estabilidade do backend durante alterações globais.
- Identificar e corrigir bugs de responsividade na interface do editor de questões.
- Documentar problemas enfrentados na configuração de ambiente de desenvolvimento (Docker/WSL) para permitir contribuições.


---

## 2. Entregas Coletivas

| Entrega                     | Status (Concluído/Parcial/Pendente) | Link/Referência                                             | Observações           |
| --------------------------- | ----------------------------------- | ----------------------------------------------------------- | --------------------- |
| Tentativa de submissão do PR #22727 | Parcial | [Issue #22727](https://github.com/oppia/oppia/issues/22727) | Push abortado devido a falhas de backend e lint |
| Registro de problemas no Discussions | Concluído |  [#23646](https://github.com/oppia/oppia/discussions/23646), [#23633](https://github.com/oppia/oppia/discussions/23633), [#23631](https://github.com/oppia/oppia/discussions/23631) | Discussão sobre pre-push, WSL e Docker |
| Revisão de código e testes finais | Concluído | [Issue #22727](https://github.com/oppia/oppia/issues/22727)| Testes manuais e unitários OK |
| Correção de bug de responsividade | Concluído | [Issue #23439](https://github.com/oppia/oppia/issues/23439), [PR #23648](https://github.com/oppia/oppia/pull/23648) | PR submetido após correção de ambiente |
| Documentação de problemas de ambiente | Concluído | [Link](https://github.com/LuizaMaluf/GCES-OPPIA-relatorios/blob/main/docs/materiais/problemas-ambiente.md) | Guia para resolver travamentos de docker cp e pre-commit no WSL |
| Análise e discussão de Issues | Concluído | [Issue #23577](https://github.com/oppia/oppia/issues/23577#issuecomment-3409130188), [Issue #23452](https://github.com/oppia/oppia/issues/23452) | Comunicação com maintainer e análise de bugs. |
|Finalizando PR de Front-end da troca de imagens para imagens de maior qualidade!| Concluído | [Issue #23387](https://github.com/oppia/oppia/issues/23387) |Erro na pipeline devido ao versionamento errado do repositório corrigido. |
| Investigação e desenvolvimento da solução | Parcial | [Issue #23452](https://github.com/oppia/oppia/issues/23452) | Testes locais e início da implementação (Issue #23452). |



---

| Integrante    | Contribuições                                                                         | Links (PRs, Issues, Docs)                   | Observações          |
| ------------- | ------------------------------------------------------------------------------------- | ------------------------------------------- | -------------------- |
| Luiza Maluf   | - Tentativa de submissão do PR #22727<br>- Investigação de erros de backend e linting que impedem pre-push<br>- Registro e detalhamento dos problemas no Discussions da comunidade<br>- Comunicação com maintainers para suporte e validação| [Issue #22727](https://github.com/oppia/oppia/issues/22727), [#23646](https://github.com/oppia/oppia/discussions/23646), [#23633](https://github.com/oppia/oppia/discussions/23633), [#23631](https://github.com/oppia/oppia/discussions/23631) | Foco em backend, testes e documentação |
| Lucas Bottino | - Investigação conjunta dos erros de backend e pre-push da issue #22727<br>- - Revisão dos arquivos modificados<br>- Testes locais para identificar causas de falha nos lint e nos testes unitários| [Issue #22727](https://github.com/oppia/oppia/issues/22727), [#23646](https://github.com/oppia/oppia/discussions/23646), [#23633](https://github.com/oppia/oppia/discussions/23633), [#23631](https://github.com/oppia/oppia/discussions/23631) | Trabalho colaborativo em backend e validação de alterações |
| Maria Alice Bernardo | - Identificação e correção de bug de responsividade no editor de questões (UI).<br>- Investigação de sobreposição de CSS (`::ng-deep`, `margin` negativo) em componentes Angular.<br>- Diagnóstico e solução de problemas de ambiente Docker/WSL (`docker cp`, `pre-commit hooks`, `watch mode`)<br>- Submissão do PR da correção de UI. | [Issue #23439](https://github.com/oppia/oppia/issues/23439)<br>[PR #23648](https://github.com/oppia/oppia/pull/23648) | Foco em frontend (Angular/CSS), responsividade e configuração de ambiente. |
| Bianca Patrocínio | - Busca e análise de Issues para contribuição.<br>- Discussão e análise de bug na Issue #23577 (tela de doação).<br>- Comunicação direta com Maintainer por e-mail.<br>- Abertura de discussão na Issue #23452 para esclarecimento de bug.<br>- Testes locais e início de desenvolvimento da solução para a Issue #23452. | [Issue #23577](https://github.com/oppia/oppia/issues/23577#issuecomment-3409130188)<br>[Issue #23452](https://github.com/oppia/oppia/issues/23452) | Foco em análise de Issues, comunicação com a comunidade e preparação para desenvolvimento. |
| Nathan Abreu e Pedro Sampaio | - Finalização e Merge do PR #23560 (Low Resolution Images).<br>- Início das contribuições de tradução (Inglês -> Português) na plataforma.<br>- Recebimento de badges da comunidade.| [PR #23560](https://github.com/oppia/oppia/pull/23560) | Merge aprovado; Foco migrado para traduções (Energia Renovável). |
| Gabriel Moura dos Santos | - Contribuição com traduções de conteúdo educacional para português<br>- Tradução de lições de energia do inglês para o português<br>- Adaptação de conteúdo para o contexto brasileiro<br>- Documentação das contribuições realizadas | Plataforma Oppia, \fotos\image1.png | Foco em tradução e localização |


## 4. Maiores Avanços

✨ **Destaques da Sprint:**

- Identificação e documentação de problemas críticos que bloqueiam o push no PR #22727.
- Abertura de três discussions no repositório oficial para suporte e orientação dos maintainers.
- Diagnóstico e solução de problemas complexos de configuração de ambiente (Docker/WSL), permitindo a execução correta dos `pre-commit hooks` e a compilação de frontend (`watch mode`).
- Participação ativa em discussões técnicas nas Issues, ajudando a validar bugs e a redefinir escopos.
- Aprovação e merge do primeiro Pull Request de código da equipe (PR #23560).

---

## 5. Maiores Dificuldades

**Principais desafios enfrentados:**

- Falhas de pre-push devido a testes backend quebrando.
- Dependência da validação e suporte dos maintainers para corrigir erros complexos.
- Configuração inicial do ambiente de desenvolvimento no Windows (WSL), especificamente a lentidão do `docker cp` e a falha dos `pre-commit hooks` ao commitar pela UI do VS Code.
- Depuração de CSS em componentes Angular aninhadose análise de regras de CSS conflitantes entre componentes.
- Erro de pipeline dos testes unitários do repositório que falham com a versão diferente do Python.

---

## 6. Lições Aprendidas

- A importância de registrar e comunicar problemas técnicos de forma clara à comunidade.
- Experiência prática em investigar falhas de CI/CD e pre-push hooks em um projeto grande.
- Aprendizado sobre a estabilidade do backend e manutenção de testes durante alterações globais.
- Valor do trabalho colaborativo para resolver problemas complexos no código. 
- Os `pre-commit hooks` são executados no ambiente onde o comando `git` é chamado (WSL) e podem falhar se chamados de uma GUI (VS Code) que usa um Git diferente (Windows).
- Compreensão do fluxo de trabalho e triagem do Oppia: a tag triage needed é crucial e indica que a Issue ainda não está validada para desenvolvimento.
- A importância de registrar e comunicar problemas técnicos (sejam de ambiente ou de bugs) de forma clara à comunidade.
- O valor da análise e discussão nas Issues: um comentário pode validar o fechamento de uma Issue (ex: componente externo) ou ajudar a redefinir o escopo de um bug (ex: Issue #23452).

---

## 7. Planejamento para a Próxima Sprint

- [ ] Corrigir erros de backend e linting conforme orientação dos maintainers.
- [ ] Submeter finalmente o PR da issue #22727 com todas as evidências de testes passando.
- [ ] Monitorar o PR #23647 e responder a revisões dos maintainers.
* [ ] Trabalhar na Issue #23452
- [ ] Traduzir exercícios de inglês para francês.
