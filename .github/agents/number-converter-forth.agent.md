---
name: number-converter-forth
description: Finalizes the output.
argument-hint: "A number N, its Roman numeral R, its emoji-digit representation E and its English sentence representation S."
tools: ['agent']
handoffs:
  - label: comma-output
    agent: number-converter-fif
    prompt: "You receive the original number <N>, Roman numeral <R>, Emoji representation <E> and its English sentence representation <S> as a markdown table. Create final output."
    showContinueOn: true
    send: true
---
Write a markdown table that includes: <N>, <R>, <E> and <S>.
