# Standards & API Reference

> Project: Service Provider Booking Platform · Generated: 2026-05-07

## Industry Standards & Specifications

### ISO Standards

**ISO/IEC 40500:2025 (WCAG 2.2)**
- URL: https://www.iso.org/standard/40500.html
- WCAG 2.2 was ratified as an ISO/IEC standard in October 2025. Level AA conformance is now the globally mandated accessibility baseline for web applications. Booking platforms must meet this standard for keyboard navigation, focus visibility, accessible authentication (no cognitive CAPTCHA), target sizing, and form completion.

**ISO 20022 (Financial Services Universal Messaging)**
- URL: https://www.iso20022.org/
- The global standard for financial messaging between institutions. Relevant for any booking platform that integrates payment rails at scale (FedNow adopted ISO 20022 in July 2025; SWIFT migration ongoing). Direct relevance is limited unless the platform integrates bank transfer payments or financial institution APIs.

**ISO/IEC 27001 (Information Security Management)**
- URL: https://www.iso.org/standard/27001
- Internationally recognised framework for information security management systems. Relevant for hosting sensitive client PII (names, contact details, payment tokens) and for enterprise sales to businesses that require supplier security certification.

### W3C & IETF Standards

**RFC 5545 — iCalendar (Internet Calendaring and Scheduling Core Object Specification)**
- URL: https://datatracker.ietf.org/doc/html/rfc5545
- Defines the `.ics` data format for representing calendar events, to-dos, and free/busy information. Essential for booking confirmations, calendar exports, and cross-platform calendar compatibility. All major calendar apps (Google Calendar, Outlook, Apple Calendar) consume RFC 5545.

**RFC 4791 — CalDAV (Calendaring Extensions to WebDAV)**
- URL: https://datatracker.ietf.org/doc/html/rfc4791
- Defines the CalDAV protocol for bidirectional, server-to-server calendar synchronisation. Enables booking platforms to push and pull events to/from users' personal calendars in real time.

**RFC 6638 — CalDAV Scheduling Extensions**
- URL: https://datatracker.ietf.org/doc/html/rfc6638
- Extends CalDAV to support scheduling operations (invitations, acceptances, free/busy lookups) between calendar servers. Relevant for multi-party booking confirmation flows.

**RFC 5546 — iCalendar Transport-Independent Interoperability Protocol (iTIP)**
- URL: https://datatracker.ietf.org/doc/html/rfc5546
- Defines how calendar components (events, tasks) are exchanged between systems: REQUEST, REPLY, CANCEL methods. Used in email-based booking confirmation and cancellation workflows.

**RFC 7265 — jCal: The JSON Format for iCalendar**
- URL: https://datatracker.ietf.org/doc/html/rfc7265
- JSON representation of iCalendar data, suitable for REST API responses where JSON payloads are preferred over raw `.ics` text.

**RFC 6749 — OAuth 2.0 Authorization Framework**
- URL: https://datatracker.ietf.org/doc/html/rfc6749
- The standard authorisation protocol for delegated access to user resources. Required for calendar integrations (Google Calendar, Microsoft Outlook), social login, and third-party platform integrations.

**RFC 7591 — OAuth 2.0 Dynamic Client Registration**
- URL: https://datatracker.ietf.org/doc/html/rfc7591
- Protocol for dynamically registering OAuth clients at runtime without pre-registration. Used by Calendly's MCP server so AI agents self-register OAuth credentials on demand. Relevant for any AI-agent booking interface.

**Schema.org LocalBusiness / Service Markup**
- URL: https://schema.org/LocalBusiness
- W3C-community-developed structured data vocabulary. JSON-LD LocalBusiness and Service markup enables search engines, Google Maps, and AI agents to understand provider listings, services, and booking actions. Critical for organic marketplace discovery and AI-agent search integration. Mandatory for SEO in 2026.

### Data Model & API Specifications

**OpenAPI Specification 3.1 / 3.2**
- URL: https://spec.openapis.org/oas/v3.2.0.html
- The de facto standard for describing REST APIs in a machine-readable format. Enables auto-generated SDK clients, interactive documentation (Swagger UI), and request validation. REST + OpenAPI 3.x is the standard API architecture for public and partner-facing booking APIs in 2026.

**JSON Schema**
- URL: https://json-schema.org/
- Standard for validating structure and content of JSON payloads. Used in conjunction with OpenAPI for request/response validation and in webhook payload contracts.

**WebSockets / RFC 6455**
- URL: https://datatracker.ietf.org/doc/html/rfc6455
- Enables real-time, bidirectional communication between server and client. Relevant for live availability display (slot taken while user is selecting) and real-time dispatch board updates in field service booking.

### Security & Authentication Standards

**OAuth 2.0 (RFC 6749) & OpenID Connect (OIDC)**
- URL: https://openid.net/developers/specs/
- OIDC is the identity layer built on OAuth 2.0. Required for "Sign in with Google/Apple/Facebook" and for third-party calendar integrations. All major platform integrations (Google, Microsoft, Facebook) require OIDC-compliant authentication flows.

