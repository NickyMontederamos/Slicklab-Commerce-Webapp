# Commerce Event Contracts

## Required envelope
```json
{
  "event_id": "uuid",
  "event_type": "payment.confirmed",
  "event_version": 1,
  "occurred_at": "ISO-8601",
  "producer": "payment-service",
  "correlation_id": "uuid",
  "trace_id": "trace-id",
  "object_refs": {
    "order_id": "SC-...",
    "payment_id": "PAY-..."
  },
  "data": {},
  "evidence_refs": []
}
```

## Required properties
- globally unique event ID
- versioned schema
- idempotent consumer handling
- authoritative producer
- correlation and trace identifiers
- no raw secrets or full payment credentials
- minimal personal data

## Core events
- `order.created`
- `payment.authorized`
- `payment.confirmed`
- `payment.failed`
- `payment.refunded`
- `procurement.requested`
- `procurement.approved`
- `procurement.completed`
- `shipment.created`
- `shipment.updated`
- `shipment.delivered`
- `exception.created`
