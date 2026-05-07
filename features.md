# Service Provider Booking Platform — Feature & Functionality Survey

> Candidate #494 · Researched: 2026-05-07

## Solutions Analysed

| Tool | Type | Licence / Model | URL |
|------|------|-----------------|-----|
| Booksy Biz | Consumer marketplace + business tool | Commercial SaaS, from $29.99/mo | https://biz.booksy.com |
| Fresha | Consumer marketplace + business tool | Commercial SaaS, free core + commission | https://www.fresha.com |
| SimplyBook.me | Scheduling SaaS | Commercial SaaS, from $9.9/mo | https://simplybook.me |
| Mindbody | Fitness/wellness marketplace + business management | Commercial SaaS, from $79/mo | https://www.mindbodyonline.com |
| Acuity Scheduling | Appointment scheduling | Commercial SaaS, from $16/mo | https://acuityscheduling.com |
| Housecall Pro | Field service management | Commercial SaaS, from $49/mo | https://www.housecallpro.com |
| ServiceTitan | Enterprise field service platform | Enterprise SaaS, custom pricing | https://www.servicetitan.com |
| Calendly | Meeting/consultation scheduling | Commercial SaaS, from $10/user/mo | https://calendly.com |
| Cal.com / Cal.diy | Open-source scheduling infrastructure | AGPL-3.0 (Cal.com); MIT (Cal.diy) | https://cal.com / https://github.com/calcom/cal.diy |

---

## Feature Analysis by Solution

### Booksy Biz

**Core features**
- 24/7 online booking with real-time availability
- Integrated consumer marketplace for organic client discovery
- Appointment and staff calendar management
- Payment processing including deposits and no-show protection
- Automated SMS/email reminders and follow-ups
- Client profiles, history, and notes
- Retail product sales alongside services
- Marketing tools (promotions, blast messaging)

**Differentiating features**
- Built-in marketplace drives demand without external advertising
- AI-powered booking gap optimisation and marketing targeting (2026)
- Digital stamp card and loyalty points system

**UX patterns**
- Mobile-first apps for both business and consumer
- Onboarding wizard with vertical-specific templates (beauty, wellness)
- Dual interface: consumer discovery app and business management dashboard

**Integration points**
- Square payments
- Google and Facebook booking buttons
- Limited third-party integrations compared to competitors

**Known gaps**
- Primarily focused on beauty/wellness verticals; weak for other service types
- Limited customisation for booking page branding
- Less robust reporting than enterprise tools
- No open API for custom integrations

**Licence / IP notes**
- Proprietary SaaS; no self-hosted option

---

### Fresha

**Core features**
- Subscription-free core scheduling with commission on marketplace new-client bookings only
- Two-way messaging (SMS, email, WhatsApp in a single inbox)
- Multi-location business management
- Membership plans with flexible perks and discounts
- Package bundling (services + discounts + products)
- Payments including deposits and checkout
- Automated reminders and follow-ups
- Retail/product inventory management

**Differentiating features**
- Zero monthly fee model lowers adoption barrier significantly
- AI receptionist (2026): handles bookings and client FAQs outside hours
- 1-in-4 bookings now driven by Google Gemini and AI agents (2026 data)
- Google booking infrastructure: 30,000+ businesses, 1.2 million appointments/month via Google Search, Maps, and Gemini
- Enterprise multi-location support (2026 expansion)

**UX patterns**
- Consumer-first marketplace app with strong discovery
- Business-facing calendar and inbox in single dashboard
- Progressive feature disclosure; core is simple, advanced features accessible

**Integration points**
- Google Search, Google Maps, Google Gemini
- Facebook and Instagram booking
- Amazon Alexa voice booking
- Website embed widget

**Known gaps**
- Commission on new client bookings can erode margin at scale
- Less depth in field-service/dispatch workflows
- API access limited; not developer-friendly

**Licence / IP notes**
- Proprietary SaaS; no self-hosted option; commission model creates lock-in

---

### SimplyBook.me

**Core features**
- Multilingual booking pages (100+ languages)
- 60+ modular custom features (intake forms, deposits, packages, waitlists, etc.)
- Calendar sync with Google Calendar, Outlook, and other calendars
- Payment integration: Stripe, Square, PayPal
- Automated reminders (tailored timing and channel)
- Class and group bookings
- Staff/resource management
- Voice booking via AI assistant

