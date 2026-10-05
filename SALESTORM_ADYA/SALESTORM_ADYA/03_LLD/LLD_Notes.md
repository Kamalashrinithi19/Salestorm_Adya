# LLD Notes

## Inventory
InventoryService → StockValidator → ReservationManager → InventoryRepository → SQL.
Use an atomic conditional update such as: `UPDATE inventory SET available = available - 1 WHERE product_id = ? AND available > 0`.

## Payment
PaymentService → PaymentFactory → PaymentStrategy → Provider Adapter → Gateway Client. Protect calls with idempotency and a circuit breaker.

## Order
OrderService → OrderStateMachine → OrderRepository + Idempotent Event Consumer + Outbox Publisher.

## Critical states
AVAILABLE → RESERVED → PAYMENT_PENDING → CONFIRMED → SOLD
Failure/expiry: RESERVED or PAYMENT_PENDING → RELEASED
