# Diário de Bordo – \[Paulo Henrique Rossi de Borba]

**Disciplina:** \[Gestão da Configuração e Evolução de Software]
**Equipe:** \[Oppia]
**Comunidade/Projeto de Software Livre:** \[Oppia]

---

## Sprint 0 – \[25/08 – 10/09]

### Resumo da Sprint

Nesta Sprint 0, o foco principal foi a imersão no projeto Oppia, compreendendo sua estrutura, diretrizes de contribuição e configuração do ambiente de desenvolvimento. Foram realizadas leituras essenciais, preenchidos formulários de contribuição e iniciado o processo de configuração do ambiente local.

### Atividades Realizadas

| Data  | Atividade | Tipo (Código/Doc/Discussão/Outro) | Link/Referência | Status |
| ----- | --------- | --------------------------------- | --------------- | ------ |
| 29/08 | Leitura e estudo do repositório do Oppia e guia de contribuição | Estudo                            | [Link](https://github.com/oppia/oppia/wiki/Overview-of-the-Oppia-codebase) | Concluído |
| 02/09 | Preenchimento do formulário de contribuição | Formulário |  [Link](https://docs.google.com/forms/d/e/1FAIpQLSfoFLKT4BlNH2937mSMJATVaWq-yBSrq8p3jjrPwcMw3gaGcg/viewform?c=0&w=1) | Concluído |
| 02/09 | Preenchimento do segundo formulário de contribuição | Formulário |  [Link](https://docs.google.com/forms/d/e/1FAIpQLSfiOd5WQp--PlbKAPmPLF14m0Ix2nTPwth9nb_48AHDv9fauw/viewform) | Concluído |
| 09/09 | Criação do fork do projeto | Código | [Link](https://github.com/paulohborba/oppia) | Concluído |
| 09/09 | Configuração do ambiente de desenvolvimento | Código | [Link](https://github.com/oppia/oppia/wiki/Installing-Oppia-%28Linux%3B-Python-3%29)   | Concluído |
| 09/09 | Criação do Diário de Bordo | Doc | (Página atual) | Concluído |

### Maiores Avanços

* Consegui entender o funcionamento do projeto, como as políticas de contribuição, qualidade e comunicação da comunidade Oppia.

* Os dois formulários para contribuição do projeto foram preenchidos.

* Consegui rodar o projeto localmente, apesar de ainda precisar de alguns ajustes.

* A equipe conseguiu se organizar de uma forma adequada.

### Maiores Dificuldades

* A configuração do ambiente de desenvolvimento teve diversos problemas.

* A configuração do ambiente de desenvolvimento ainda não está no nível que gostaria, mas espero conseguir ajustar.


### Aprendizados

* Consegui entender melhor o funcionamento de um projeto opensource de grande escala.

* Aprendi um pouco mais sobre configuração de ambientes de desenvolvimento.

### Plano Pessoal para a Próxima Sprint

* [ ] Ajustar o ambiente de desenvolvimento para ficar de acordo com minhas expectativas.
* [ ] Buscar issues "introdutórias" que me preparem para a integralização ao projeto.
* [ ] Melhorar a documentação pessoal e do grupo.
* [ ] Participar ativamente nas discussões, resoluções e dúvidas do grupo.

## Sprint 1 – \[10/09 – 24/09]

### Resumo da Sprint

Nesta Sprint 1, o foco principal foi novamente a imersão no projeto Oppia, compreendendo sua estrutura, diretrizes de contribuição, configuração do ambiente de desenvolvimento e também compreender melhor a contribuição de issues. Foi necessário refazer a configuração do ambiente de desenvolvimento.

### Atividades Realizadas

| Data  | Atividade | Tipo (Código/Doc/Discussão/Outro) | Link/Referência | Status |
| ----- | --------- | --------------------------------- | --------------- | ------ |
| 12/09 | Nova configuração do ambiente de desenvolvimento | Código |  [Link](https://github.com/oppia/oppia/wiki/Installing-Oppia-%28Linux%3B-Python-3%29) | Concluído |
| 15/09 | Entendimento sobre o funcionamento dos PRs | Estudo | [Link](https://github.com/oppia/oppia/wiki/Rules-for-making-PRs) | Concluído |
| 20/09 | Avaliando a primeira Issue para trabalhar| Estudo | - | Em andamento |

### Maiores Avanços

* Avanço no entendimento das diretrizes de Pull Request (PR) da comunidade Oppia

* Consegui configurar instalação na minha máquina.

* Revisão e refinamento do conhecimento sobre a arquitetura (frontend/backend).

### Maiores Dificuldades

* Persistência de conflitos de dependência no ambiente local (Python/Node).

* Grande curva de aprendizado necessária para entender o fluxo completo de contribuição em um projeto de grande porte.

### Aprendizados

* Dominar a configuração do ambiente (mesmo que instável) é o primeiro passo para contribuição efetiva.

* A leitura da documentação de PRs e guias de contribuição é crucial antes de iniciar o código.

### Plano Pessoal para a Próxima Sprint
* [ ] Finalizar a migração da configuração para Docker e estabilizar o ambiente.
* [ ] Escolher e reservar uma good first issue para começar.

## Sprint 2 – \[25/09 – 08/10]

### Resumo da Sprint

Nesta Sprint 2, foi necessário novamente ampliar a configuração do ambiente de desenvolvimento utilizando o docker dessa vez. O estudo sobre quais issues seriam ideais para começar, como contribuir e o início da realização dessa issue.

### Atividades Realizadas

| Data  | Atividade | Tipo (Código/Doc/Discussão/Outro) | Link/Referência | Status |
| ----- | --------- | --------------------------------- | --------------- | ------ |
| 12/09 | Configuração do ambiente de desenvolvimento utilizando Docker | Código |  [Link](https://github.com/oppia/oppia/wiki/Installing-Oppia-using-Docker) | Concluído |
| 15/09 | Entendimento sobre as issues ideais para começar | Estudo | [Link](https://github.com/oppia/oppia/issues?q=is%3Aopen+is%3Aissue+label%3A%22good+first+issue%22) | Concluído |
| 20/09 | Avaliando a primeira Issue para trabalhar| Estudo | [Link](https://github.com/oppia/oppia/issues/20003) ou [Link](https://github.com/oppia/oppia/issues/19763) | Em andamento |


### Maiores Avanços

* Identificação da necessidade de migrar para Docker devido à instabilidade do ambiente local.

* Configuração e build bem-sucedidos do ambiente com Docker, superando os desafios de dependência.

* Definição da primeira Issue a ser trabalhada, marcando a transição de estudo para contribuição.


### Maiores Dificuldades

* O tempo gasto para resolver erros durante o build do Docker.

* Selecionar uma boa primeira Issue a ser trabalhada.

### Aprendizados

* A importância da virtualização (Docker) para isolar e padronizar ambientes complexos como o Oppia.

### Plano Pessoal para a Próxima Sprint
* [ ] Finalizar a implementação da Issue escolhida.
* [ ] Criar o Pull Request (PR) seguindo rigorosamente as diretrizes da comunidade Oppia.
* [ ] Revisar e responder aos comentários de reviewers do PR de forma proativa.
* [ ] Tentar começar ou fazer mais uma issue.