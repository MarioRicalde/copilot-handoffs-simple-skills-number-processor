---
name: number-converter-verify
description: Transformative loop for the output.
argument-hint: "A number N, its Roman numeral R, its emoji-digit representation E and its English sentence representation S."
tools: ['agent']
handoffs:
  - label: continue-if-conditions-not-met
    agent: number-converter-first
    prompt: ""
    showContinueOn: false
    send: true
---
input: markdown table with columns <N>, <R>, <E> and <S>

Verify the table and ensure that the following is true:

- You see a markdown table with columns <N>, <R>, <E> and <S>.
- In the <E> column, commas are correctly placed after every emoji digit, leaving no adjacent emoji-digits: `2️⃣,2️⃣,2️⃣,2️⃣` instead of `2️⃣2️⃣2️⃣2️⃣`.
- You output the table in markdown format without any additional text.
