# Criar um ótimo Pull Request (PR)

Esta página é uma introdução sobre como criar um ótimo Pull Request (PR). Um ótimo Pull Request (PR) é mais do que apenas código — ele é limpo, claro e fácil para os revisores entenderem. Este guia compartilha as melhores práticas para escrever PRs de alta qualidade que são fáceis de revisar e rápidos de incorporar (merge).

> **Nota:** Este guia é uma tradução e adaptação do documento [Creating a great PR da wiki oficial do Oppia](https://github.com/oppia/oppia/wiki/Create-a-Good-PR#table-of-contents). Recomendamos visitar o link original para visualizar imagens e exemplos que ilustram as boas práticas.

## Por que isso é importante

Um bom pull request não se trata apenas de código funcional — trata-se de facilitar a colaboração. PRs claros e bem estruturados economizam o tempo dos revisores, reduzem a confusão e ajudam a manter a alta qualidade do código. Em projetos de código aberto (open source), PRs bem elaborados constroem confiança e mantêm o projeto sustentável para todos.

Para o checklist essencial e as melhores práticas, certifique-se de seguir as `Regras para fazer PRs` — todo bom PR começa por aí.

## Antes de Abrir seu PR

Certifique-se de que você:

  - Criou um branch a partir da `develop` mais recente
  - Baixou o código mais recente: `git pull upstream develop`
  - Testou suas alterações localmente
  - Passou em todos os testes relevantes
  - Limpou seu código (sem logs de depuração perdidos ou código comentado)
  - Escreveu um plano de correção (se necessário) e obteve aprovação

## O que torna um PR "Ótimo"

Aqui está o que faz um PR se destacar:

> **Nota Importante:** Todo o conteúdo do seu Pull Request (título, descrição, commits e comentários no código) deve ser escrito em **inglês**. Isso garante que colaboradores do mundo todo possam participar e entender o seu trabalho.

### 1\. Propósito Claro

Use um **título de PR descritivo em inglês** e mencione o número da issue.

**Bom:**

```
Fixes #4567: Correctly align navbar on small screens
```

**Ruim:**

```
Update UI stuff
```

### 2\. Escopo Focado

  - Mantenha **um tópico por PR**
  - Não inclua alterações não relacionadas
  - Mantenha seus PRs pequenos sempre que possível — PRs menores são mais rápidos de revisar

### 3\. Descrição Útil

Preencha o template do PR completamente (em inglês):

  - O que você mudou?
  - Por que foi necessário?
  - Alguma parte complicada?
  - Capturas de tela para alterações de UI
  - Perguntas para as quais você quer feedback

### 4\. Mostre, Não Apenas Descreva

Se o seu PR altera a interface do usuário (UI), **inclua capturas de tela de antes e depois**. Isso ajuda os revisores a entenderem instantaneamente o impacto visual.

### 5\. Testado e Verificado

Antes de solicitar a revisão:

  - Todos os testes passaram (unitários, de integração, lint)
  - Você testou manualmente (especialmente para alterações de UI ou lógica)
  - Casos de borda (edge cases) foram tratados

## Erros Comuns a Evitar

| ❌ Não Faça Isso | ✅ Faça Isso em Vez |
| :--- | :--- |
| Título "Corrigindo algumas coisas" ou em português | "Fix \#1234: Add padding to dashboard cards" |
| Combinar correções não relacionadas | Separar em PRs focados |
| Pular a descrição | Explicar claramente o quê e o porquê (em inglês) |
| Adicionar código inacabado | Enviar apenas código que está pronto |
| Esquecer capturas de tela | Adicionar prova visual para alterações de UI |

## Checklist Final Antes de Solicitar a Revisão

  - [ ] Meu PR aborda **penas um problema** (issue)
  - [ ] Meu PR está totalmente **escrito em inglês** (título, descrição, commits)
  - [ ] Eu segui o **estilo de código do Oppia**
  - [ ] Todos os **testes passaram**
  - [ ] Eu preenchi o **template do PR**
  - [ ] Eu incluí **capturas de tela** (se necessário)
  - [ ] Minha mensagem de commit está clara e formatada
  - [ ] Eu enviei o **código mais recente**
  - [ ] Estou pronto para **responder às revisões** prontamente

## O que os Revisores Apreciam...

  - Código limpo e legível
  - Histórico de commits claro
  - Contexto fornecido em comentários se algo não for óbvio
  - Respeito pelo tempo deles

## Precisa de Ajuda?

Não tenha medo de perguntar\! Você pode:

  - Marcar os revisores nos comentários
  - Usar as **Discussões (Discussions) do GitHub**

Obrigado por dedicar seu tempo para fazer seu PR brilhar.
PRs de alta qualidade tornam o Oppia melhor para todos\!

-----

## Histórico de Versão

  - **v1.0 (04/10/2025):** Primeira versão do documento, criada por Bianca Patricinio.