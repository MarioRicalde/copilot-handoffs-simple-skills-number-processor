# README

Repository containing an example of GitHub Copilot handoffs for agents. The goal of this implementation is to have a simple clean experiment to understand the inputs and outputs.

This repository is part of a series of repositories exploring GitHub Copilot specific features. To find other repositories, [search for topic:0-awesome-copilot](https://github.com/topics/0-awesome-copilot)

## Simple Number Processor Flow

![alt text](plan.drawio.png)

### Inputs and Outputs

Using `number-converter-first` agent, provide a number: `1234` as input.

This should trigger the whole flow and produce the final decorated output:

| N | R | E | S |
|-----|---|---|---|
| 1234 | MCCXXXIV | 1️⃣2️⃣3️⃣4️⃣ | one thousand two hundred thirty four |

### Local Observations

This implementation uses a SKILL.md file to keep the critical "Do not stop working on this issue until there are no further subagents to run." instruction.

As of **12/25/2025** this feature requires a experminental flag to be enabled in your GitHub Copilot setting `chat.useAgentSkills`. And it seems to work with every model BUT the `gpt-` models.

Works well with:
- Grok Code Fast 1
- Raptor mini (Preview)
- Claude Haiku 4.5
- Claude Opus 4.5
- Gemini 3 Flash (Preview)
- Gemini 3 Pro (Preview)

Does not work with:
- GPT-5.2
- GPT-5.1-Codex
- GPT-5.1-Codex-Max

This is not documented anywhere currently, so your mileage may vary.

## Observations

Observations live in a separate repository: [MarioRicalde/copilot-observations](https://github.com/MarioRicalde/copilot-observations).

