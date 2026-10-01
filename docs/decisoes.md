# Diário de Decisões e Conflitos

## Conflito 1 – cor primária (`styles.css`, linha 2)
- **Causa:** B (`rename`) mudou `--primary` para `green` e C (`tema`) para `red`, na mesma linha.
- **Alternativas:** manter verde (B), manter vermelho (C) ou escolher um terceiro tom.
- **Decisão final:** manter `green`. A `rename` foi mesclada primeiro e o verde combina melhor com o tema claro e o escuro.
- **Quem resolveu:** Aluno A, 2026-10-01.

## Mesclas sem conflito (registradas por transparência)
- `app.js`: B e C alteraram o incremento/decremento para 2 em 2 com o mesmo conteúdo; o Git juntou sem conflito. A lógica do `toggleTheme` (C) também entrou sem conflito.
- `index.html`: C alterou `<title>` e `<h1>` ("Modo Escuro") e B alterou o rodapé ("Equipe B"); linhas diferentes, sem conflito.

## Pendências da Fase 2
- B não renomeou `setCount` para `updateCount`.
- B colocou "Equipe B" no rodapé, não no título.

## Hotfix – título no modo claro (`app.js`, linha 31)
- **Causa:** simulação de bug em produção na `main` (commit `020355a`): o título ficava fixo em "Modo Escuro" ao voltar para o modo claro.
- **Alternativas:** corrigir direto na `main` ou via branch `hotfix/titulo-claro`.
- **Decisão final:** hotfix em `hotfix/titulo-claro`, mesclado direto na `main` (commit `12ade4a`) e sincronizado com a `develop`, sem conflito.
- **Quem resolveu:** Aluno B (Alan), sincronização pelo Aluno A, 2026-10-01.

## Pendência registrada
- O Aluno B colocou "Equipe B" no rodapé do `index.html`, e a tarefa pedia no título. Mantido no rodapé: não gerou conflito com o título "Modo Escuro" do Aluno C e não afeta o funcionamento.

## Observações de processo
- As branches de feature foram nomeadas `rename` (B) e `tema` (C), fora da convenção `feature/*` combinada.
- O histórico foi reescrito localmente pelo Aluno A para trocar o autor dos commits, mas a reescrita não foi enviada ao GitHub porque quebraria as branches de B e C.
