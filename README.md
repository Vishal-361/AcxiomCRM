# AcxiomCRM

A full-stack **Customer Relationship Management** web application built with
**ASP.NET Core 8 MVC + ASP.NET Core Identity + Entity Framework Core (SQLite)**.

## What's inside

- `AcxiomCRM.zip` — the complete project source (solution + `src/AcxiomCRM`)
- `AcxiomCRM_Demo.mp4` — a 2:50 screen-recorded walkthrough covering every
  evaluation item: login, dashboard analytics, client-side validation,
  lead workflow + convert-to-customer, opportunity pipeline, business rules,
  follow-up rules, audit log, role-based scoping, REST API, and architecture

## Features

- Authentication: PBKDF2 password hashing, 8-character complexity policy,
  5-attempt / 15-minute account lockout
- Roles: **Admin**, **Manager**, **SalesExecutive** — with server-side record
  scoping (sales executives only see their own records)
- Users & roles administration, append-only audit log
- Dashboard with KPIs, Chart.js analytics, and date filters
- Customers (duplicate prevention), Leads (workflow-guarded statuses,
  convert to customer), Opportunity pipeline board with weighted values,
  Follow-ups (overdue tracking), Activities
- 8 reports with CSV export
- Secured REST API (`/api/auth`, `/api/customers`, `/api/leads`, `/api/opportunities`,
  `/api/followups`, `/api/reports/pipeline`) with DTOs and proper status codes
- Client-side (jQuery Unobtrusive, incl. a custom date-not-in-past adapter)
  **and** server-side validation throughout

## Run it

Requires the [.NET 8 SDK](https://dotnet.microsoft.com/download/dotnet/8.0).

```bash
unzip AcxiomCRM.zip
cd AcxiomCRM/src/AcxiomCRM
dotnet run
```

Then open http://localhost:5000 (or the URL shown in the console).

## Demo logins

Use these accounts to try the app:

| Role            | Email                 | Password   |
|-----------------|-----------------------|------------|
| Admin           | admin@acxiomcrm.com   | Admin@123  |
| Manager         | manager@acxiomcrm.com | Manager@123 |
| Sales Executive | sales@acxiomcrm.com   | Sales@123  |

Tip: log in as the sales executive first, then as admin, to see how
role-based record scoping changes what each user can see.

## Docs

Full details live inside the zip: `README.md`, `docs/TRACEABILITY.md`
(every spec requirement mapped to code), `docs/API.md`, and
`docs/DEMO_SCRIPT.md` (step-by-step evaluation demo guide with viva Q&A).
