# Clio GraphQL Schema

## Overview

This document describes a conceptual GraphQL schema for the Clio Manage API v4. Clio is a cloud-based legal practice management platform used by law firms for matter management, contacts, calendaring, time and billing, trust accounting, document management, tasks, and client communications.

The Clio Manage REST API is available at `https://app.clio.com/api/v4` with regional variants for Canada (`ca.app.clio.com`), EU/UK (`eu.app.clio.com`), and Australia (`au.app.clio.com`). This GraphQL schema represents the same underlying data model expressed as a typed graph.

- **Source API**: Clio Manage API v4 (REST/JSON)
- **Authentication**: OAuth 2.0 Authorization Code Flow
- **Reference**: https://docs.developers.clio.com/api-docs/
- **Schema file**: clio-schema.graphql

## Domain Model

### Matter Management

The core entity in Clio is the `Matter`, representing a legal case or client engagement. Matters are associated with clients (via `Contact`), assigned to `User` records, categorized by `PracticeArea`, and tracked through configurable `MatterStatus` stages.

Related types: `Matter`, `MatterPracticeArea`, `MatterStatus`, `OriginalMatter`, `RelatedMatter`, `ConflictCheck`

### Contacts and Relationships

`Contact` records represent people and companies that interact with the firm — clients, opposing parties, witnesses, experts, and so on. Each contact has a `ContactType`, one or more `Address` records, and optional `Relationship` links to other contacts.

Related types: `Contact`, `ContactType`, `Address`, `Relationship`, `ClioConnect`, `ClientPortal`

### Firm and Users

`Firm` holds the organizational account. `User` records map to individual attorneys, paralegals, and staff, each with a `UserProfile` and access permissions. `Practice` groups define team or department-level organization.

Related types: `Firm`, `User`, `UserProfile`, `Practice`, `PracticeArea`

### Calendar and Tasks

`CalendarEntry` and `CalendarEvent` track court dates, appointments, and deadlines on the matter calendar. `Task` items with configurable `TaskStatus` track work items, and `Reminder` records provide deadline alerts.

Related types: `CalendarEntry`, `CalendarEvent`, `Task`, `TaskStatus`, `Reminder`

### Documents

`Document` records store files attached to matters or contacts, organized into `DocumentFolder` hierarchies and categorized via `DocumentCategory`. `DocumentVersion` tracks the revision history of each document. `WebLink` records store external URLs.

Related types: `Document`, `DocumentFolder`, `DocumentCategory`, `DocumentVersion`, `WebLink`

### Communications

`Communication` is the base type for all firm communications. Subtypes include `EmailMessage` (with `InboundEmail` and `OutboundEmail` variants), `PhoneCall`, and `PhoneLog` records.

Related types: `Communication`, `EmailMessage`, `InboundEmail`, `OutboundEmail`, `PhoneCall`, `PhoneLog`

### Time and Billing

`TimeEntry` and `TimerEntry` capture billable and non-billable time against matters, described by `ActivityDescription`. Fees and expenses are tracked as `Fee` and `Expense` (including unbilled variants), then assembled into `Bill` records (rendered as `Invoice`) with `InvoiceLineItem` detail, `Discount`, `TaxRate`, and potential `WriteOff` or `Adjustment` records.

Related types: `TimerEntry`, `TimeEntry`, `ActivityDescription`, `Fee`, `Expense`, `UnbilledFee`, `UnbilledExpense`, `Bill`, `Invoice`, `InvoiceLineItem`, `Discount`, `TaxRate`, `WriteOff`, `Adjustment`

### Payments and Credits

`Payment` records record received funds. `Credit` tracks credits applied against balances.

Related types: `Payment`, `Credit`

### Accounts and Trust Accounting

Clio provides full trust accounting. `Account` is the base type, with `BankAccount` and `TrustAccount` specializations. Transactions are split into `BankTransaction` and `TrustTransaction`. Balances are tracked via `Balance` and `TrustBalance`.

