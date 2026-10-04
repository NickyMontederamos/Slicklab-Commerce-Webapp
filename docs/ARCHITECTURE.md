# Public Architecture

SlickLab Commerce separates flexible AI-assisted judgment from authoritative commerce services.

- **Commerce core:** catalog, cart, order, inventory, payment state, fulfillment, returns.
- **PaymentProvider:** provider-independent payment abstraction.
- **Pricing and risk:** deterministic financial and policy controls.
- **Specialist intelligence:** market discovery, customer assistance, supervised procurement, and reconciliation.
- **Governance:** least privilege, human review for high-risk actions, auditable evidence, and explicit authority boundaries.

Detailed internal contracts, prompts, agent instructions, supplier adapters, scoring rules, and deployment runbooks are proprietary and intentionally excluded from the public repository.
