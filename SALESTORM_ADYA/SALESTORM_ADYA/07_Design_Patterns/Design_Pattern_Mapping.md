# Design Pattern Mapping

| Pattern | Where | Why |
|---|---|---|
| Strategy | Payment providers | Swap provider behavior. |
| Factory | PaymentFactory | Select provider strategy. |
| Adapter | StripeAdapter | Normalize provider-specific APIs. |
| State | OrderStateMachine | Control valid lifecycle transitions. |
| Repository | Inventory/Payment/Order | Isolate persistence. |
| Observer/Event Publisher | Kafka | Decouple downstream services. |
| Facade | Checkout orchestration | Simplify reservation/payment flow. |
| Circuit Breaker | Payment gateway | Prevent cascading failures. |
