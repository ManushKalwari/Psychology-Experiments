# Behavioral Economics Experiments with LLM Agents

The goal is to explore whether language models reproduce human-like behavioral patterns in trust, cooperation, punishment, and risk decisions. Each experiment models participants, prompts LLM agents to make decisions, extracts actions, and logs results for analysis. 

This work was conducted as part of research at the Moran Cerf Lab (Columbia University).

---
## Motivation

Do LLMs behave like humans in economic experiments?

Behavioral-economics experiments test:
- cooperation
- fairness
- punishment
- trust
- risk preferences
  
---
## Experiments

### 1. Prisoner’s Dilemma (1993)

Simulates repeated Prisoner’s Dilemma games under multiple matching conditions.

- Multi-game repeated interactions
- Payoff-matrix environment
- LLM-based player decisions
- Optional tit-for-tat computer opponent

---
### 2. Public Goods Game with Punishment (2000)

- Stage 1: Agents decide contributions
- Stage 2: Agents assign punishment points to others
- Punishment reduces payoff and has a cost

The simulation runs multiple periods with persistent group membership.

---
### 3. Gender Trust Game (1999)

- Sample and pair participants from demographic distributions
- Proposer sends money (0–1000)
- Amount is tripled
- Responder returns some amount

---
### 4. Decomposing Trust Experiment (2006)

Sub-experiments-
1. Dictator game
2. Triple dictator game
3. Trust game
4. Risk-preference task

- Trustor chooses send amount and expected return
- Trustee provides a return schedule for possible transfers
- Multiple GAMBLE vs SURE decisions

---
## Architecture

- Prompt-based decision generation 
- Dataclass-based state tracking
- Structured extraction using LLMs

Models:
- Llama-3.2-3B-Instruct
- Qwen-2.5-7B-Instruct
  
---
## Future Work

- multi-model comparisons
- statistical validation against original studies
- testing RL fine-tuned LLMs

Note:
The experiment-definition file (`experiments_v3.json`) used in this project is not included in the repository due to research-data access restrictions. The codebase is written so that experiments can be reproduced using any JSON file that follows the same schema as described in the experiment loaders.

