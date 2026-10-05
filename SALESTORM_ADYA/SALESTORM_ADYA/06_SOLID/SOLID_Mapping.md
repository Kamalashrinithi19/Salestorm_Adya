# SOLID Mapping

| Principle | Application |
|---|---|
| SRP | Reservation, payment, order-state and reconciliation responsibilities are separated. |
| OCP | Payment strategies allow new providers without rewriting orchestration. |
| LSP | Gateway implementations conform to the payment abstraction. |
| ISP | Small repository/gateway interfaces avoid broad contracts. |
| DIP | Business services depend on abstractions; adapters implement infrastructure ports. |
