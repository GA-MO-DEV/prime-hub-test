---
feature: checkout
version: 1
status: approved
---

# Spec: checkout (fake)

## AC

### AC-01 VAT on the total
- priority: must
- money: yes
- hash: "218d3353"

Given a cart of 100.00 THB
When the customer checks out
Then the total is 107.00 THB including VAT

### AC-02 Coupon before VAT
- priority: must
- money: yes
- hash: "544e6607"

Given a coupon SAVE10 on a cart of 100.00 THB
When the coupon is applied
Then the total is 96.30 THB including VAT
