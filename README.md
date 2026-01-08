# RabbitMQ – Topic Exchange (Basic Example)

This repository contains a **very simple implementation of RabbitMQ using the `topic` exchange type**.  
The goal of this project is **learning**, not scale, not perfection—just understanding how messages flow.

---

## What is RabbitMQ?

RabbitMQ is a **message broker**.  
It sits between services and delivers messages **asynchronously**, so one service doesn’t block or crash another.

Think of it as a **post office**:
- Producers send messages
- RabbitMQ routes them
- Consumers receive what they subscribed to

---

## Why Topic Exchange?

A **topic exchange** routes messages based on **routing key patterns**.

It allows:
- Flexible routing
- One message → many consumers
- Filtering messages using wildcards

### Wildcards
- `*` → matches exactly one word  
- `#` → matches zero or more words  

### Example routing keys:
- order.created
- order.updated.email
- user.signup.success
