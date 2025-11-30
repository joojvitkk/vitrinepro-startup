# Plano de Garantia de Qualidade – VitrinePro

Este documento define como a equipe da startup **VitrinePro** garante a qualidade do produto ao longo do desenvolvimento.

---

## 1. Objetivos de Qualidade

- Garantir que as funcionalidades implementadas atendam aos requisitos definidos no backlog.
- Reduzir retrabalho e correções de última hora antes das entregas (Sprints/apresentações).
- Manter o código organizado, legível e fácil de evoluir.
- Evidenciar que houve revisão (não apenas “codar e empurrar”).

---

## 2. O que será validado?

Em cada entrega (User Story / tarefa), serão validados pelo menos:

1. **Aderência ao Requisito**
   - A funcionalidade atende ao que foi descrito na história de usuário.
   - Campos obrigatórios, regras de negócio e fluxos principais funcionam.

2. **Comportamento da Interface**
   - Navegação entre as telas principais funciona (login, cadastro, dashboard, listagem, ações).
   - Mensagens de feedback (sucesso/erro) são exibidas em pontos críticos.

3. **Qualidade de Código**
   - Estrutura de pastas coerente com a arquitetura definida.
   - Nomes descritivos para variáveis, funções e componentes.
   - Ausência de código morto ou comentários sem sentido.

4. **Estabilidade Básica**
   - Testes manuais dos fluxos principais realizados.
   - Ausência de erros evidentes no console (navegador/backend).
   - Build rodando sem falhas (quando aplicável).

---

## 3. Responsáveis pela Qualidade

- **Product Owner (PO):**
  - Valida se a funcionalidade atende ao requisito e gera valor para o usuário.
  - Aprova a entrega em termos de comportamento e experiência.

- **Desenvolvedor Autor da Tarefa:**
  - Responsável por seguir o checklist de qualidade antes de abrir o PR.
  - Realiza testes manuais básicos da funcionalidade implementada.

- **Revisor de Código (Dev ou outro membro da equipe):**
  - Analisa o código conforme o “Checklist de Revisão”.
  - Garante que a DoD está sendo cumprida antes do merge.

Em equipes muito pequenas, uma mesma pessoa pode acumular papéis, mas as **atividades** (desenvolver, revisar, validar) devem ser tratadas separadamente.

---

## 4. Como evidenciar a revisão e validação?

Para cada tarefa/feature, a equipe deve gerar evidências de qualidade:

1. **Pull Request no GitHub**
   - Descrição da funcionalidade implementada.
   - Link da User Story ou item do backlog.
   - Checklist de revisão preenchido (copiado do documento de processos).

2. **Comentários de Review**
   - Pelo menos um comentário confirmando a revisão (por outra pessoa ou self review).
   - Ajustes solicitados e respostas, quando houver.

3. **Evidência de Testes**
   - Prints de tela/gif do fluxo funcionando, anexados na PR.
   - Ou descrição clara dos testes manuais realizados (cenários principais).

4. **Registro de Decisões**
   - Decisões relevantes de arquitetura ou padrões devem ser anotadas no README ou em um arquivo `docs/DECISOES-ARQUITETURA.md` (quando existirem).

---

## 5. Localização no Repositório

- Este plano está versionado em:  
  `docs/Plano-Qualidade.md`
- O processo detalhado de revisão de código está em:  
  `docs/Processos-Qualidade-Revisao.md`
- A Definition of Done (DoD) está em:  
  `docs/DoD.md` (ou seção específica no `README.md`).

Qualquer alteração nas práticas de qualidade ou revisão deve ser refletida nestes documentos.

