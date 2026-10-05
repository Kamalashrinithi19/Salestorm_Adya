# Assumptions

1. SQL is the final inventory source of truth.
2. Kafka is used for burst buffering and asynchronous event propagation.
3. `product_id` is the Kafka partition key for flash-sale processing.
4. Redis is supporting infrastructure, not the final inventory authority.
5. Payment provider/adapters support idempotent processing.
6. Order consumers are idempotent.
7. Reservation expiry is handled by a reliable worker.
8. Logical architecture is cloud-neutral; deployment maps it to AWS/EKS.
