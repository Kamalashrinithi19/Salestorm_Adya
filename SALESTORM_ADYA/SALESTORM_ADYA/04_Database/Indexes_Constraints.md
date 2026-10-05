# Indexes & Constraints

Recommended indexes: INVENTORY(product_id); RESERVATION(idempotency_key, product_id); RESERVATION(status, expires_at); PAYMENT(idempotency_key); PAYMENT(provider_reference); ORDER(idempotency_key); OUTBOX_EVENT(status, created_at).

Inventory writes must be conditional on sufficient available quantity.
