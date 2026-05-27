# Data Pipeline

## 中文理解

Eval 和 AI backend 的数据管道要处理 traces、labels、feedback、outputs 和 metrics。重点是数据质量、版本、隐私和可追溯。

## Core Concepts

- Event ingestion
- Dataset creation
- Label management
- Feature or trace extraction
- Aggregation and reporting
- Retention policy

## Interview Talking Points

- Keep raw events separate from curated eval datasets.
- Version datasets and graders.
- Track lineage from production event to eval case.

## System Design Hooks

- Streaming ingestion
- Batch processing
- Data warehouse
- Dataset registry

## Failure Modes

- Label noise
- Data leakage
- Missing lineage
- Skewed sampling

## TODOs

- Add anonymization and privacy notes.
