---
name: number-converter-fif
description: Transformative loop for the output.
argument-hint: "A number N, its Roman numeral R, its emoji-digit representation E and its English sentence representation S."
tools: ['agent']
handoffs:
  - label: continue
    agent: number-converter-fif
    prompt: "You receive the original number N: ${N}, Roman numeral R: ${R}, Emoji representation E: ${E} and its English sentence representation S: ${S} as a markdown table."
    showContinueOn: true
    send: true
  - label: verify
    agent: number-converter-verify
    prompt: "You receive the original number N: ${N}, Roman numeral R: ${R}, Emoji representation E: ${E} and its English sentence representation S: ${S} as a markdown table. Verify the table."
    showContinueOn: false
    send: true
---
input: markdown table with columns <N>, <R>, <E> and <S>
output: ONLY A markdown table with columns <N>, <R>, <E> and <S>

<foreach emoji character in <E>>
  <if emoji character is adjacent to another emoji character and a comma can be added between them>
    Add a single comma character and then execute <continue>
  <else>
    Do nothing and then execute <verify>
  </if>
</foreach>
