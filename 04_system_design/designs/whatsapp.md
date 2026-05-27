# Realtime Messaging / WhatsApp

## 中文理解

实时消息系统重点是连接、消息持久化、投递、顺序、离线同步和多设备。不要只讲 WebSocket。

## Requirements

- Send and receive messages in near real time.
- Support offline delivery.
- Preserve per-conversation ordering.
- Support presence if required.

## APIs

- `POST /messages`
- `GET /conversations/{id}/messages`
- WebSocket event: `message.new`

## Data Model

- Conversation
- Message
- Participant
- Delivery receipt

## High-Level Design

- WebSocket gateways manage connections.
- Message service persists messages.
- Delivery service fans out to online devices.
- Offline clients sync from storage.

## Deep Dives

- Message ordering per conversation.
- Reconnect and missed message recovery.
- Presence at scale.

## Bottlenecks

- Connection fanout.
- Hot group chats.
- Cross-region latency.

## Tradeoffs / 取舍

- Strict global ordering is expensive.
- Per-conversation ordering is usually enough.

## Failure Modes

- Gateway disconnects.
- Duplicate delivery.
- Client misses messages during reconnect.

## English Interview Script

I would separate connection gateways from durable message storage. Messages are persisted first, then delivered to online devices, and offline clients recover by syncing from the last acknowledged message.

## TODOs

- Add multi-device read receipt details.