**PCI DSS 4.0.1 (Payment Card Industry Data Security Standard)**
- URL: https://www.pcisecuritystandards.org/standards/
- As of April 2025, all 64 updated requirements of PCI DSS 4.0.1 are mandatory for any platform collecting or transmitting cardholder data. Key requirements for booking platforms: script management and change detection on payment pages (Requirement 6.4.3), strong multi-factor authentication, and encryption of all transmitted cardholder data. Non-compliance fines range from $5,000 to $100,000/month. For most booking platforms, delegating payment processing to Stripe or Square (which are PCI-compliant) significantly reduces scope.

**GDPR (EU General Data Protection Regulation) / CCPA**
- URL: https://gdpr-info.eu/
- GDPR applies to any platform storing personal data of EU residents. Booking platforms collect identity data (name, email, phone), appointment history, and potentially health-sensitive information. Key obligations: lawful basis for data processing, right to erasure, data portability in interoperable formats (CSV, JSON, ICS), pseudonymisation/encryption at rest, and strict data processor contracts with sub-processors. Fines up to €20 million or 4% of global turnover for serious violations. CCPA applies for California residents.

**OWASP Top 10 (Web Application Security)**
- URL: https://owasp.org/www-project-top-ten/
- The authoritative reference for web application security risks. Booking platforms must address injection attacks, broken authentication, insecure direct object references (booking IDs), security misconfiguration, and cross-site scripting (XSS) in embedded booking widgets.

### MCP Server Specifications

**Model Context Protocol (MCP) — Anthropic / Open Standard**
- URL: https://modelcontextprotocol.io/specification/2025-11-25
- MCP is the open protocol (97 million monthly SDK downloads as of March 2026, 81,000+ GitHub stars) that enables AI agents and LLMs to connect to external tools and data sources. A booking platform MCP server allows AI assistants to discover available slots, create bookings, cancel appointments, and query provider profiles using natural language commands. Calendly has already shipped an MCP server; Cal.com supports MCP via its API-first architecture. Building an MCP server is now a standard expectation for developer-facing scheduling platforms.

---

## Similar Products — Developer Documentation & APIs

### Calendly

- **Description:** Leading meeting-scheduling SaaS. Strong developer ecosystem with REST API, webhooks, and a hosted MCP server for AI-agent integration.
- **API Documentation:** https://developer.calendly.com/
- **SDKs/Libraries:** No official SDK; community SDKs available for JavaScript/TypeScript and Python via API tracker ecosystem
- **Developer Guide:** https://developer.calendly.com/getting-started
- **Standards:** REST/JSON, OpenAPI-described endpoints, OAuth 2.0, RFC 7591 Dynamic Client Registration (MCP), Webhooks
- **Authentication:** OAuth 2.0 (personal access tokens for development; OAuth apps for production)
- **Notes:** MCP server hosted at https://mcp.calendly.com; uses Dynamic Client Registration so AI agents self-register. Webhooks (invitee.created, invitee.canceled, routing_form_submission.created) require paid plan.

### Cal.com

- **Description:** Open-source scheduling infrastructure (Cal.diy: MIT licence; Cal.com cloud: AGPL / commercial). API-first, self-hostable, 70+ integrations.
- **API Documentation:** https://cal.com/docs/api-reference/v2/introduction
- **SDKs/Libraries:** JavaScript/TypeScript SDK; Python community client; REST API with OpenAPI spec
- **Developer Guide:** https://cal.com/docs
- **Standards:** REST/JSON, OpenAPI 3.x, Webhooks, OAuth 2.0, GraphQL playground
- **Authentication:** API key (development); OAuth 2.0 apps (production)
- **Notes:** Base URL `https://api.cal.com/v2`; rate limit 120 requests/minute. Self-hosted deployment supported via Docker. Webhook events cover booking created, rescheduled, cancelled. CVE-2026-23478 patched in v6.0.7.

### Mindbody

- **Description:** Fitness, wellness, and beauty SaaS with consumer marketplace and REST API for booking, client management, and class scheduling.
- **API Documentation:** https://developers.mindbodyonline.com/ui/documentation/public-api
- **SDKs/Libraries:** No official SDK; REST API with Swagger documentation
- **Developer Guide:** https://developers.mindbodyonline.com/
- **Standards:** REST/JSON, OpenAPI (Swagger), Webhooks
- **Authentication:** API Key + Site ID (per location); paid API access at $11/month/location (2,000 requests/day/location)
- **Notes:** Webhooks available for class booking events, add-on bookings. Affiliate API for marketplace discovery. Paid and rate-limited model limits developer adoption.

### ServiceTitan

