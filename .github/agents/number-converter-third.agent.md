---
name: number-converter-third
description: Adds the English sentence representation as S.
argument-hint: "A number N, its Roman numeral R, and its emoji-digit representation E."
tools: ['vscode', 'read', 'edit', 'todo', 'agent', 'search']
handoffs:
  - label: finalize-output
    agent: number-converter-forth
    prompt: "You receive the original number <N>, Roman numeral <R>, Emoji representation <E> and its English sentence representation <S>. Create final output."
    showContinueOn: true
    send: true
---

Write the final English <sentence-representation> of the number <N> as <S>. Then <finalize-output>

<sentence-representation>
123 would be "one hundred twenty three".
</sentence-representation>
