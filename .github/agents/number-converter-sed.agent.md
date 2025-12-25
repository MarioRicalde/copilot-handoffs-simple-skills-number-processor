---
name: number-converter-sed
description: Adds an emoji-digit representation as E.
argument-hint: "A number N and its Roman numeral R."
tools: ['agent']
handoffs:
  - label: continue
    agent: number-converter-tri
    prompt: ""
    showContinueOn: true
    send: true
---
Convert and write the number provided <N> as an <emoji-digit> representation <E> then <continue>

<emoji-digit>
Using <N>, convert each digit:
0-9 to 0️⃣ 1️⃣ 2️⃣ 3️⃣ 4️⃣ 5️⃣ 6️⃣ 7️⃣ 8️⃣ 9️⃣
</emoji-digit>
