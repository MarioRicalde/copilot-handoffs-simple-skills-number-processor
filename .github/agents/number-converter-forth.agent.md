---
name: number-converter-forth
description: Prepares table output for further processing.
argument-hint: "A number N, its Roman numeral R, its emoji-digit representation E and its English sentence representation S."
tools: ['agent']
handoffs:
  - label: continue-always
    agent: number-converter-fif
    prompt: ""
    showContinueOn: false
    send: true
---
Write a markdown table that includes: <N>, <R>, <E> and <S>