Related types: `Account`, `BankAccount`, `TrustAccount`, `BankTransaction`, `TrustTransaction`, `Balance`, `TrustBalance`

### Notes, Tags, and Custom Fields

`Note` records attach free-text annotations to matters and contacts. `Tag` records provide ad-hoc labeling. `CustomField` defines firm-level metadata fields; `CustomFieldValue` stores the per-record values.

Related types: `Note`, `Tag`, `CustomField`, `CustomFieldValue`

### Grants and Reports

`Grant` tracks funding grants (used in legal aid firms). `Report` represents generated reports within Clio.

Related types: `Grant`, `Report`

### Integrations

`Webhook` subscriptions deliver real-time event notifications. `ESignature` tracks electronic signature requests for documents.

Related types: `Webhook`, `ESignature`

## Type Summary

| Category | Types |
|---|---|
| Matter | Matter, MatterPracticeArea, MatterStatus, OriginalMatter, RelatedMatter, ConflictCheck |
| Contacts | Contact, ContactType, Address, Relationship, ClioConnect, ClientPortal |
| Firm & Users | Firm, User, UserProfile, Practice, PracticeArea |
| Calendar & Tasks | CalendarEntry, CalendarEvent, Task, TaskStatus, Reminder |
| Documents | Document, DocumentFolder, DocumentCategory, DocumentVersion, WebLink |
| Communications | Communication, EmailMessage, InboundEmail, OutboundEmail, PhoneCall, PhoneLog |
| Time & Billing | TimerEntry, TimeEntry, ActivityDescription, Fee, Expense, UnbilledFee, UnbilledExpense, Bill, Invoice, InvoiceLineItem, Discount, TaxRate, WriteOff, Adjustment |
| Payments | Payment, Credit |
| Accounts | Account, BankAccount, TrustAccount, BankTransaction, TrustTransaction, Balance, TrustBalance |
| Annotations | Note, Tag, CustomField, CustomFieldValue |
| Other | Grant, Report, Webhook, ESignature |

Total named types: 71

## Query Entry Points

- `matter(id: ID!)` / `matters(filter: MatterFilter, page: Int, perPage: Int)` — retrieve one or many matters
- `contact(id: ID!)` / `contacts(filter: ContactFilter, ...)` — retrieve contacts
- `user(id: ID!)` / `users(...)` — firm users
- `document(id: ID!)` / `documents(...)` — documents and folders
- `timeEntry(id: ID!)` / `timeEntries(...)` — time entries
- `bill(id: ID!)` / `bills(...)` — bills and invoices
- `calendarEntry(id: ID!)` / `calendarEntries(...)` — calendar events
- `task(id: ID!)` / `tasks(...)` — tasks and reminders
- `trustAccount(id: ID!)` / `trustAccounts(...)` — trust accounts and balances
- `note(id: ID!)` / `notes(...)` — notes
- `webhook(id: ID!)` / `webhooks(...)` — webhook subscriptions
- `report(id: ID!)` / `reports(...)` — reports
- `me` — the authenticated user

## Mutation Entry Points

- `createMatter` / `updateMatter` / `deleteMatter`
- `createContact` / `updateContact` / `deleteContact`
- `createTimeEntry` / `updateTimeEntry` / `deleteTimeEntry`
- `createTask` / `updateTask` / `deleteTask`
- `createNote` / `updateNote` / `deleteNote`
- `createDocument` / `updateDocument` / `deleteDocument`
- `createCalendarEntry` / `updateCalendarEntry` / `deleteCalendarEntry`
- `createBill` / `updateBill` / `deleteBill`
- `createPayment` / `updatePayment` / `deletePayment`
- `createWebhook` / `updateWebhook` / `deleteWebhook`

## References

- Clio Developer Docs: https://docs.developers.clio.com/
- API Reference: https://docs.developers.clio.com/api-docs/
- OAuth 2.0 Authorization: https://docs.developers.clio.com/api-docs/authorization/
- Webhooks: https://docs.developers.clio.com/api-docs/webhooks/
- GitHub: https://github.com/clio
