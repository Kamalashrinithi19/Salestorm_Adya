# API Specification

## POST /checkout/reserve
Creates a reservation. Requires Authorization and Idempotency-Key.

## POST /checkout/payment
Starts/confirms payment for a reservation using a stable idempotency key.

## GET /orders/{orderId}
Returns current order state.

## GET /payments/{paymentId}
Returns payment and reconciliation status.

## POST /reservations/{reservationId}/release
Releases an eligible reservation.

## Events
ReservationCreated, ReservationExpired, InventoryReleased, PaymentSucceeded, PaymentFailed, OrderCreated, OrderConfirmed, OrderCancelled.
