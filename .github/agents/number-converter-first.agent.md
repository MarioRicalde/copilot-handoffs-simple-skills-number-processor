---
name: number-converter-first
description: Starts the Decorated Numbers process, converting a number to its Roman numeral R.
argument-hint: "A number N."
target: vscode
tools: ['vscode', 'read', 'edit', 'todo', 'agent', 'search']
handoffs:
  - label: continue-with-decoration-process
    agent: number-converter-second
    prompt: "You receive a number N: ${N} and Roman numeral R: ${R}."
    showContinueOn: false
    send: true
---

Convert and write the number provided <N> as a Roman numeral as <R>, then <continue-with-decoration-process>
