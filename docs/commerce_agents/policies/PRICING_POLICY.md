# Pricing Policy V1

## Initial thresholds
- Default target gross margin: 22%
- Minimum gross margin: 15%
- Minimum expected contribution profit: PHP 150
- High-risk target margin: 30%

These are configurable starting controls, not permanent market claims. REC-BOT reconciliation data must be used to adjust them after sufficient completed orders.

## Definitions
```text
risk_adjusted_cost = supplier_price
                   + supplier_shipping
                   + expected_payment_cost
                   + operating_allowance
                   + return_and_cancellation_reserve
                   + risk_buffer

floor_price = risk_adjusted_cost / (1 - minimum_margin)
target_price = risk_adjusted_cost / (1 - target_margin)
```

## Listing rules
- `LIST`: margin at or above target, profit at or above minimum, evidence fresh, market supports price, risk acceptable
- `REVIEW`: margin at or above minimum but below target
- `REJECT`: margin below minimum, profit below minimum, or market ceiling below safe floor

## Controls
- Models never calculate authoritative price or profit.
- Payment cost must use the selected provider/method schedule or a conservative allowance.
- Taxes and regulatory obligations must be configured by qualified business/accounting guidance.
- Promotions must not reduce price below the approved floor without a distinct authorization.
