# Clio (clio)

<!-- API-EVANGELIST-PROVENANCE:BEGIN -->
> ### About this repository
>
> **This is not our API.** This repository is an independent, third-party profile of a company's
> **publicly available** API surface, maintained by [API Evangelist](https://apievangelist.com).
> API Evangelist does not operate, host, resell, or support this company's APIs, and is not
> affiliated with or endorsed by the company unless stated on the profile.
>
> **Where the information came from.** Everything here is assembled from material a member of the
> public can reach with a browser and no credentials — the company's own website, developer portal
> and documentation, the specifications it publishes for public use (OpenAPI, AsyncAPI, JSON Schema,
> `apis.json`, `llms.txt` and similar), its public repositories, and its public status, pricing and
> changelog pages. **Nothing here is obtained by breaching a system, defeating an access control, or
> using credentials of any kind.**
>
> **The rating is an independent assessment.** The Kin Score and Agent Readiness rating are
> independently calculated scores of a company's *public* API artifacts, produced by API Evangelist
> against a published rubric. They are not certifications, endorsements, security assessments, or
> audits, and they score published artifacts — not the quality, safety, or security of the software.
>
> **Corrections, re-scores, and removal are free.** No partnership, contract, or purchase is
> required, and you do not need to justify the request.
>
> - **Something wrong?** Open an issue on this repository, or email
>   [info@apievangelist.com](mailto:info@apievangelist.com).
> - **Published something new?** Ask for a re-score and we will re-run the rating.
> - **Want the listing taken down?** Say so and we will honor it. The profile is reduced to your
>   company name, a factual description, and a link to your own site, and the company is recorded as
>   **unrated** — never scored zero for having asked.
>
> **Response times.** Acknowledgement within **one business day**; removal or restriction within
> **two business days**; corrections and re-scores within **five business days**.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

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
