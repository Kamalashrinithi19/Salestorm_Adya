# ADR-001 — Inventory Concurrency Control
Status: Accepted

Use SQL as the final inventory source of truth with atomic conditional updates. Admission control and Kafka partitioning reduce uncontrolled contention before the database.
