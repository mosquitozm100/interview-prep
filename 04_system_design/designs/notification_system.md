# Notification System

## 中文理解

通知系统是异步投递系统。核心是 fanout、渠道、重试、幂等、用户偏好和可观测性。

## Requirements

- Send email, push, SMS, or in-app notifications.
- Respect user preferences.
- Retry transient failures.
- Track delivery status.

## APIs

- `POST /notifications`
- `GET /notifications/{id}`

## Data Model

- Notification request
- User preference
- Delivery attempt
- Template

## High-Level Design

- API receives request and writes job.
- Queue fans out by channel.
- Workers call providers.
- Status and attempts are stored.

## Deep Dives

- Idempotency key for duplicate requests.
- Dead-letter queue for repeated failure.
- Rate limits per provider.

## Bottlenecks

- Provider limits.
- Large fanout.
- Retry storms.

## Tradeoffs / 取舍

- Synchronous send gives immediate result but poor reliability.
- Async send improves resilience but needs status tracking.

## Failure Modes

- Provider outage.
- Duplicate notification.
- Preference stale.

## English Interview Script

I would design notifications as an async pipeline with durable jobs, channel-specific workers, retries, idempotency, and delivery observability.

## TODOs

- Add provider fallback strategy.
