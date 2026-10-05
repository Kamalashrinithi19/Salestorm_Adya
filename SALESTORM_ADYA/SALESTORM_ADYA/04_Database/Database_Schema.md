# Database Schema

Core entities: CUSTOMER, PRODUCT, INVENTORY, CART, CART_ITEM, RESERVATION, ORDER, ORDER_ITEM, PAYMENT, SHIPMENT, OUTBOX_EVENT, IDEMPOTENCY_RECORD, AUDIT_LOG.

Critical uniqueness: inventory.product_id, reservation idempotency key, payment idempotency key, payment provider reference, order idempotency key.
