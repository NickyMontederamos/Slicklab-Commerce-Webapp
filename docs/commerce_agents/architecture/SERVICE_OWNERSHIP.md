# Service Ownership and Boundaries

## Medusa
Authoritative owner of catalog, cart, customer, order, inventory, payment-session, fulfillment, return, and refund state.

## Windmill
Operational jobs, schedules, approval interfaces, supplier synchronization, imports, reports, and remediation. It invokes application services and never writes commerce tables directly.

## TCC
Governance, policy coordination, permission boundaries, approval orchestration, and operational visibility.

## Hermes
Runs bounded agent tasks with scoped tools and isolated context.

## Payment Service
Normalizes Mock, Maya, Xendit, PayMongo, or future providers. Agents only see normalized payment facts.

## Pricing and Risk Services
Perform deterministic calculations and rule evaluation. Agent reasoning cannot override their results.

## Notification Service
Consumes commerce events and delivers approved templates through configured channels.

## OpenTelemetry
Correlates traces, metrics, and logs using order, payment, procurement, approval, supplier-order, and agent-run identifiers.

## Deferred components
- Typesense: add when catalog search requires typo tolerance and facets.
- Keycloak: add when multiple applications, roles, passkeys, or social identity justify it.
- OPA: add when policies span enough services to require centralized policy-as-code.
- Temporal: add when durable multi-day workflows and scale exceed Medusa + Windmill.
