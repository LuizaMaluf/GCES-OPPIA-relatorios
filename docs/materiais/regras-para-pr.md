# Regras para fazer PRs

Esta página fornece as regras para fazer pull requests (PRs) no repositório do Oppia. Seguir estas regras ajuda a garantir que seu PR seja revisado e incorporado (merged) o mais rápido possível. Para dicas sobre como criar um PR de *alta qualidade*, consulte o guia [Criar um ótimo Pull Request (PR)](https://github.com/LuizaMaluf/GCES-OPPIA-relatorios/blob/main/docs/materiais/como-abrir-pr.md).

> **Nota:** Este guia é uma tradução e adaptação das [Regras para Fazer PRs da wiki oficial do Oppia](https://github.com/oppia/oppia/wiki/Rules-for-making-PRs). Recomendamos visitar o link original para visualizar imagens e exemplos ilustrativos.

## Regras

### 1. Garanta que seu PR esteja vinculado a uma issue

Todo PR deve resolver uma issue existente.

- **Vincule a issue** na descrição do seu PR usando a palavra-chave `Fixes #issue_number` (por exemplo, `Fixes #1234`). Isso garante que a issue seja fechada automaticamente quando o PR for incorporado.
- Se não houver uma issue para o seu trabalho, **crie uma primeiro** e descreva o bug ou a funcionalidade. Isso permite que a equipe discuta a mudança antes que você invista tempo no código.

### 2. Mantenha os PRs pequenos e focados

Cada PR deve tratar de **apenas uma issue**.

- **Não combine** correções de bugs não relacionadas, refatorações e novas funcionalidades em um único PR.
- PRs menores e focados são **mais fáceis de revisar**, o que leva a um feedback mais rápido e a uma incorporação mais veloz. Se o seu trabalho for grande, divida-o em vários PRs menores e independentes.

### 3. Escreva um título de PR claro e descritivo

O título do seu PR é a primeira coisa que um revisor vê. Ele deve ser conciso e informativo.

- **Formato:** Siga o padrão `Fixes #issue_number: [Breve descrição da mudança]`
- **Exemplo Bom:** `Fixes #4567: Add validation for user email format`
- **Exemplo Ruim:** `Fixed a bug`

### 4. Preencha o template do PR completamente

O template do PR existe para dar aos revisores o contexto de que precisam.

- **Explique o "o quê" e o "porquê"** das suas mudanças.
- **Inclua passos para teste** para que os revisores possam verificar seu trabalho.
- **Adicione capturas de tela** para mudanças visuais. Um PR sem uma descrição preenchida provavelmente será fechado.

### 5. Garanta que todos os testes passem

Seu PR deve passar em todas as verificações de Integração Contínua (CI), como os GitHub Actions.

- Um PR com testes falhando **não será revisado**.
- **Execute os testes localmente** antes de enviar seu PR para economizar tempo. Se um teste falhar no CI, investigue e corrija o problema.

### 6. Atualize a documentação, se necessário

Se suas mudanças afetam o comportamento do código, a arquitetura ou a experiência do usuário, atualize a documentação relevante. O código e a documentação devem estar sempre sincronizados.

### 7. Seu PR deve estar em inglês

Para garantir que todos na nossa comunidade global possam entender e colaborar, todo o conteúdo do PR (título, descrição, commits e comentários) **deve ser escrito em inglês**.

### 8. Limpe seu histórico de commits

- **Use `squash` ou `rebase`** para combinar commits relacionados em um único commit lógico antes de solicitar a revisão. Um histórico de commits limpo torna a revisão e a manutenção mais fáceis.
- Escreva mensagens de commit claras e descritivas.

### 9. Solicite a revisão das pessoas certas

Use a função "Reviewers" (Revisores) do GitHub para solicitar revisões. Se você não tiver certeza de quem contatar, pode marcar a equipe relevante (por exemplo, `@oppia/core-maintainers`).

### 10. Responda ao feedback prontamente

- Participe ativamente da conversa durante a revisão do seu PR.
- Responda aos comentários, faça as mudanças solicitadas e informe aos revisores quando o PR estiver pronto para uma nova rodada de revisão.

---

## Histórico de Versão

- **v1.0 (04/10/2025):** Primeira versão do documento, traduzida e adaptada por Bianca Patricinio.