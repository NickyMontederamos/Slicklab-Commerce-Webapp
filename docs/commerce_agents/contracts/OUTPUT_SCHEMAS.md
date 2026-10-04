# Agent Output Schemas

## OfferCandidateV1
```json
{
  "schema": "OfferCandidateV1",
  "recommendation": "LIST|MONITOR|REJECT",
  "product_id": "PROD-...",
  "variant_id": "VAR-...",
  "supplier_offer_id": "OFF-...",
  "floor_price": 1377,
  "target_price": 1499,
  "expected_margin": 0.219,
  "expected_profit": 329,
  "stock_confidence": "HIGH|MEDIUM|LOW",
  "supplier_risk": "LOW|MEDIUM|HIGH",
  "facts": [],
  "assumptions": [],
  "uncertainties": [],
  "evidence_refs": [],
  "evidence_expires_at": "ISO-8601"
}
```

## ProcurementRecommendationV1
```json
{
  "schema": "ProcurementRecommendationV1",
  "order_id": "SC-...",
  "decision": "APPROVE_CANDIDATE|HOLD|FIND_ALTERNATIVE",
  "maximum_total_cost": 1170,
  "expected_order_version": 7,
  "required_approval_class": "R3",
  "facts": [],
  "risks": [],
  "evidence_refs": [],
  "expires_at": "ISO-8601"
}
```

## ReconciliationFindingV1
```json
{
  "schema": "ReconciliationFindingV1",
  "order_id": "SC-...",
  "status": "MATCHED|EXCEPTION",
  "exception_type": null,
  "severity": "LOW|MEDIUM|HIGH|CRITICAL",
  "actual_profit": 200,
  "evidence_refs": [],
  "recommended_action": "NONE|REVIEW|REFUND_REVIEW"
}
```
