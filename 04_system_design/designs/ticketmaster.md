# Ticketmaster / Booking

## 中文理解

订票系统核心是库存一致性、短暂锁定、支付超时和高并发热点。难点是不能超卖，同时要支持大量读流量。

## Requirements

- Browse events and seats.
- Reserve seats briefly.
- Complete payment.
- Release expired reservations.

## APIs

- `GET /events/{id}/seats`
- `POST /reservations`
- `POST /payments`

## Data Model

- Event
- Seat
- Reservation
- Order
- Payment

## High-Level Design

- Read path uses cache/search for event data.
- Reservation service owns inventory state.
- Payment flow confirms or releases reservation.
- Expiration worker releases timed-out holds.

## Deep Dives

- Seat locking and reservation TTL.
- Idempotent payment confirmation.
- Hot event traffic shaping.

## Bottlenecks

- Hot event inventory.
- Payment provider latency.
- Cache consistency for seat availability.

## Tradeoffs / 取舍

- Strong consistency for reservation state.
- Eventual consistency acceptable for browsing availability.

## Failure Modes

- Payment succeeds but confirmation fails.
- Reservation expires during payment.
- Hot event causes overload.

## English Interview Script

I would separate browsing from reservation. Browsing can be cached and eventually consistent, but reservation needs strong control over seat state with TTL holds and idempotent payment confirmation.

## TODOs

- Add detailed concurrency control options.
