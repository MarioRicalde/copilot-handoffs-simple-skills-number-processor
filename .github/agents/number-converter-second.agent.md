---
name: number-converter-second
description: Adds an emoji-digit representation as E.
argument-hint: "A number N and its Roman numeral R."
tools: ['vscode', 'read', 'edit', 'todo', 'agent', 'search']
handoffs:
  - label: continue-with-decoration-process
    agent: number-converter-third
    prompt: "You receive the original number N: ${N}, Roman numeral R: ${R}, and Emoji representation E: ${E}."
    showContinueOn: true
    send: true
---
Convert and write the number provided <N> as an <emoji-digit> representation <E> then <continue-with-decoration-process>

<emoji-digit>
Using <N>, convert each digit:
0-9 to 0️⃣ 1️⃣ 2️⃣ 3️⃣ 4️⃣ 5️⃣ 6️⃣ 7️⃣ 8️⃣ 9️⃣
</emoji-digit>