**Differentiating features**
- Modular feature architecture allows pay-for-what-you-need configurability
- Strong multilingual and international reach
- Voice booking via AI assistant that understands natural language requests

**UX patterns**
- Feature marketplace approach: add modules as needed
- Admin dashboard with per-service and per-provider configuration
- White-label booking pages available

**Integration points**
- Facebook, Instagram, Google My Business
- WordPress and other CMS via embed
- QuickBooks, FreshBooks (native), Xero (export)
- Zapier (hundreds of downstream apps)
- REST API for custom integrations and enterprise deployments

**Known gaps**
- No built-in consumer discovery marketplace
- UI complexity increases significantly as modules are added
- Some integrations are workaround-based (e.g., Xero requires file export)

**Licence / IP notes**
- Proprietary SaaS; API access available but not open-source

---

### Mindbody

**Core features**
- Appointment and class scheduling
- Membership and package management
- Client app with discovery marketplace (Mindbody Explore)
- Payment processing and POS
- Staff payroll and performance reporting
- Virtual class streaming (on-demand and live)
- Automated marketing campaigns

**Differentiating features**
- Large consumer app user base drives marketplace discovery
- Hybrid virtual/in-person class management
- Branded consumer mobile apps for business accounts

**UX patterns**
- Business management console and separate consumer app
- Onboarding support for fitness/wellness studios
- Reporting dashboard with revenue and class attendance analytics

**Integration points**
- REST API (paid: $11/mo per location, up to 2,000 requests/day)
- Webhooks for booking events
- Zapier, Appy Pie, APIANT connector ecosystems
- Video conferencing integrations for virtual classes

**Known gaps**
- High pricing excludes small providers
- API access is paid and rate-limited, limiting developer adoption
- Complex onboarding for non-technical users
- Limited customisation for non-wellness verticals

**Licence / IP notes**
- Proprietary SaaS; API access is an additional paid tier

---

### Acuity Scheduling (Squarespace)

**Core features**
- Appointment scheduling with intake/intake forms
- Two-way calendar sync (Google, Outlook, iCloud, Exchange)
- Payment collection at booking via Stripe, Square, PayPal
- Up to 3 email reminders and 1 SMS reminder per appointment
- Group classes and workshop booking
- Client self-service rescheduling and cancellation
- Website embed (native Squarespace block)

**Differentiating features**
- Deep Squarespace website integration with no-code embed
- Clean, customisable client-facing booking pages
- Strong intake form and consent form support

**UX patterns**
- Simple setup wizard aimed at solo/small business operators
- Admin calendar view with drag-and-drop management
- Client portal for self-service changes

**Integration points**
- Squarespace websites (native block)
- Stripe, Square, PayPal
- Google, Outlook, iCloud Calendar (two-way sync)
- Zoom, GoTo Meeting for virtual sessions
- Zapier for extended automation

**Known gaps**
- No consumer discovery marketplace
- Frozen in Squarespace ecosystem; limited roadmap innovation
- iCloud new integrations discontinued August 2024
- Round-robin team scheduling unavailable; no advanced routing
- Weak reporting and analytics compared to enterprise alternatives
- No open API; developer access very limited

**Licence / IP notes**
- Proprietary SaaS; part of Squarespace; no self-hosted option

---

### Housecall Pro

**Core features**
- Job scheduling and booking (including customer self-booking from website/social)
- Drag-and-drop dispatch calendar with real-time updates
- GPS fleet tracking and route optimisation
- Automated SMS job confirmations and updates (98.2% delivery rate)
- On-site mobile payment processing and invoicing
- Customer communication hub (SMS, email)
- Job notes, photos, checklists, and work order management
- Reporting and revenue analytics

**Differentiating features**
- Dispatch optimisation: assigns technicians by skill, location, and availability
- GPS tracking and route management for field teams
- Automated post-job review request sequences
- Designed specifically for home services vertical (HVAC, plumbing, electrical, cleaning)

**UX patterns**
- Mobile-first for field technicians; desktop-first for dispatchers/owners
- Job pipeline view shows status from booking to invoice
- Customer-facing booking widget for website/social media embeds

**Integration points**
- QuickBooks, Xero (accounting)
- Stripe (payments)
- Google, Yelp, Facebook (reviews)
- Zapier for third-party automation
- Webhook support for custom integrations

