# SALESTORM_TEAM_NAME

## SALESTORM | SYSCRAFTERS 2026
### Design-First, AI-Assisted High-Scale Flash Sale Architecture

This package documents a flash-sale system handling **10,000 concurrent purchase requests for only 100 units**.

## Core guarantee
**Successful sales can never exceed available stock.**

## Architecture backbone
Customer → CDN/WAF → Load Balancer/API Gateway → Admission Control → Kafka (`product_id`) → Inventory/Reservation → SQL → Checkout/Payment → Transactional Outbox → Kafka → Order → Fulfilment → Shipment → Notification → Tracking.

## Critical scenario
- Stock = 100
- Concurrent users = 10,000
- Payment success = 95%
- Payment failure = 5%
- Duplicate requests = 2%
- Order Service unavailable = 30 seconds

## Folder guide
| Folder | Purpose |
|---|---|
| 01_Requirements | Scope, requirements, NFRs, assumptions |
| 02_HLD | System context, HLD architecture, deployment |
| 03_LLD | Inventory/payment components and critical sequences |
| 04_Database | ERD, schema, constraints |
| 05_API | REST and Kafka event flow |
| 06_SOLID | SOLID mapping |
| 07_Design_Patterns | Pattern mapping |
| 08_Scalability_Reliability | Concurrency and failure recovery |
| 09_Security_Observability | Security and telemetry |
| 10_ADR | Architecture decisions |
| 11_AI_Assisted_Validation | Simulation/validation material |
| 12_Presentation | Pitch/demo plan |

## Design principles
- SQL is the final inventory source of truth.
- Kafka partitions flash-sale work by `product_id`.
- Idempotency is enforced at reservation, payment and order transaction boundaries.
- Redis supports cache/rate limiting; it is not the final inventory authority.
- Transactional outbox prevents lost downstream events.
- Idempotent consumers and reconciliation handle retries and outages.

## Final judging message
**Traffic can scale. Inventory contention cannot be allowed to scale uncontrollably.**
