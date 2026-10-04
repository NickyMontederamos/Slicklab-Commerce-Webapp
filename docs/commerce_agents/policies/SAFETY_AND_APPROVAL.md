# Safety and Approval Policy

## Risk classes
- **R0 Read-only:** public catalog search, approved policy explanations, and read-only evidence retrieval
- **R1 Reversible:** drafts, recommendations, internal notes, test events, and queued reviews
- **R2 Controlled side effect:** catalog publication, customer notification, supplier reservation, and support-case updates
- **R3 Financial/contractual:** purchase, cancellation, refund, capture, void, substitution, and post-payment address change
- **R4 Prohibited:** unauthorized data use, credential sharing, platform-control bypass, unapproved scraping, and permission escalation

## Approval policy
- R0: automatic after authorization
- R1: automatic with audit log
- R2: policy gate and role permission; human review during MVP
- R3: blocking human approval, authoritative state, idempotency key, expected version, cost ceiling, expiry, and post-action verification
- R4: deny and record the reason

## Fail-safe rules
- Missing evidence means `HOLD`, not `PASS`.
- Conflicting evidence means `EXCEPTION`, not model-selected truth.
- Expired price or stock evidence must be refreshed.
- Approval expires when material facts change.
- Unknown side-effect result requires reconciliation before retry.
- A handoff never transfers permissions.
- A model recommendation never overrides a policy denial.