**Known gaps**
- No consumer discovery marketplace
- Limited support for service verticals beyond home services
- Custom pricing rules and dynamic scheduling logic require manual setup
- Weak CRM compared to enterprise alternatives

**Licence / IP notes**
- Proprietary SaaS; no open API or self-hosted option

---

### ServiceTitan

**Core features**
- End-to-end job management: booking, dispatch, field execution, invoicing, payroll
- CRM: customer history, equipment records, service agreements
- Pricebook management with line items, bundles, and estimates
- Advanced dispatch board with skill-based routing
- Inventory and parts management
- Integrated payments and financing
- Marketing ROI tracking (connects ad spend to job revenue)
- Franchise and multi-location management

**Differentiating features**
- Full V2 API covering CRM, dispatch, inventory, payroll, pricebook, task management
- Marketing attribution linking call tracking to booked jobs
- Service agreement and recurring maintenance scheduling
- Designed for scale: hundreds of technicians, thousands of customers

**UX patterns**
- Complex, feature-rich admin interface aimed at operations managers
- Mobile app for field technicians
- Role-based access: CSR, dispatcher, technician, owner

**Integration points**
- Open V2 API (all core data entities)
- QuickBooks (accounting sync)
- Google Ads, Call Rail (marketing attribution)
- Zapier, custom webhooks
- Equipment finance partners

**Known gaps**
- Very high cost and complex onboarding; unsuitable for small/solo providers
- Booking flow involves manual CSR follow-up rather than instant confirmation
- Consumer discovery marketplace absent
- Steep learning curve for field technicians

**Licence / IP notes**
- Proprietary Enterprise SaaS; API available but terms restrict competitive use

---

### Calendly

**Core features**
- 1:1, round-robin, and collective meeting scheduling
- Multi-calendar conflict detection (Google, Outlook, Exchange, iCloud)
- Automated email and SMS reminders
- Payment collection via Stripe and PayPal
- Routing forms for lead qualification and smart meeting assignment
- Embed widget for websites and landing pages
- Video conferencing link generation (Zoom, Google Meet, Teams)
- Workflows for automated follow-up sequences

**Differentiating features**
- Clean, polished booking UX that dominates the meeting-scheduling category
- Routing forms with intelligent meeting distribution logic
- Large integration ecosystem (HubSpot, Salesforce, Marketo, Pardot)

**UX patterns**
- Guest-first: minimal friction for booker
- Admin calendar with event type configuration
- Progressive pricing tiers unlock enterprise features (Salesforce, round-robin, analytics)

**Integration points**
- 70+ native integrations (CRM, video, marketing automation, analytics)
- Scheduling API with webhook support
- Zapier and Make for long-tail automation
- Google Analytics, Meta Pixel for conversion tracking

**Known gaps**
- Free plan limited to one active event type; one calendar sync
- No consumer discovery marketplace
- Weak customisation of booking page appearance
- Advanced routing limited to higher plans; leaves logic gaps vs. CRM-native routing
- Not designed for multi-service businesses (salons, field service)
- iCloud new integrations discontinued August 2024
- Round-robin logic requires higher plan; Standard plan has no equitable distribution

**Licence / IP notes**
- Proprietary SaaS; API access gated to Standard plan and above

---

### Cal.com / Cal.diy

**Core features**
- 1:1, round-robin, collective, and group event scheduling
- Recurring events and booking automation workflows
- Routing forms for lead qualification
- Payment collection (Stripe, PayPal)
- 70+ integrations via app store
- SSO/SAML (Cal.com cloud, removed from Cal.diy)
- Team and organisation management
- Self-hosted deployment option

**Differentiating features**
- Fully open-source infrastructure (Cal.diy: MIT licence, relaunched April 2026)
- API-first architecture enables deep custom integrations and white-labelling
- No per-seat licensing for self-hosted deployments
- Cal.diy provides scheduling engine, app store framework, and booking infrastructure with no enterprise lock

**UX patterns**
- Developer-friendly: API-first, well-documented, easily embeddable
- Admin console for event type and team management
- Booking page themes and white-label support

**Integration points**
- REST API and webhooks
- 70+ app store integrations (video, CRM, payment, analytics)
- Self-hosted deployment via Docker or cloud providers (Railway, Vercel, etc.)

