# Service Provider Booking Platform

> Part of the [worlds-biggest-software-project](https://github.com/worlds-biggest-software-project) initiative.
>
> An AI-native, open-source platform that unifies service discovery, booking, payments, and reviews across verticals -- giving independent providers marketplace reach without commission lock-in.

Service Provider Booking Platform is a scheduling and discovery system for independent service providers, small businesses, and field service teams. It combines a consumer-facing marketplace (where clients discover, compare, and book providers) with a business management backend (calendar, payments, reminders, reviews). The core problem it solves: existing tools force providers to choose between marketplace reach with punishing commissions, or affordable scheduling tools with zero discovery.

---

## Why Service Provider Booking Platform?

- **Marketplace reach is locked behind commissions.** Fresha charges 20% on new-client bookings; Mindbody starts at $79/month with additional API fees. Providers who depend on marketplace discovery pay a growing tax on every customer relationship.
- **No single platform spans verticals.** Booksy targets beauty/wellness, Housecall Pro targets home services, Calendly targets meetings. A salon owner, a plumber, and a tutor cannot share a single discovery ecosystem today.
- **Scheduling tools lack discovery; marketplace tools lack openness.** Acuity and Calendly offer clean booking but no consumer marketplace. Booksy and Fresha offer discovery but no open API, no self-hosting, and no escape from proprietary lock-in.
- **Developer access is gated or absent.** Mindbody charges $11/month per location for API access capped at 2,000 requests/day. Acuity and Booksy offer no public API at all. ServiceTitan's API terms restrict competitive use.
- **AI capabilities are bolted on, not built in.** Incumbents are adding AI features (Fresha's AI receptionist, SimplyBook.me's voice booking) as paid add-ons rather than embedding intelligence into the scheduling and matching core.

---

## Key Features

### Booking and Scheduling

- Online booking page with real-time availability per provider and service type
- Calendar sync with Google Calendar, iCal, and CalDAV to prevent double-booking
- Client self-service rescheduling and cancellation
- Staff and provider schedule management with admin dashboard
- Group, class, and recurring appointment support

### Consumer Discovery Marketplace

- Cross-vertical marketplace with search, filter, and provider profile pages
- Provider ratings, reviews, and specialisation-based discovery
- Multi-language booking pages for international reach
- Website embed widget and social media booking buttons (Google, Facebook, Instagram)

### Payments and Revenue

- Payment collection at booking via Stripe (deposits and full payment)
- Dynamic pricing suggestions for off-peak slots to maximise revenue per available hour
- Loyalty programs with points or stamp card systems
- Transparent pricing model with no commission on bookings

### Communication and Retention

- Automated SMS and email reminders with configurable timing
- Two-way messaging inbox (SMS, email, WhatsApp) for client communication
- Post-appointment review request automation optimised per client channel and profile
- Marketing tools including promotions and blast messaging

### Field Service and Multi-Location

- Multi-location and multi-provider team management with centralised oversight
- Dispatch board with GPS tracking for field service providers
- Job pipeline from booking through to invoice
- Route optimisation and skill-based technician assignment

---

## AI-Native Advantage

Unlike incumbents that bolt AI onto existing workflows, this platform embeds intelligence at the core. Machine learning scores each client's no-show likelihood and automatically triggers deposit requests or targeted reminder sequences for high-risk appointments. Embedding-based provider-client matching surfaces the most compatible providers based on preferences, specialisations, and past ratings. AI analyses historical booking patterns to recommend optimal scheduling windows, reducing gaps between appointments and maximising utilisation. An AI receptionist handles after-hours bookings and FAQs, while natural-language voice booking replaces manual intake across phone and messaging channels.

---

## Tech Stack & Deployment

- **Standards:** iCalendar (RFC 5545) for booking confirmations and calendar sync; CalDAV for two-way calendar synchronisation; Schema.org LocalBusiness/Service markup for search engine discovery; PCI DSS compliance for payment processing
- **Integrations:** Stripe for payments; Google Calendar, Outlook, and iCloud for calendar sync; REST API and webhooks for custom integrations
- **Deployment:** Self-hosted option planned alongside managed cloud; open-source core with no per-seat licensing for self-hosted deployments
- **Compliance:** GDPR and CCPA support for client data handling and booking history

---

## Market Context

The global online appointment scheduling software market is valued at approximately USD 400 million in 2026, growing at over 13% CAGR through 2030, with the broader field service management market exceeding USD 6 billion. Incumbents span from free-with-commission models (Fresha) through $10-300/month professional tools to $100k+ enterprise contracts (ServiceTitan). Primary buyers are independent service providers (salons, tutors, cleaners, photographers), small business owners seeking discovery alongside scheduling, home service companies needing dispatch and routing, and wellness studios managing class bookings and memberships.

---

## Project Status

> This project is in the **research and specification phase**.  
> Contributions, feedback, and domain expertise are welcome.

---

## Contributing

We welcome contributions from developers, domain experts, and potential users.
See [CONTRIBUTING.md](CONTRIBUTING.md) for guidelines.

**Important:** All contributions must be your own original work or clearly attributed
open-source material with a compatible licence. Copyright infringement and licence
violations will not be tolerated and will result in immediate removal of the offending
contribution. If you are unsure whether a piece of code, text, or other material is
safe to contribute, open an issue and ask before submitting.

---

## Licence

Licence to be determined. See [discussion](#) for context.
