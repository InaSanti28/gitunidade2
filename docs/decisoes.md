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
