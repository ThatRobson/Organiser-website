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

There's no build step — it's plain HTML/CSS, deployed as-is. That means anything you see in the repo is exactly what goes live.

## Working with this repo (git basics)

If you're new to git, here's the everyday flow for this project.

**1. Clone it (only once, to get it onto your machine)**

```bash
git clone https://github.com/ThatRobson/Organiser-website.git
cd Organiser-website
```

**2. Check what state you're in**

```bash
git status
```

This tells you which branch you're on and whether you have uncommitted changes. Run it often — it's always safe.

**3. Create a branch before making changes**

Don't edit directly on `main`. Branch off first:

```bash
git checkout -b my-change-name
```

**4. Preview your changes locally**

Since it's static HTML, you can just open `index.html` in a browser, or run a quick local server so relative links/paths behave the same as they will live:

```bash
python3 -m http.server 8000
```

Then visit `http://localhost:8000` in your browser.

**5. Stage and commit your changes**

```bash
git add .
git commit -m "Short description of what you changed"
```

**6. Push your branch to GitHub**

```bash
git push -u origin my-change-name
```

**7. Open a pull request**

GitHub will print a link after the push (or visit the repo on GitHub — it'll show a banner offering to open a PR for your branch). A pull request lets you review the diff before it merges into `main`.

**8. Merge**

Once you're happy with it, merge the PR on GitHub. GitHub Pages will redeploy the live site automatically from `main` within a few minutes.

### A few things worth knowing

- `git status` before anything destructive (`git checkout .`, `git reset --hard`, etc.) — it shows you what you'd lose.
- Commits are local until you `git push` — nothing reaches GitHub (or the live site) until then.
- If you just want to see a diff of what you've changed but not staged yet: `git diff`.
- If you made a mess and just want to discard uncommitted edits to a file: `git checkout -- filename`.

## Privacy

Organiser is designed around a local-first approach. The product brief describes on-device data storage and integrations with Apple services including Calendar, Contacts and notifications. The published Privacy Policy should be kept in step with the actual app implementation as the beta develops.

## Current state

Organiser is in beta and the initial market focus is the UK. The long-term direction is to make the app useful well beyond that starting point, without losing the simple, personal feel that makes it useful in the first place.