- **Description:** Enterprise field service management platform with comprehensive V2 API covering CRM, dispatch, inventory, payroll, and pricebook.
- **API Documentation:** https://developer.servicetitan.io/docs/api-resources-crm/
- **SDKs/Libraries:** No official SDK; REST API
- **Developer Guide:** https://developer.servicetitan.io/
- **Standards:** REST/JSON, OAuth 2.0
- **Authentication:** OAuth 2.0 (client credentials flow for server-to-server)
- **Notes:** API covers: CRM (customers, leads, bookings), Job Planning (jobs, appointments), Pricebook, Payroll, Inventory, Task Management. Terms of service restrict competitive use of the API.

### Stripe (Payment Processing)

- **Description:** The de facto payment infrastructure for booking platforms. Covers card payments, ACH, deposits, refunds, subscriptions, and terminal payments.
- **API Documentation:** https://docs.stripe.com/api
- **SDKs/Libraries:** Official SDKs for JavaScript, Python, Ruby, PHP, Go, Java, .NET, iOS, Android — https://docs.stripe.com/development
- **Developer Guide:** https://docs.stripe.com/get-started
- **Standards:** REST/JSON, OpenAPI-described, PCI DSS compliant (reduces merchant scope)
- **Authentication:** API Key (publishable for client; secret for server); OAuth for Connect platform accounts
- **Notes:** Stripe Connect enables marketplace-style payment routing (provider receives funds minus platform fee). PaymentIntents API manages deposit-at-booking and post-service capture flows. Radar provides fraud detection. Stripe is the most commonly integrated payment provider across all analysed booking platforms.

### SimplyBook.me

- **Description:** Multilingual appointment booking SaaS with modular features and a public REST API for enterprise custom integrations.
- **API Documentation:** https://help.simplybook.me/index.php/User_API_guide
- **SDKs/Libraries:** PHP and JavaScript client examples in documentation; Zapier integration for no-code connectivity
- **Developer Guide:** https://help.simplybook.me/index.php/User_API_guide
- **Standards:** REST/JSON, JSON-RPC, Zapier triggers
- **Authentication:** API Token (per account)
- **Notes:** JSON-RPC interface alongside REST. Supports Google My Business, Facebook, Instagram booking integrations natively. Webhook support limited; Zapier fills the automation gap.

### Housecall Pro

- **Description:** Field service management SaaS (home services: HVAC, plumbing, cleaning). API available for custom integrations; webhook support for job events.
- **API Documentation:** https://docs.housecallpro.com/ (partner integrations)
- **SDKs/Libraries:** No official SDK
- **Developer Guide:** Contact via partner programme
- **Standards:** REST/JSON, Webhooks
- **Authentication:** OAuth 2.0 (partner applications)
- **Notes:** Integration ecosystem includes QuickBooks, Stripe, Xero, Google, Yelp. GPS tracking and dispatch optimisation APIs not publicly documented. Partner programme required for API access.

### Google Calendar API

- **Description:** Google's calendar data API enabling read/write access to user calendars for availability checking, event creation, and two-way sync.
- **API Documentation:** https://developers.google.com/calendar/api/v3/reference
- **SDKs/Libraries:** Official clients for JavaScript, Python, Java, Go, .NET, Ruby, PHP
- **Developer Guide:** https://developers.google.com/calendar/api/quickstart
- **Standards:** REST/JSON, OAuth 2.0, CalDAV (legacy), iCalendar (event format)
- **Authentication:** OAuth 2.0 with Google Identity (OpenID Connect)
- **Notes:** Required for Google Calendar two-way sync. Also supports free/busy queries without full event access (minimal OAuth scope). Google Gemini AI booking integration (used by Fresha) routes through Google's Booking API, not the Calendar API directly.

---

## Notes

**Emerging areas to monitor:**
- **MCP for booking:** Calendly's hosted MCP server (using RFC 7591 Dynamic Client Registration) sets a new bar. A new AI-native booking platform should plan an MCP server from day one to be accessible to AI agents across all major LLM platforms.
- **AI-agent booking via Google Gemini:** Fresha reports 1-in-4 bookings driven by Google Gemini and AI agents as of 2026. Schema.org `ReservationAction` and `MakeAction` markup in service listings enables this pathway without custom integrations.
- **WCAG 2.2 as ISO standard:** Since October 2025, WCAG 2.2 Level AA is an ISO/IEC standard. US DOJ mandated WCAG 2.1 AA compliance by April 2026 for state/local government digital services; private sector enforcement is accelerating through ADA litigation.
- **PCI DSS 4.0.1 enforcement:** All assessments from 2026 onward must be against v4.0.1. The safest path for booking platforms is to use Stripe, Square, or Adyen as payment processors and minimise cardholder data environment scope.
- **CalDAV vs Google/Microsoft OAuth:** Two-way calendar sync via Google and Microsoft OAuth (using their proprietary calendar APIs) provides better user experience and adoption than raw CalDAV, though CalDAV remains important for enterprise deployments and self-hosted calendar servers.
