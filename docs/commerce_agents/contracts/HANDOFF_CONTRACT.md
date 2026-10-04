# Agent Handoff Contract

Every handoff must be structured, minimal, scoped, and expiring.

```json
{
  "handoff_id": "uuid",
  "from_agent": "mark-bot",
  "to_agent": "proc-bot",
  "task_type": "find_alternative_offer",
  "object_refs": {
    "order_id": "SC-...",
    "product_id": "PROD-...",
    "variant_id": "VAR-..."
  },
  "facts": [],
  "assumptions": [],
  "evidence_refs": [],
  "constraints": [],
  "requested_output_schema": "AlternativeOfferV1",
  "authority": {
    "read": true,
    "write": false,
    "financial": false
  },
  "expires_at": "ISO-8601",
  "correlation_id": "uuid"
}
```

## Rules
- Pass object references instead of full customer records.
- Never transfer credentials or permissions through narrative text.
- The receiving agent performs an independent authorization check.
- Reject expired, malformed, over-broad, or unsupported handoffs.
- Record sender, receiver, result, duration, and error state.
