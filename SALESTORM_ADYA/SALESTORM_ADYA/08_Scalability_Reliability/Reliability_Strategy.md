# Scalability & Reliability

- Stateless service replicas scale horizontally.
- Admission control protects hot paths.
- Kafka partitions by product_id.
- Inventory uses atomic conditional SQL updates.
- Reservation expiry returns eligible stock.
- Payment calls use idempotency, timeout and circuit breaker protection.
- Transactional outbox closes the dual-write gap.
- Idempotent consumers prevent duplicate orders.
- Reconciliation resolves payment/order mismatches.
