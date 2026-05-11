# QSR AI Ops Preview

Practical AI workflow preview for quick-service restaurants, POS builders, and automation consultants.

This repo is a buyer-readable demo, not a generic AI toy. It shows how lightweight n8n workflows and small agent specs can sit around an existing POS to recover missed orders, normalize messy intake, flag inventory risks, triage reviews, and produce daily manager summaries.

## Fast Read

If you run or build restaurant/POS software, the first question is not "can AI replace the POS?"

The useful question is:

```text
Where are orders, reviews, inventory counts, manager notes, and customer follow-ups leaking money before a human sees them?
```

This preview focuses on those edges. It does not require replacing the POS. The first implementation can run beside the POS through exports, webhooks, email/SMS, Google Sheets, Slack, or API endpoints.

## Live Offer

- Full sales page: https://igorganapolsky.github.io/qsr-n8n-workflow-vault-site/
- Visual POS compatibility demo: https://igorganapolsky.github.io/qsr-n8n-workflow-vault-site/pos-compatibility-demo.html
- Same-day workflow teardown: https://buy.stripe.com/6oU4gz3Ug7Dg6tPfSH3sI1e
- Setup diagnostic / POS compatibility map: https://buy.stripe.com/eVq28rfCY0aOdWh5e33sI0N

The setup diagnostic is the right next step for POS builders or restaurant operators who want to know which workflow should plug in first.

## What This Demo Includes

- Importable n8n workflow previews in `workflows/n8n/`
- OpenClaw-ready agent specs in `openclaw-agents/`
- Test fixtures for sample orders, inventory counts, waste logs, reviews, and shift notes in `fixtures/`
- A POS compatibility map in `docs/pos-compatibility-map.md`
- A 2-minute walkthrough script in `docs/demo-walkthrough.md`

## Included Workflow Previews

1. `qsr-order-intake-normalizer.json`
   Turns messy order/channel intake into structured fields for review, routing, and manager handoff.

2. `qsr-inventory-reorder-watch.json`
   Flags low-stock items and creates reorder alerts before menu availability breaks.

3. `qsr-review-triage-desk.json`
   Drafts review responses and escalates food safety, refund, allergy, and legal-risk cases.

4. `qsr-daily-store-ops-digest.json`
   Summarizes shift notes, customer issues, equipment notes, and opening tasks for managers.

5. `qsr-loyalty-winback-segmenter.json`
   Segments customers for follow-up and winback campaigns without making the POS the campaign brain.

## Integration Pattern

The safest first version is edge automation:

```text
POS / ordering channel / review site / inbox
  -> export, webhook, API, email, SMS, or sheet row
  -> n8n workflow
  -> AI triage or summary
  -> manager approval, Slack/SMS/email, CRM, or POS note
```

Start with intake, summaries, alerts, and human handoff. Do not start by letting AI autonomously change orders, refunds, tax, allergy handling, or menu availability.

## Good First Use Cases

- Missed catering lead follow-up
- DM/SMS order clarification
- Low-stock reorder alerts
- Daily manager digest
- Review response triage
- Loyalty/winback segmentation

## What I Need To Map A POS

For a POS compatibility pass, send any of these:

- API docs or webhook docs
- sample order export
- sample customer export
- review/inbox source
- current manager reporting flow
- where staff already approve actions

I will map the first low-risk workflow to plug in, the integration path, the human approval point, and the smallest paid pilot worth building.

## Buyer Promise

Recover missed follow-ups and reduce manager busywork without replacing the POS or retraining the whole store.

## Disclaimers

These are starter systems. Buyers must test menu logic, tax rules, allergy warnings, refunds, privacy policies, and POS integrations before using any automation in production. This project is not affiliated with Subway, Yum Brands, Restaurant Brands International, DoorDash, Uber Eats, Toast, Square, n8n, or OpenClaw.
