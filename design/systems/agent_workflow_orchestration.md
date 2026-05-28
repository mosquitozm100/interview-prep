# Agent Workflow Orchestration

## Problem Statement

Design a backend system that runs multi-step agent workflows with durable state, tool calls, permissions, retries, and traceability.

## Requirements

- Start and track workflow runs.
- Execute model and tool steps.
- Persist workflow state.
- Enforce tool permissions.
- Support retries, cancellation, and human review.
- TODO: Define example workflow.

## Core Entities

- Workflow definition
- Run
- Step
- Tool call
- State snapshot
- Permission policy
- Trace event

## API / Interface

- `POST /workflows/{id}/runs`
- `GET /runs/{id}`
- `POST /runs/{id}/cancel`
- `GET /runs/{id}/trace`

## High-Level Architecture

- Orchestrator owns workflow state.
- Queue dispatches executable steps.
- Workers run model calls and tool calls.
- Tool gateway enforces permissions and audit logging.
- Trace store records step-level events.

## Key Flows

- Client starts workflow run.
- Orchestrator chooses next step.
- Worker executes model or tool call.
- State is updated and next step is scheduled.
- Human review is requested when policy requires it.

## Scaling / Reliability

- Persist state after every step.
- Make tool calls idempotent where possible.
- Limit retries and detect loops.
- Separate long-running jobs from request path.

## Observability

- Step latency
- Tool error rate
- Retry count
- Workflow success rate
- Trace-level debugging view

## Tradeoffs

- Fixed workflows are easier to debug and govern.
- Dynamic planning is more flexible but harder to control.

## Interview Summary

I would design agent orchestration around durable state, explicit step transitions, a permissioned tool gateway, and detailed traces so workflows are recoverable, auditable, and debuggable.

