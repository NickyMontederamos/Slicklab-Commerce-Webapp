# Human Review Runbook

## Procurement approval checklist
- Correct customer order and exact variant
- Payment verified by authoritative backend event
- Supplier permitted and active
- Price, stock, shipping, and delivery checked recently
- Expected profit and margin above policy thresholds
- Customer shipping data valid and handled lawfully
- No unresolved fraud, authenticity, content-rights, or platform-policy flag
- Request includes evidence, cost ceiling, expected order version, and expiry

## Decision options
- **Approve:** issue a time-limited approval bound to the current facts.
- **Find alternative:** return to MARK-BOT with explicit constraints.
- **Hold:** preserve the order and create an exception.
- **Reject/refund review:** follow the separate refund policy and approval process.

## Approval record
Capture:
- approver identity and role
- decision
- reason
- timestamp
- facts and evidence hash
- expiry
- maximum approved cost

## After execution
Confirm supplier order reference, final cost, delivery estimate, audit event, and customer notification event. If any are missing, create an exception immediately.
