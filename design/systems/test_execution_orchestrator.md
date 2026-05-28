# Test Execution Orchestrator

## Problem Statement

Design a service that schedules and runs automated tests efficiently across many projects while handling retries, flaky tests, and result reporting.

## Requirements

- Accept test execution requests from CI or developers.
- Split test suites into executable shards.
- Schedule tests across workers.
- Retry failed or flaky tests using clear policy.
- Report results and logs.
- TODO: Define supported languages and test frameworks.

## Core Entities

- Test suite
- Test case
- Test shard
- Execution request
- Worker
- Test result
- Flaky test signal

## API / Interface

- `POST /test_runs`
- `GET /test_runs/{id}`
- `GET /test_runs/{id}/results`
- `POST /test_runs/{id}/cancel`

## High-Level Architecture

- API service receives requests.
- Planner creates shards.
- Scheduler assigns shards to workers.
- Workers run tests and stream logs.
- Result service aggregates outcomes.

## Key Flows

- CI asks for test run.
- Planner selects tests and creates shards.
- Workers execute shards in parallel.
- Aggregator reports pass/fail and retry outcomes.

## Scaling / Reliability

- Parallelize by shard.
- Use retries with limits and clear flaky classification.
- Preserve deterministic logs and artifacts.
- Prioritize critical test runs when capacity is limited.

## Observability

- Test duration by suite and shard
- Retry rate
- Flaky test rate
- Worker utilization
- Queue wait time

## Tradeoffs

- More sharding improves latency but adds scheduling overhead.
- Automatic retries reduce noise but can hide real failures.

## Interview Summary

I would design the orchestrator as a scheduler for test shards, with strong result aggregation, retry policy, flaky test tracking, and metrics that help teams improve reliability and speed.

