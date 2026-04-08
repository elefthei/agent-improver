# Agent Improver

A meta-agent that optimizes other agents' prompt files (`.md`) for **determinism**, **context efficiency**, and **evaluation quality**.

## What It Does

Agent Improver rewrites agent prompt files along six axes:

| Axis | Goal |
|------|------|
| **Context Reduction** | Cut filler, deduplicate, consolidate — every token must earn its place |
| **Determinism** | Replace subjective guidelines with checklists, decision trees, and concrete examples |
| **LLM-as-Judge** | Gatekeeper triage (hard pass/fail gates), then anchor scores to observables with calibration examples |
| **Context Placement** | U-shaped attention (critical content at start/end) + KV-cache-aware ordering (static before volatile) |
| **Progressive Disclosure** | Tier content into selection → activation → full; load on demand, not all at once |

After rewriting, it validates quality using **probe-based evaluation** — recall, artifact, continuation, and decision probes that test whether the rewrite preserved critical information.

## Usage

Point the agent at one or more `.md` prompt files. It will analyze, rewrite, and report token-count changes along with a summary of improvements.

## Constraints

- Does **not** change an agent's fundamental role or purpose
- Does **not** add new capabilities or tools
- Preserves all file paths and identifiers
- Aims to reduce token count while increasing the ratio of verifiable instructions to subjective guidelines
