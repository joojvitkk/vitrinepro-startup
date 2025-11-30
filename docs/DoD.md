Definition of Done (DoD) – VitrinePro
A história só pode ser considerada “Done” quando:

1. Código
O código foi implementado conforme a User Story.
Está versionado no GitHub.
Passa pelos testes básicos definidos para a sprint.
Não contém erros conhecidos.
Segue boas práticas de organização e nomeação.

2. Funcionalidade
Atende integralmente ao que a User Story descreve.
Critérios de aceitação foram atendidos.
Funciona no ambiente local sem erros.
Não gera comportamento inesperado.
Foi revisado por outro membro do time (ou autoavaliação quando o grupo é pequeno).

3. Interface / UX
Interface clara e responsiva.
Botões, labels e feedbacks estão visíveis e funcionando.
Mensagens de erro e sucesso foram implementadas.

4. Documentação
README foi atualizado quando necessário.
A história foi marcada como concluída no backlog.
Qualquer endpoint, componente ou módulo criado foi documentado em /docs.

5. Testes
Testes manuais executados e registrados.
Bugs encontrados foram corrigidos.
O comportamento final foi validado pelo Product Owner.

6. Deploy Local
A aplicação roda localmente com um único comando ou instrução simples.
Dependências estão documentadas.

## Qualidade e Revisão (Extensão da DoD)

Além dos critérios já existentes, a entrega só será considerada concluída quando:

- [ ] Houver branch específica para a tarefa (feature/hotfix).
- [ ] A implementação tiver passado por code review, seguindo o checklist em `docs/Processos-Qualidade-Revisao.md`.
- [ ] A funcionalidade tiver sido testada manualmente e as evidências estiverem anexadas na Pull Request.
- [ ] Não houver erros aparentes no console ou falhas graves nos fluxos principais.
- [ ] A documentação mínima tiver sido atualizada (README, exemplos, textos da interface).

