# Talyxion

## Copy trading, with the user still in control

[Open Talyxion](https://talyxion.com)

Talyxion is a quant-fintech platform built around three connected workflows: researching alpha, discovering strategies, and executing through a non-custodial DEX desk.

## The product idea

Users should be able to discover a strategy and follow its activity without handing custody of their assets to the platform. Talyxion coordinates the research, strategy, account connection, and trading workflow while the user's venue account or wallet remains the source of control.

## Core surfaces

| Surface | Purpose |
| --- | --- |
| Alpha research | Explore and evaluate systematic strategies |
| Strategy discovery | Understand what a strategy does before following it |
| Copy trading | Follow a strategy through a connected account |
| Non-custodial DEX desk | Execute with a user-controlled wallet or venue account |
| Risk controls | Pause, inspect, and manage an allocation safely |

## Engineering shape

The private monorepo uses Django and Django REST Framework for the application layer, React/Webpack/Tailwind for interactive surfaces, PostgreSQL for durable state, Redis and Celery for asynchronous work, and ASGI/WebSockets for real-time communication.

The important boundary is custody: the product coordinates trading workflows without turning the platform into the owner of user assets.

## What I focused on

- Product boundaries between research, discovery, and execution
- Explicit wallet/account state and authorization scopes
- Trading workflows that can be paused and inspected
- Operational safeguards around asynchronous execution

The implementation repository is private; the live product is available at [talyxion.com](https://talyxion.com).
