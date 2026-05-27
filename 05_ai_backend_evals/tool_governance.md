# Tool Governance

## 中文理解

Tool governance 是控制 agent 能调用什么工具、什么时候调用、用什么参数、是否需要审批，以及如何审计。

## Core Concepts

- Permission model
- Tool registry
- Policy checks
- Approval gates
- Audit logs
- Rate limits

## Interview Talking Points

- Treat tool calls like privileged backend actions.
- Separate model suggestion from policy enforcement.
- Log decisions for debugging and compliance.

## System Design Hooks

- Tool gateway
- Policy engine
- Per-tenant configuration
- Audit log pipeline

## Failure Modes

- Over-permissive tool access
- Missing audit trail
- Unsafe retries
- Policy drift

## TODOs

- Add sample policy model.
