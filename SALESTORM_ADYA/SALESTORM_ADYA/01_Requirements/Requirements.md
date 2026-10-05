# System Requirements

## Functional
1. Product discovery and availability.
2. Cart management.
3. Admission and inventory reservation.
4. Atomic stock updates.
5. Reservation expiry/release.
6. Checkout and payment.
7. Payment idempotency.
8. Order lifecycle management.
9. Fulfilment, shipment, notification and tracking.
10. Duplicate-request protection.
11. Failure recovery and reconciliation.
12. Auditability.

## Critical invariants
- Inventory never becomes negative.
- Confirmed sales never exceed available stock.
- Duplicate requests do not create duplicate business transactions.
- Successful payment eventually reconciles to an order or compensation.
