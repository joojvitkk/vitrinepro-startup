# Processos de Qualidade e Revisão de Código

Este documento descreve como o time da startup **VitrinePro** organiza o versionamento de código, o fluxo de revisão (code review) e as regras mínimas de qualidade que fazem parte da Definition of Done (DoD).

---

## 1. Regras de Versionamento (GitFlow Simples)

Adotamos um fluxo simplificado inspirado no GitFlow, adequado para um time pequeno.

### 1.1. Branches principais

- `main`: 
  - Contém o código estável e pronto para entrega/apresentação.
  - Toda entrega de Sprint deve estar integrada e funcionando na `main`.
- `develop` (opcional, se o time crescer):
  - Branch de integração de funcionalidades antes de chegar na `main`.
  - No início do projeto, podemos trabalhar direto a partir da `main` + feature branches.

### 1.2. Branches de funcionalidade (feature branches)

- Criadas a partir de `main` (ou `develop`, se estiver sendo usada).
- Nome padrão:  
  - `feature/nome-curto-da-feature`
  - Ex.: `feature/login-usuario`, `feature/listagem-catalogos`.

### 1.3. Branches de correção (hotfix branches)

- Criadas a partir de `main` para corrigir problemas críticos em produção/demonstração.
- Nome padrão:  
  - `hotfix/descricao-curta`
  - Ex.: `hotfix/ajuste-login`, `hotfix/corrige-build`.

### 1.4. Fluxo de trabalho

1. Abrir uma branch de feature:
   - `git checkout -b feature/nome-da-feature`
2. Implementar a funcionalidade, seguindo checklist de qualidade.
3. Comitar com mensagens claras:
   - Padrão: `<tipo>: descrição`
   - Ex.: `feat: adiciona tela de login`, `fix: corrige validação de email`.
4. Abrir Pull Request (ou Merge Request) para `main`.
5. Passar pelo code review (mínimo 1 revisor).
6. Após aprovação, fazer merge na `main`.
7. Deletar a branch de feature.

---

## 2. Processo de Code Review

Todo código que altera comportamento do sistema **deve passar por revisão**, mesmo que o time seja pequeno (pair review ou self review estruturado).

### 2.1. Quando é obrigatório code review?

- Novas funcionalidades.
- Alterações em regras de negócio.
- Refatorações relevantes.
- Correções de bugs críticos.

### 2.2. Quem revisa?

- Ideal: outro desenvolvedor do time.
- Se não houver alguém disponível:
  - O autor faz um **self review estruturado**, preenchendo o checklist de revisão e registrando na Pull Request.

### 2.3. Como o review é registrado?

- Via Pull Request na plataforma Git (GitHub).
- O revisor deve:
  - Comentar pontos de melhoria.
  - Confirmar o checklist de qualidade.
  - Aprovar formalmente o PR (ou, em último caso, registrar o review na descrição do commit).

---

## 3. Checklist de Revisão de Código

Antes de aprovar uma Pull Request (ou considerar o código “pronto”), o revisor deve validar os seguintes itens:

1. **Correção e Requisitos**
   - [ ] A funcionalidade atende ao requisito descrito na User Story.
   - [ ] Não quebra funcionalidades já existentes (teste básico de regressão manual).
   - [ ] Mensagens de erro/sucesso são claras para o usuário.

2. **Qualidade de Código**
   - [ ] Não há código morto/comentado desnecessário.
   - [ ] Nomes de variáveis, funções e arquivos são descritivos.
   - [ ] Funções não estão excessivamente longas ou fazendo “de tudo um pouco”.
   - [ ] Não há duplicação óbvia de lógica (código copy-paste que deveria ser função).

3. **Padrões e Organização**
   - [ ] O código segue o padrão de estrutura do projeto (pastas, componentes, services etc).
   - [ ] Não foram introduzidas bibliotecas sem alinhamento prévio.
   - [ ] Arquivos estão no módulo/camada correta (ex.: lógica de negócio não está misturada na camada de view).

4. **Testes e Validação**
   - [ ] A funcionalidade foi testada manualmente nos principais fluxos.
   - [ ] Casos de erro mais comuns foram simulados (ex.: campos obrigatórios, formato inválido).
   - [ ] Se houver testes automatizados, foram atualizados e estão passando.

5. **Versionamento**
   - [ ] A branch está atualizada com a `main` (ou `develop`) para evitar conflitos.
   - [ ] A mensagem de commit é clara e segue o padrão acordado.

---

## 4. Atualização da Definition of Done (DoD)

A partir deste documento, **a DoD passa a incluir obrigatoriamente**:

- [ ] Código integrado em branch específica (`feature/...`, `hotfix/...`).
- [ ] Pull Request aberto e revisado (por outra pessoa ou self review com checklist).
- [ ] Checklist de revisão preenchido (no PR ou no corpo do commit).
- [ ] Funcionalidade testada manualmente, com evidência:
  - Prints de tela, GIFs ou descrição clara do teste realizado.
- [ ] Sem erros evidentes no console (frontend/backend).
- [ ] Documentação mínima atualizada (README, comentários essenciais, exemplos de uso se necessário).

A tarefa só pode ser marcada como **concluída** quando todos esses itens forem atendidos.

