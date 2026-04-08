# Agent Improver

A meta-agent that optimizes other agents' prompt files (`.md`) for **determinism**, **context efficiency**, and **evaluation quality**.

## What It Does

Agent Improver rewrites agent prompt files along four axes:

| Axis | Goal |
|------|------|
| **Context Reduction** | Cut filler, deduplicate, consolidate — every token must earn its place |
| **Determinism** | Replace subjective guidelines with checklists, decision trees, and concrete examples |
| **LLM-as-Judge** | Anchor scores to observables, add calibration examples, require justification before scoring |
| **Context Placement** | Exploit U-shaped attention — critical content at the start/end, reference material in the middle |

## Usage

Point the agent at one or more `.md` prompt files. It will analyze, rewrite, and report token-count changes along with a summary of improvements.

## Constraints

- Does **not** change an agent's fundamental role or purpose
- Does **not** add new capabilities or tools
- Preserves all file paths and identifiers
- Aims to reduce token count while increasing the ratio of verifiable instructions to subjective guidelines
