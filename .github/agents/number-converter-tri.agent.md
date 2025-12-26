---
name: number-converter-tri
description: Adds the English sentence representation as S.
argument-hint: "A number N, its Roman numeral R, and its emoji-digit representation E."
tools: ['agent']
handoffs:
  - label: continue-always
    agent: number-converter-forth
    prompt: ""
    showContinueOn: false
    send: true
---
Write the final English <sentence-representation> of the number <N> as <S>

<sentence-representation>
123 would be "one hundred twenty three".
</sentence-representation>
