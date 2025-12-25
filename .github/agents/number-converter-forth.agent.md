---
name: number-converter-forth
description: Prepares table output for further processing.
argument-hint: "A number N, its Roman numeral R, its emoji-digit representation E and its English sentence representation S."
tools: ['agent']
handoffs:
  - label: continue
    agent: number-converter-fif
    prompt: "You receive the original number N: ${N}, Roman numeral R: ${R}, Emoji representation E: ${E} and its English sentence representation S: ${S} as a markdown table."
    showContinueOn: true
    send: true
---
Write a markdown table that includes: <N>, <R>, <E> and <S>. Then <continue>.
