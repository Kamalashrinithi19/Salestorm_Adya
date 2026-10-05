# ADR-005 — Transactional Outbox
Status: Accepted

Persist business state and its outgoing event record in the same transaction, then publish the outbox asynchronously. Consumers must be idempotent.
