# Agent Orchestration

## 中文理解

Agent orchestration 是把模型调用、工具调用、状态和控制流连接起来。面试重点是可靠性、可恢复性、权限和可观测性。

## Core Concepts

- Workflow state
- Step execution
- Tool gateway
- Retry and idempotency
- Human approval
- Trace logging

## Interview Talking Points

- Durable state is more reliable than in-memory chains.
- Tool calls need permissions, audit logs, and safe retries.
- Traces are essential for debugging multi-step failures.

## System Design Hooks

- State machine
- Async worker queue
- Tool execution service
- Trace store

## Failure Modes

- Infinite loop
- Partial tool success
- Repeated action
- Missing approval gate

## TODOs

- Add example workflow after safe details are verified.
