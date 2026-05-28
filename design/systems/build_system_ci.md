# Build System / CI Platform

## Problem Statement

Design a platform that can run builds and CI checks reliably for many repositories, teams, and code changes.

## Requirements

- Trigger builds from commits, pull requests, or manual requests.
- Schedule build jobs across worker pools.
- Store logs, artifacts, and build results.
- Support retries, cancellation, and timeouts.
- TODO: Define scale assumptions.

## Core Entities

- Repository
- Commit / change
- Build pipeline
- Job
- Worker
- Artifact
- Build result

## API / Interface

- `POST /builds`
- `GET /builds/{id}`
- `POST /builds/{id}/cancel`
- Webhook from source control provider

## High-Level Architecture

- API service receives build requests.
- Scheduler breaks pipelines into jobs.
- Queue dispatches jobs to workers.
- Workers execute build steps in isolated environments.
- Storage keeps logs, artifacts, and results.

## Key Flows

- Pull request triggers build.
- Scheduler creates job graph.
- Workers execute jobs and upload artifacts.
- Result service updates commit status.

## Scaling / Reliability

- Use queues for backpressure.
- Autoscale workers by queue depth.
- Cache dependencies and build outputs when safe.
- Isolate jobs to avoid cross-build contamination.

## Observability

- Build duration
- Queue wait time
- Worker failure rate
- Cache hit rate
- Failed step logs

## Tradeoffs

- Strong isolation improves safety but increases cost.
- Aggressive caching improves speed but can create correctness risk.

## Interview Summary

I would design CI as an async job platform with durable scheduling, isolated workers, artifact storage, and strong observability around queue time, failure rate, and build latency.
