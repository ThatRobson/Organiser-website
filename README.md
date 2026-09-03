# Organiser

**Your life, organised.**

[organiserapp.co.uk](https://organiserapp.co.uk)

Organiser is an iOS and iPadOS personal life-management app built around a simple idea: everyday life shouldn't be scattered across half a dozen places.

It brings the things you need to remember, the things you need to do, and the money you need to plan for into one place.

## What Organiser does

### Home

Your life at a glance. Home pulls together upcoming dates, reminders, important events, recurring financial commitments, pay-period insights, calendar information and other useful feeds so you can see what needs your attention without hunting around the app.

**What's happening in my life?**

### Organiser

Keep track of the things you really don't want to forget:

- Birthdays and anniversaries
- Bills and subscriptions
- Vehicle MOT and tax renewals
- Insurance
- Appointments and travel
- Documents and taxes
- Home, family and pet events
- Work and civic events
- Custom dates

Dates can be one-off or recurring, with configurable reminders and staged notifications. Where useful, Organiser can turn a reminder into a next step — an approaching MOT, for example, can prompt you to get it booked.

**What do I need to remember or do?**

### Budget

Budget is about context, not replacing your banking app. Track salary and other income, recurring bills and outgoings, pay periods, spending categories, and paid or unpaid commitments to get a clearer picture of what you have left.

**What can I afford?**

### Profile

Make Organiser yours. Profile and Settings cover personal details, appearance, currency, notifications, calendar and contacts integrations, automatic calendars, privacy and security, data export/import, support and dashboard customisation.

## The idea

Modern life is fragmented. Birthdays can live in Contacts, appointments in Calendar, tasks in Reminders, and bills somewhere between your bank and your inbox.

Organiser connects those everyday commitments and makes them actionable.

The core flow is deliberately simple:

**Home → What's happening?**  
**Organiser → What's coming?**  
**Budget → What can I afford?**

Or, put another way:

> **Remember it. Prepare for it. Pay for it. Plan for it.**

## Product principles

- **One place** — less jumping between apps.
- **Action over information** — don't just show the date; help with what happens next.
- **Financial context** — connect recurring commitments with income and available money.
- **At-a-glance simplicity** — answer the important questions quickly.
- **Personalisation** — let people decide what matters most.
- **Privacy first** — keep personal life data local-first wherever possible.

## Platform and status

- iOS / iPadOS
- Currently in beta
- UK-focused, including £ currency, UK bank holidays, MOT and vehicle tax categories
- Local-first architecture, with iCloud sync infrastructure prepared for the future

## Technology

The app is built with Apple's native frameworks:

- **SwiftUI** for the interface
- **SwiftData** for on-device persistence
- **EventKit** for calendar integration
- **UserNotifications** for reminders
- **Contacts** for read-only birthday import
- **LocalAuthentication** for biometric app lock
- **AppIntents** for Siri and Shortcuts support

The architecture uses MVVM with a service layer for side effects such as calendar sync, notifications, contacts and biometrics. A shared `OrganiserStore` provides the SwiftData `ModelContainer` used by the UI and App Intents.

## Website

This repository contains the public Organiser website hosted with GitHub Pages at [organiserapp.co.uk](https://organiserapp.co.uk) (see `CNAME`).

- `index.html` — main landing page
- `privacy-policy.html` — privacy policy
- `privacy/` — legacy `/privacy` URL, redirects to `privacy-policy.html`
- `404.html` — custom not-found page
- `style.css` — shared site styling
- `favicon.svg`, `favicon.ico`, `assets/` — favicon, app icons and social share images
- `site.webmanifest` — web app manifest referencing the icons
- `robots.txt`, `sitemap.xml` — search engine crawling and indexing
- `llms.txt` — plain-language site summary for LLM crawlers

## Privacy

Organiser is designed around a local-first approach. The product brief describes on-device data storage and integrations with Apple services including Calendar, Contacts and notifications. The published Privacy Policy should be kept in step with the actual app implementation as the beta develops.

## Current state

Organiser is in beta and the initial market focus is the UK. The long-term direction is to make the app useful well beyond that starting point, without losing the simple, personal feel that makes it useful in the first place.
