# Clio (clio)

Clio is a cloud-based legal practice management platform used by law firms for matter management, contacts, calendaring, time and billing, trust accounting, document management, tasks, and client communications. The Clio Manage API is a REST/JSON API at app.clio.com/api/v4 that uses OAuth 2.0 (authorization code flow) for authentication and exposes the full data model behind Clio Manage, with regional endpoints for the U.S., Canada, EU/UK, and Australia. Webhooks deliver near real-time event notifications, and the Clio App Directory hosts certified third-party integrations.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/clio/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/clio/refs/heads/main/apis.yml)

## Scope

- **Type:** Index

## Tags

- Billing
- Calendaring
- Document Management
- Law Firms
- Legal
- Matter Management
- OAuth 2.0
- Practice Management
- Time Tracking
- Trust Accounting

## Timestamps

- **Created:** 2026-05-11
- **Modified:** 2026-05-11

## APIs

### Clio Manage API v4

The Clio Manage API v4 is a JSON REST API that gives developers programmatic access to Clio's legal practice management data model — matters, contacts, activities, bills, trust accounts, documents, tasks, calendar entries, custom fields, and users. Authentication is OAuth 2.0 (authorization code flow). Regional endpoints exist for the U.S. (app.clio.com), Canada (ca.app.clio.com), EU/UK (eu.app.clio.com), and Australia (au.app.clio.com). Standard pagination, filtering, sparse fieldsets, and ETag-based caching are supported.

- **Human URL:** [https://docs.developers.clio.com/](https://docs.developers.clio.com/)
- **Base URL:** `https://app.clio.com/api/v4`

#### Tags

- Legal
- Matter Management
- OAuth 2.0
- Practice Management
- REST

#### Properties

- [Documentation](https://docs.developers.clio.com/)
- [Reference](https://docs.developers.clio.com/api-docs/)
- [Authentication](https://app.clio.com/oauth/authorize)
- [OpenAPI](openapi/clio-manage-api-v4-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)

### Clio Webhooks

Clio Webhooks deliver near real-time notifications when matters, contacts, activities, tasks, calendar entries, bills, and other Clio resources are created, updated, or deleted. Subscriptions are managed through the Webhooks endpoints in the Manage API and payloads are delivered to the integrator's HTTPS endpoint with an X-API-V4-Signature header for verification.

- **Human URL:** [https://docs.developers.clio.com/api-docs/webhooks/](https://docs.developers.clio.com/api-docs/webhooks/)

#### Tags

- Events
- Legal
- Notifications
- Webhooks

#### Properties

- [Documentation](https://docs.developers.clio.com/api-docs/webhooks/)
- [AsyncAPI](asyncapi/clio-webhooks-asyncapi.yml) — [AsyncAPI Specification](https://www.asyncapi.com/docs/reference/specification/latest)
- [Postman Collection](collections/clio.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/clio.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Clio App Directory

The Clio App Directory is the integration marketplace for certified third-party apps that connect to Clio Manage. Apps listed in the directory are reviewed by Clio's developer partnerships team and made discoverable to Clio's customer base.

- **Human URL:** [https://app.clio.com/companion](https://app.clio.com/companion)

#### Tags

- Integrations
- Marketplace
- Partners

#### Properties

- [Marketplace](https://app.clio.com/companion)
- [Listing  Guide](https://docs.developers.clio.com/getting-started/listing-your-app/)
- [Postman Collection](collections/clio.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/clio.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

## Common Properties

- [LinkedIn](https://www.linkedin.com/company/clio---cloud-based-legal-technology)
- [Website](https://www.clio.com/)
- [Documentation](https://docs.developers.clio.com/)
- [Pricing](https://www.clio.com/pricing/)
- [Sign Up](https://app.clio.com/sign-up)
- [Portal](https://docs.developers.clio.com/)
- [Reference](https://docs.developers.clio.com/api-docs/)
- [Authentication](https://docs.developers.clio.com/api-docs/authorization/)
- [Login](https://app.clio.com/login)
- [Support](https://support.clio.com/)
- [Status Page](https://status.clio.com/)
- [Blog](https://www.clio.com/blog/)
- [Privacy Policy](https://www.clio.com/privacy/)
- [Terms of Service](https://www.clio.com/terms/)
- [App  Directory](https://app.clio.com/companion)
- [Git Hub](https://github.com/clio)
- [JSON-LD](json-ld/clio-context.jsonld) — [JSON-LD](https://www.w3.org/TR/json-ld11/)
- [Spectral Rules](rules/clio-rules.yml) — [Spectral](https://docs.stoplight.io/docs/spectral)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
