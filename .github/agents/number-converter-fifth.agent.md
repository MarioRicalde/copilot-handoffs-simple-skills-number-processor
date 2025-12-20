---
name: number-converter-fifth
description: Transformative loop for the output.
argument-hint: "A number N, its Roman numeral R, its emoji-digit representation E and its English sentence representation S."
tools: ['vscode', 'read', 'edit', 'todo', 'agent', 'search']
handoffs:
  - label: comma-output
    agent: number-converter-fifth
    prompt: "Continue adding commas as needed."
    showContinueOn: true
    send: true
---
Modify the markdown table that includes: <N>, <R>, <E> and <S>. Add a single comma after every one digits in the number <E> for better readability. Just insert one comma at a time.
