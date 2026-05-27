# Support Automation Eval

## 中文理解

Support automation eval 关注自动化是否真的帮用户解决问题，同时不能产生不安全、错误或不可追踪的动作。

## Core Concepts

- Resolution quality
- Escalation correctness
- Policy compliance
- User satisfaction signals
- Tool call accuracy

## Interview Talking Points

- Evaluate both final answer and workflow path.
- Include negative cases and edge cases.
- Use human review for policy-sensitive failures.

## System Design Hooks

- Conversation trace storage
- Tool call audit logs
- Eval datasets from anonymized scenarios
- Escalation queue

## Failure Modes

- Incorrect resolution
- Failure to escalate
- Overconfident answer
- Tool misuse

## TODOs

- Add metric examples after role details are known.
