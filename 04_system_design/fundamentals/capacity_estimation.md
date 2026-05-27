# Capacity Estimation

## 中文理解

容量估算不是为了精确，而是展示系统感。先估 QPS、读写比例、数据大小、峰值倍数，再推存储、带宽和分片需求。

## English Interview Script

I start with traffic assumptions, separate reads and writes, estimate data size, then identify the bottleneck: compute, storage, bandwidth, or hot keys.

## Common Numbers

- Daily active users: TODO
- Requests per user per day: TODO
- Peak multiplier: 2x-10x depending on product

## TODOs

- Add one worked example for eval platform.
- Add one worked example for rate limiter.
