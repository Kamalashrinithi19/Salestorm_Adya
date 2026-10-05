# Simulation Pseudocode

Generate 10,000 requests for 100 units, inject 2% duplicates, use 95% payment success, inject a 30-second Order Service outage, then assert:

- successful_sales <= 100
- inventory_available >= 0
- duplicate_business_transactions == 0
- payment/order mismatches == 0 after reconciliation
