# Tool Contract Standards

## Every tool requires
- exact purpose and explicit non-purpose
- typed input and output schema
- authentication and role requirements
- object scope
- risk and side-effect classification
- idempotency behavior
- expected-version support
- timeout and retry policy
- freshness requirements
- privacy classification
- audit events
- examples for success, validation failure, authorization failure, partial success, timeout, and unknown result

## Naming
Use narrow verb-object names:
- `catalog_search_products`
- `supplier_get_offer`
- `pricing_calculate_quote`
- `orders_get_authorized_order`
- `procurement_prepare_request`
- `approvals_request_decision`
- `shipments_get_status`

Avoid vague names such as `manage_order`, `do_purchase`, or `use_marketplace`.

## Side-effect requirements
Purchase, refund, cancellation, capture, void, address change, publication, and outbound-message tools must expose when relevant:
- `dry_run`
- `idempotency_key`
- `expected_version`
- `approval_id`
- `maximum_cost`
- `evidence_expires_at`

## Output discipline
Tools return normalized facts and machine-readable error codes. Agents do not parse screenshots or free-form success messages as authoritative state.
