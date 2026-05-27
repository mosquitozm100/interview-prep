# URL Shortener

## 中文理解

URL shortener 是经典读多写少系统。重点是短码生成、跳转低延迟、缓存、过期和恶意链接处理。

## Requirements

- Create short URL from long URL.
- Redirect short URL to long URL.
- Support custom aliases if needed.
- Track basic analytics if required.

## APIs

- `POST /urls`
- `GET /{short_code}`

## Data Model

- URL mapping: short_code, long_url, owner, created_at, expires_at
- Click event: short_code, timestamp, user_agent, referrer

## High-Level Design

- Write path generates unique code and stores mapping.
- Read path resolves code through cache then database.
- Analytics events go to queue.

## Deep Dives

- ID generation: base62 counter, Snowflake-style ID, or random code.
- Cache hot URLs.
- Abuse detection and blocklist.

## Bottlenecks

- Hot short URLs.
- Database lookup latency.
- Analytics write volume.

## Tradeoffs / 取舍

- Random code avoids central counter but needs collision handling.
- Sequential ID is simple but may reveal volume.

## Failure Modes

- Cache miss storm.
- Duplicate custom alias.
- Malicious link redirects.

## English Interview Script

I would optimize the read path because redirects dominate traffic. The service stores URL mappings, caches hot short codes, and sends analytics asynchronously so redirects stay fast.

## TODOs

- Add capacity estimation.
