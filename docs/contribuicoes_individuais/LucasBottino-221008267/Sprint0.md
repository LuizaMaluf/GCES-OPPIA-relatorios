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
