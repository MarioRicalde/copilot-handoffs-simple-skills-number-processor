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
