---
name: number-converter-fif
description: Transformative loop for the output.
argument-hint: "A number N, its Roman numeral R, its emoji-digit representation E and its English sentence representation S."
tools: ['agent']
handoffs:
  - label: continue-if-adjacent-emojis
    agent: number-converter-fif
    prompt: ""
    showContinueOn: false
    send: true
  - label: verify-table
    agent: number-converter-verify
    prompt: ""
    showContinueOn: false
    send: true
---
input: markdown table with columns <N>, <R>, <E> and <S>
output: ONLY A markdown table with columns <N>, <R>, <E> and <S>

<foreach emoji character in <E>>
  <if emoji character is adjacent to another emoji character and a comma can be added between them>
    Add a single comma character and then <continue-if-adjacent-emojis>
  <else>
    Do nothing and then execute <verify-table>
  </if>
</foreach>
