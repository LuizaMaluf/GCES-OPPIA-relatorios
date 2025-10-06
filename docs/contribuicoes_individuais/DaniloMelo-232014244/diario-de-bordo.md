# Diário de Bordo – Danilo de Melo Ribeiro

**Disciplina:** Gestão da Configuração e Evolução de Software\
**Equipe:** Oppia\
**Comunidade:** Oppia

---

## Sprint 0 – \[25/08 – 10/09]

### Resumo da Sprint

Esta sprint inicial teve como foco a integração ao projeto Oppia e a estruturação da equipe. Os objetivos principais foram realizar o _onboarding_ no ecossistema do projeto, compreender suas diretrizes de contribuição e configurar o ambiente de desenvolvimento para futuras contribuições.

### Atividades Realizadas

| Data  | Atividade                                                               | Tipo (Código/Doc/Discussão/Outro) | Link/Referência                                                                                                                                      | Status    |
| :---- | :---------------------------------------------------------------------- | :-------------------------------- | :--------------------------------------------------------------------------------------------------------------------------------------------------- | :-------- |
| 25/08 | Criação do fork do repositório oficial                                  | Código                            | [Github](https://github.com/EngDann/oppia)                                                                                                           | Concluído |
| 25/08 | Análise da documentação e arquitetura do projeto                        | Estudo                            | [Overview-of-the-Oppia-codebase](https://github.com/oppia/oppia/wiki/Overview-of-the-Oppia-codebase)                                                 | Concluído |
| 04/09 | Mapeamento das diretrizes de contribuição e qualidade                   | Estudo                            | [Oppia Wiki](https://github.com/oppia/oppia/wiki)                                                                                                    | Concluído |
| 06/09 | Alinhamento da estratégia de trabalho da equipe                         | Discussão                         | Reunião interna da equipe                                                                                                                            | Concluído |
| 06/09 | Configuração do ambiente de desenvolvimento (Linux)                     | Código                            | [Installing Oppia (Linux; Docker)](https://github.com/oppia/oppia/wiki/Installing-Oppia-using-Docker)                                                | Concluído |
| 09/09 | Criação do relatório de contribuição individual                         | Doc                               | -                                                                                                                                                    | Concluído |
| 10/09 | Preenchimento dos formulários para iniciar comunicação com a comunidade | Formulário                        | [Forms](https://docs.google.com/forms/d/e/1FAIpQLSfoFLKT4BlNH2937mSMJATVaWq-yBSrq8p3jjrPwcMw3gaGcg/alreadyresponded?c=0&w=1&fbzx=947187622883277373) | Concluído |

### Maiores Avanços

-   A equipe foi organizada e o fork do repositório, que servirá como base para as contribuições acadêmicas, foi criado com sucesso.
-   Foi obtida uma compreensão clara das políticas de contribuição, padrões de qualidade e fluxos de comunicação da comunidade Oppia.
-   O ambiente de desenvolvimento foi configurado e executado localmente com sucesso via Docker.

### Maiores Dificuldades

-   O processo de build inicial do projeto foi extenso, exigindo um alto consumo de recursos computacionais.

### Aprendizados

-   Compreensão aprofundada da estrutura do projeto Oppia, seu fluxo de trabalho e a organização da comunidade, incluindo os diferentes papéis e responsabilidades.
-   Aprofundamento prático em Docker, ferramenta escolhida para a configuração do ambiente.

### Plano Pessoal para a Próxima Sprint

-   [ ] Mapear e selecionar _issues_ relacionadas a CI/CD e DevOps para alinhar as contribuições com os meus objetivos pessoais e aproveitar ao máximo a disciplina.
-   [ ] Iniciar a colaboração ativa com a equipe e os mantenedores do Oppia para solucionar a _issues_ escolhidas.
-   [ ] Aplicar e consolidar os conhecimentos de CI/CD e DevOps através da contribuição prática no projeto.

---

## Sprint 1 – [10/09 – 24/09]

### Resumo da Sprint

Nesta sprint, eu reavaliei meu foco inicial no projeto. Descobri que o Oppia mantém um repositório dedicado ao Android, uma área que despertou muito mais meu interesse. Com isso, decidi concentrar meus esforços em compreender a fundo este novo repositório, sua estrutura e seus objetivos. Para me integrar mais rapidamente, entrei em contato com um contribuidor experiente do projeto e participante do GSoC, que me ajudou a esclarecer diversas dúvidas técnicas e sobre a comunidade.

### Atividades Realizadas

| Data  | Atividade                                                                  | Tipo (Código/Doc/Discussão/Outro) | Link/Referência                                                                            | Status    |
| :---- | :------------------------------------------------------------------------- | :-------------------------------- | :----------------------------------------------------------------------------------------- | :-------- |
| 15/09 | Identificação e análise inicial do repositório Oppia-Android               | Estudo                            | [GitHub: oppia-android](https://github.com/oppia/oppia-android)                            | Concluído |
| 16/09 | Estudo da arquitetura e das diretrizes de contribuição do Android          | Estudo                            | [Wiki: Developing for Oppia-Android](https://github.com/oppia/oppia-android/wiki)          | Concluído |
| 18/09 | Primeiro contato com um dos contribuidores da comunidade                   | Discussão                         | Comuinicação direta                                                                        | Concluído |
| 19/09 | Tive uma conversa com o mantenedor para esclarecer dúvidas sobre o projeto | Discussão                         | Comunicação direta (Discord/GitHub)                                                        | Concluído |
| 22/09 | Configurei o ambiente de desenvolvimento específico para o Android         | Código                            | [Guia de Instalação](https://github.com/oppia/oppia-android/wiki/Installing-Oppia-Android) | Concluído |

### Maiores Avanços

-   A descoberta de uma área no projeto (Android) que me motiva genuinamente a contribuir.
-   A conversa com o mantenedor foi fundamental. Ele compartilhou conhecimentos que aceleraram minha compreensão do projeto e da dinâmica da comunidade.
-   Agora tenho um entendimento claro da estrutura do projeto Android e de por onde posso começar a aplicar minhas habilidades.

### Maiores Dificuldades

-   A principal dificuldade foi a percepção de que meu foco inicial não era o ideal, o que consumiu parte do tempo da sprint e gerou a necessidade de correr atrás do prejuízo.
-   A configuração do ambiente de desenvolvimento foi desafiadora. O Android Studio exige muitos recursos computacionais, o processo de setup é longo e, após várias tentativas, a única versão que se mostrou compatível foi a "Giraffe".

### Aprendizados

-   Aprendi como é importante encontrar uma área de contribuição que esteja alinhada com meus interesses, pois a diferença na motivação é enorme.
-   Percebi que a comunicação proativa com membros experientes é uma ferramenta muito eficaz para acelerar o aprendizado.
-   Obtive um conhecimento prático valioso sobre a arquitetura de um aplicativo Android de código aberto e em larga escala.

### Plano Pessoal para a Próxima Sprint

-   [ ] Identificar e selecionar duas `good first issues` ou tarefas de escopo similar para começar a contribuir com código.
-   [ ] Focar na implementação para compensar o período de estudo e adaptação desta sprint.
-   [ ] O objetivo principal é submeter, no mínimo, 2 _Pull Requests_ (PRs) de qualidade.
