# Python developer

I automate business processes: CRM and payment integrations, LLM agents, processing of complex data, backend
services and Telegram bots. From a script to a product that runs in production. Open to work.

Open source, with tests and CI on Python 3.9-3.13:

- **[svcwatch](https://github.com/ololowj-dotcom/svcwatch)** - a watchdog for Linux servers that reports to Telegram
  (systemd, Docker, processes, HTTP/TCP).
- **[tgcast](https://github.com/ololowj-dotcom/tgcast)** - mailing to a base of Telegram chats: one message posted to
  every channel and group in your list, with previews, permission checks, safe pauses and no repeats.

Client code is private under NDAs, so the projects below are described rather than linked.

## Selected projects

### CRM sync and online payments for an e-commerce store
Commerce backend for an existing shop: orders and payment statuses are synchronised with RetailCRM in real time; online
payments (YooKassa with a fiscal receipt under Russian law 54-FZ, or T-Kassa) with server-side re-verification of the
amount and status, so neither price nor payment fact is trusted to the client. A separate bot delivers order cards to
managers with one-time-code subscription. Custom CRM panel: login, revenue and order overview.
`Python` `RetailCRM API` `YooKassa` `webhooks` `aiogram`

### Multi-agent system for Wildberries sellers
Handling of negative reviews: an agent finds a review, talks to the buyer in the seller chat and brings the case to a
return request and an updated review. One agent classifies the buyer's replies (LLM with a rule-based fallback), another
checks outgoing messages for policy risks; outgoing texts come only from templates. Also rating-reason analysis and
seller-account monitoring (stock, prices, commissions). Autonomous engine that respects marketplace API limits, outgoing
queue, multi-tenant web panel, automated tests. Status: in development, piloted on a real account.
`Python` `FastAPI` `LLM` `Next.js` `SQLite` `Wildberries API`

### HR reporting automation for a state hospital
A program parses heterogeneous Excel timesheets of every department (about 1,000 employees) and computes the average
headcount under the official statistical methodology (Rosstat Order No. 638): it finds and removes duplicates and
phantom rows, and the result was reconciled with the accountants' manual calculation until it matched exactly. One
unified timesheet template for all departments and a web panel: upload an archive of tables and get the finished
document in a couple of minutes. Staff used to spend two days on it by hand.
`Python` `openpyxl` `web panel`

### Daily Wildberries reporting into Google Sheets
Stock by warehouse, the sales funnel and advertising spend with an automatic ad-cost-ratio calculation land in a
spreadsheet every morning, with no manual export. Cumulative history, automatic cleanup of stale data; runs on a
schedule for months unattended and survives changes of API endpoints and limits.
`Python` `Wildberries API` `Google Sheets API` `cron`

### LLM matchmaking in Telegram
A dating service with weekly rounds: an LLM ranks pairs from questionnaires and explains why they fit. The model
sometimes ignored the "never repeat a pair" rule, so the guarantee is enforced in code; personal data is anonymised
before it reaches the LLM, a fallback algorithm covers model outages, and there are 60+ automated tests.
`Python` `aiogram 3` `LLM` `SQLite`

### E-commerce stores with a custom CMS
Two clothing stores on a shared codebase: catalogue, cart, checkout, a no-code admin (texts, products, orders,
lookbook), legal pages, and a security review (CSRF, rate limiting, upload validation, signed sessions).
`Next.js` `Prisma` `Tailwind` `Motion`

### Scroll-storytelling sales site
For a solar-equipment seller: the day turns into night as you scroll, the product explodes into layers, leads reach
Telegram through a delivery queue that survives network failures, Yandex Metrica goals for ad campaigns, SEO. Page weight
cut from 28 MB to 2.7 MB.
`GSAP` `Lenis` `Yandex Metrica` `Telegram API`

### SaaS and platforms in Telegram
A job platform by city (employer and candidate roles, moderation, paid listings, AI text improvement), a multi-bot SaaS
for beauty professionals (a main bot sells access and launches personal bots), and a document bot that turns PDFs, DOCX
files and scans into a structured report via OCR and an LLM.
`Python` `aiogram 3` `YooKassa` `Tesseract` `PostgreSQL`

All 34 projects with descriptions and screenshots: **[okulovdeveloper.space](https://okulovdeveloper.space)** and the
Telegram Mini App [cases-miniapp.vercel.app](https://cases-miniapp.vercel.app).

## Telegram bots with live demos

| Bot | What it does | Demo |
|---|---|---|
| AI psychologist | CBT-style dialogue, subscriptions, auto-billing, admin panel | [@TerraPsychology_bot](https://t.me/TerraPsychology_bot) |
| AI astrologer | forecasts by birth date, compatibility, premium tier | [@AstroMatcherBot](https://t.me/AstroMatcherBot) |
| Entertainment AI bot | a character with attitude, paid extended access | [@Bydlochat_bot](https://t.me/Bydlochat_bot) |
| Portfolio bot + Mini App | case showcase, demo chats, request form | [@Tgprokeys_bot](https://t.me/Tgprokeys_bot) |

## Stack

- **Languages and backend:** Python (asyncio, FastAPI, aiogram 3), Rust for high-load tasks
- **AI:** OpenAI, Claude, DeepSeek, RAG, OCR
- **Data:** PostgreSQL, SQLite, Redis, Excel and Google Sheets
- **Frontend:** React, Next.js, TypeScript, Telegram WebApp SDK
- **Integrations:** RetailCRM, amoCRM, Bitrix24, MoySklad, Wildberries, payment systems (YooKassa, T-Kassa, CloudPayments, Stripe)
- **Infrastructure:** Linux, Docker, Nginx, systemd, CI

## Contact

Reach me through GitHub. I can show code samples without any customer data or do a small test assignment.
