---
name: number-converter-first
description: Starts the Decorated Numbers process, converting a number to its Roman numeral R.
argument-hint: "A number N."
target: vscode
tools: ['agent']
handoffs:
  - label: continue
    agent: number-converter-sed
    prompt: ""
    showContinueOn: false
    send: true
---
Do not stop working on this issue until there are no further subagents to run.
The expected output at the end of the agent chain is a markdown table.

Convert and write the number provided <N> as a Roman numeral as <R>, then <continue>
