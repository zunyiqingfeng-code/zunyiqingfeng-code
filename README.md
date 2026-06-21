# AI Engineering Production System

I build low-cost, verifiable engineering workflows around coding agents,
simulation, and remote execution.

The core line:

```text
cheaper runtime
-> durable context
-> run-verify workflow
-> remote execution
-> human-reviewed delivery
```

## Project Map

| Layer | Repository | What it solves |
| --- | --- | --- |
| Verification | [matlab-deepseek-workflow](https://github.com/zunyiqingfeng-code/matlab-deepseek-workflow) | MATLAB / Simulink simulation needs numeric checks, reference comparison, and root-cause judgment. Running code is not enough. |
| Execution | [engineering-pod](https://github.com/zunyiqingfeng-code/engineering-pod) | Submit work from a phone or laptop, run long jobs on a server, and review artifacts before delivery. |
| Runtime | [claude-codex-proxy-stack](https://github.com/zunyiqingfeng-code/claude-codex-proxy-stack) | Local proxy work for cheaper backend routing, protocol differences, tool calls, context, and Windows edge cases. |
| Context | [context-guard](https://github.com/zunyiqingfeng-code/context-guard) | Long-session guardrails: handoff, monitoring, clearing, recovery notes, and memory search. |

## Current Focus

- Verifiable simulation workflows for engineering code.
- Remote execution patterns for long-running tasks.
- Deterministic checks before anything becomes a deliverable.
- Low-cost model routing without hiding the engineering tradeoffs.

## Selected Work

### matlab-deepseek-workflow

The main principle:

> Running is not correctness.

This repo documents a practical MATLAB / Simulink workflow: split tasks into
verifiable units, run short feedback loops, check numeric health, compare
against reference implementations, and locate root causes when curves look right
but the math is wrong.

### engineering-pod

A reference implementation of a personal remote engineering pod:

- submit tasks through an API or browser console;
- run them on a server with the real toolchain installed;
- keep long jobs detached from the local machine;
- apply deterministic delivery checks before review.

### claude-codex-proxy-stack

This repo is about the parts that decide whether an agent stack actually works:

- protocol translation;
- tool-call compatibility;
- local proxy routing;
- context and reasoning payload handling;
- Windows / local network edge cases.

### context-guard

Long sessions fail when memory, context, and recovery are treated as vibes. This
repo collects the defensive layer: session handoff, context monitoring, smart
clearing, recovery notes, and searchable session memory.

## Writing

- [用 DeepSeek 写代码,你怎么知道它写得对不对?](https://juejin.cn/post/7652621263220015144)

## Direction

The goal is not to collect tools. The goal is to build a small engineering
production system:

```text
write faster
verify harder
run remotely
deliver cleaner
```
