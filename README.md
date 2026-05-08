# QSR AI Ops Pack

Importable AI automation templates for quick-service restaurants, ghost kitchens, franchise operators, and automation consultants serving food-service clients.

This pack is built to sell as a narrow outcome product, not a generic workflow dump. It gives buyers five workflows, three OpenClaw-ready agent specs, prompt libraries, test payloads, and setup guidance for adapting the automations to Subway-style ordering, inventory checks, waste review, customer reviews, and shift handoffs.

## What Buyers Get

- 6 importable n8n workflow JSON templates
- 3 OpenClaw-ready AI agent specs
- QSR prompt library for ordering, inventory, reviews, and manager reporting
- Test fixtures for sample orders, inventory counts, waste logs, reviews, and shift notes
- Setup guide, environment variable checklist, and operator QA checklist
- Gumroad buyer license

## Included Workflows

1. AI Order Triage Agent
2. Inventory Forecaster and Reorder Alerts
3. Daily Waste and Loss Report
4. Customer Review Responder
5. Shift Handoff Briefing
6. Stripe Payment Fulfillment Email

## Suggested Pricing

- Launch price: $29
- Standard price: $49
- Agency/commercial license: $149

For faster cashflow, sell the pack at $49 with a $149 "client-use" license for freelancers and automation agencies.

## Buyer Promise

"Install five restaurant-ready AI workflows in n8n and adapt them to your menu, store rules, and manager alerts in under one afternoon."

## Setup

1. Import a workflow from `templates/n8n`.
2. Create credentials in n8n for OpenAI or OpenRouter, Google Sheets, Gmail, Slack, Twilio, or your chosen equivalents.
3. Copy `.env.example` into your n8n environment or deployment secrets.
4. Run each workflow with the matching fixture in `fixtures`.
5. Customize prompt text in `prompts`.

## Disclaimers

These templates are starter systems. Buyers must test menu logic, tax rules, allergy warnings, refunds, privacy policies, and POS integrations before using any automation in production. This product is not affiliated with Subway, Yum Brands, Restaurant Brands International, DoorDash, Uber Eats, Toast, Square, or n8n.
