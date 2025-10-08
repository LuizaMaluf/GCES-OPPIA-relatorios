# 📝 Relatório de Contribuição – Sprint 2

**Disciplina:** Gestão de Configuração e Evolução de Software

**Equipe:** \[Oppia]

**Comunidade/Projeto de Software Livre:** \[Oppia]

**Período da Sprint:** \[25/09 – 08/10]

---

## 1. Objetivos da Sprint


- Contribuir para a evolução do Oppia removendo a dependência do parâmetro `SERVER_CAN_SEND_EMAILS` em todo o código.
- Atualizar testes, controllers e cron jobs relacionados ao envio de emails.
- Garantir que as funcionalidades de email continuem funcionando corretamente sem a plataforma parameter antiga.
- Documentação de regras para PR.


---

## 2. Entregas Coletivas

| Entrega                     | Status (Concluído/Parcial/Pendente) | Link/Referência                                             | Observações           |
| --------------------------- | ----------------------------------- | ----------------------------------------------------------- | --------------------- |
| Remoção do parâmetro SERVER_CAN_SEND_EMAILS | Concluído | [Issue #22727](https://github.com/oppia/oppia/issues/22727) | Alterações em `admin.py`, `cron.py` e `utils.py` |
| Atualização de testes de email | Concluído | [Issue #22727](https://github.com/oppia/oppia/issues/22727) | Mock de requests implementado para testes de email |
| Revisão de código e testes finais | Concluído | [Issue #22727](https://github.com/oppia/oppia/issues/22727)| Testes manuais e unitários OK |


---

| Integrante    | Contribuições                                                                         | Links (PRs, Issues, Docs)                   | Observações          |
| ------------- | ------------------------------------------------------------------------------------- | ------------------------------------------- | -------------------- |
| Luiza Maluf   | - Identificação dos locais onde `SERVER_CAN_SEND_EMAILS` era utilizado<br>- Alterações em `admin.py` e controllers de email<br>- Atualização de testes unitários com mocks<br>- Verificação da funcionalidade do cron<br>- Discussão de abordagem e validação com maintainers| [Issue #22727](https://github.com/oppia/oppia/issues/22727) | Foco em backend e testes |
| Lucas Bottino | - Revisão das alterações feitas<br>- Ajustes em `cron.py` e `utils.py`<br>- Verificação de impactos nos envios de email |[Issue #22727](https://github.com/oppia/oppia/issues/22727) | Foco em backend e integração |
| Bianca Patrocinio| - Estudo na arquitetura do Oppia<br>- Tradução de regras da Wiki<br>- Nevegação pelas abas do site|[Como abrir uma boa PR](https://github.com/LuizaMaluf/GCES-OPPIA-relatorios/blob/main/docs/materiais/como-abrir-pr.md) [Regras para abrir uma PR](https://github.com/LuizaMaluf/GCES-OPPIA-relatorios/blob/main/docs/materiais/regras-para-pr.md) | Foco estudo e documentação |
| Nathan Abreu  | - Adicionei o aluno Pedro Sampaio para o meu fork para contribuirmos juntos na issue <br> - Ajustei a posição da imagem e subi para o fork principal <br> - Iniciamos o PR e estamos aguardando a a aprovação | [Issue #23387](https://github.com/oppia/oppia/issues/23386) | Foco em Front End|


## 4. Maiores Avanços

✨ **Destaques da Sprint:**

- Removemos com sucesso a dependência do parâmetro `SERVER_CAN_SEND_EMAILS`, simplificando o código e reduzindo condicionais desnecessárias.  
- Todos os testes de envio de email foram ajustados para funcionar com mocks, mantendo a cobertura de testes intacta.  
- Revisão colaborativa e validação das alterações antes de submeter o PR.  


---

## 5. Maiores Dificuldades

**Principais desafios enfrentados:**

- Encontrar todas as ocorrências do parâmetro no código distribuído pelo Oppia.  
- Ajustar testes sem quebrar a cobertura existente, principalmente com chamadas externas (URL requests).  

---

## 6. Lições Aprendidas

- Como manter a consistência de funcionalidades enquanto remove parâmetros obsoletos.  


---

## 7. Planejamento para a Próxima Sprint

- [ ] Submeter o PR final com todas as alterações e evidências de testes.  