**Known gaps**
- Cal.diy strips out enterprise features (Teams, Orgs, Insights, Workflows, SSO)
- No consumer discovery marketplace
- Security vulnerabilities reported in 2026 (CVE-2026-23478, broken access controls in versions before 6.0.7)
- Cal.com SaaS now on a restrictive licence; community fragmentation risk

**Licence / IP notes**
- Cal.diy: MIT licence (self-hosted, individual use); Cal.com platform: AGPL-3.0 for earlier versions, proprietary for newer versions; enterprise features behind paid cloud

---

## Cross-Cutting Feature Themes

### Table-Stakes Features
- 24/7 online booking with real-time availability
- Automated reminders (email + SMS) before appointments
- Calendar sync (Google, Outlook) to prevent double-booking
- Payment collection at booking (deposits, full payment, or post-service)
- Mobile-responsive or native mobile booking experience
- Client self-service rescheduling and cancellation
- Staff/provider schedule and availability management
- Basic reporting (bookings, revenue, cancellations)

### Differentiating Features
- Consumer marketplace with organic discovery (Booksy, Fresha, Mindbody)
- AI-driven booking gap optimisation and no-show prediction
- Voice and AI agent bookings (Fresha AI receptionist; Google Gemini integration)
- Multi-location and franchise management with centralised oversight
- Dispatch optimisation and GPS fleet tracking (Housecall Pro, ServiceTitan)
- Marketing attribution linking ad spend to booked revenue (ServiceTitan)
- Loyalty programs and digital stamp cards (Booksy)
- Full open-source self-hosted deployment (Cal.diy)

### Underserved Areas / Opportunities
- Cross-vertical marketplace: no single platform supports beauty + home services + professional services + education/tutoring in one discovery layer
- AI-powered provider-client matching using embeddings and preference signals
- Dynamic/surge pricing for high-demand time slots
- No-show prediction with automated deposit enforcement triggered per-client risk score
- Post-appointment AI review generation optimised per communication channel and client profile
- Open-source, self-hosted platform combining marketplace discovery with full business management
- Transparent pricing with no commission model eating into provider revenue at scale
- Multi-language support combined with marketplace reach (SimplyBook.me has language reach but no marketplace)
- B2B service bookings (e.g., contractor booking for businesses) with approval workflows

### AI-Augmentation Candidates
- Availability slot recommendation based on historical booking patterns and gap analysis
- No-show and cancellation risk scoring per client → automated mitigation triggers
- Optimal reminder timing and channel selection per client behaviour profile
- Natural-language voice booking (phone and messaging channels) replacing manual intake
- Post-appointment review prompt timing optimisation
- Intelligent provider-client matching based on specialisations, past ratings, and preferences
- Dynamic pricing suggestions for off-peak slots to maximise revenue per available hour

---

## Legal & IP Summary

No patent concerns were identified among the open-source tools analysed. Cal.diy is MIT-licensed and safe for commercial use. Easy!Appointments (GPL-3.0) and similar GPL tools require derivative works to remain open source. The major commercial platforms (Booksy, Fresha, Mindbody, Acuity, Housecall Pro, ServiceTitan, Calendly) are proprietary SaaS products; replicating their feature sets is legally acceptable provided no source code, trademarks, or proprietary APIs are incorporated. ServiceTitan's API terms of service restrict competitive use — any integration with their API should be reviewed against their published developer terms. No copyright or licensing concerns prevent building an AI-native competitor that incorporates comparable capabilities.

---

## Recommended Feature Scope

**Must-have (MVP)**
- Online booking page with real-time availability per provider and service type
- Calendar sync (Google Calendar, iCal/CalDAV)
- Automated SMS and email reminders with configurable timing
- Payment collection at booking (deposits and full payment via Stripe)
- Client self-service rescheduling and cancellation
- Basic staff/provider schedule management and admin dashboard

**Should-have (v1.1)**
- Consumer discovery marketplace with search, filter, and profile pages
- AI-powered no-show risk scoring with automated deposit triggers
- Post-appointment review request automation optimised per client channel
- Multi-location and multi-provider team management
- Two-way messaging inbox (SMS, email, WhatsApp) for client communication
- Loyalty program (points or stamp card)

**Nice-to-have (backlog)**
- AI receptionist for after-hours bookings and FAQ handling
- Dynamic pricing suggestions for off-peak slots
- Embedding-based provider-client matching
- Voice booking via phone and messaging AI agents
- Open-source self-hosted deployment option
- Dispatch board with GPS tracking for field service providers
