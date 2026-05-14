# QSR AI Ops Preview

**For QSR operators, POS builders, and automation consultants who want AI workflows that sit *beside* the POS — not replace it.**

This repo is the readable preview. The buyable version is:

- **[$29 — QSR AI Ops Template Pack →](https://iganapolsky.gumroad.com/l/qsr-ai-ops-pack)** — the 5 n8n workflows, OpenClaw agent specs, test fixtures, and POS compatibility map in this repo, packaged for import.
- **[$499 — 48-Hour Workflow Diagnostic →](https://iganapolsky.gumroad.com/l/qsr-ai-automation-diagnostic)** — you send your POS export + one workflow you want to automate; I send back a written plan with integration path, approval gate, and the smallest paid pilot worth building.

[Full sales page](https://igorganapolsky.github.io/qsr-n8n-workflow-vault-site/) · [POS compatibility demo](https://igorganapolsky.github.io/qsr-n8n-workflow-vault-site/pos-compatibility-demo.html)

---

## The useful question

Not "can AI replace the POS?" — that question is unsellable inside an operating restaurant.

The useful question is:

```text
Where are orders, reviews, inventory counts, manager notes, and customer
follow-ups leaking money before a human sees them?
```

The workflows in this repo target those edges. They run *beside* the POS through exports, webhooks, email/SMS, Google Sheets, Slack, or API endpoints. No POS replacement required.

## What's in the repo (and the $29 pack)

Five importable n8n workflows, each with a real outcome:

| Workflow | What it does | Who feels the pain |
|---|---|---|
| `qsr-order-intake-normalizer.json` | Turns messy multi-channel orders (DM, SMS, online forms) into structured fields for review and routing | Catering lead handlers, ghost-kitchen ops |
| `qsr-inventory-reorder-watch.json` | Flags low-stock items and drafts reorder alerts before menu availability breaks | Single-store owner-operators, multi-unit GMs |
| `qsr-review-triage-desk.json` | Drafts review responses; escalates food-safety, allergy, refund, and legal-risk cases to humans | Brand managers, district managers |
| `qsr-daily-store-ops-digest.json` | Summarizes shift notes, customer issues, equipment notes, and opening tasks | Multi-unit operators reading 6 store reports each morning |
| `qsr-loyalty-winback-segmenter.json` | Segments lapsed customers for follow-up without making the POS the campaign brain | Operators with a POS that "has loyalty" but no real winback |

Plus:
- OpenClaw-ready agent specs in `openclaw-agents/` — for builders running local agents with approval gates
- Test fixtures (`fixtures/`) — sample orders, inventory counts, waste logs, reviews, shift notes you can run through each workflow on day one
- POS compatibility map (`docs/pos-compatibility-map.md`) — Toast, Square, Clover, and Subway-style POS surfaces ranked by what's automatable first
- 2-minute walkthrough script (`docs/demo-walkthrough.md`) — for consultants selling this to operators

## The safe integration pattern

```text
POS / ordering channel / review site / inbox
  → export, webhook, API, email, SMS, or sheet row
  → n8n workflow
  → AI triage or summary
  → manager approval
  → Slack / SMS / email / CRM / POS note
```

Start with intake, summaries, alerts, and human handoff.

**Do not** start by letting AI autonomously change orders, refunds, tax, allergy handling, or menu availability. That's how brands get sued.

## FAQ

**What exactly do I get for $29?**
A downloadable ZIP with the 5 n8n workflow JSONs, the OpenClaw agent specs, the test fixtures, the POS compatibility map, and the demo walkthrough script — same content as in this repo, packaged for immediate import. License: use in client work, do not resell as-is.

**What do I get for $499?**
A 48-hour async written diagnostic. You send: API/webhook docs from your POS, a sample order export, a sample customer export, your review/inbox source, your current manager reporting flow, and where staff already approve actions. I send back: the first low-risk workflow to plug in, the integration path, the human approval point, and the smallest paid pilot worth building. Async — no calls required.

**Refund policy?**
$29 pack: 14-day refund if the workflows don't import into your n8n instance. $499 diagnostic: full refund if you don't receive a written deliverable within 72 hours of sending the inputs.

**Is this affiliated with Subway / Toast / Square / n8n / OpenClaw?**
No. See disclaimers below.

**Can I just clone the repo and skip the $29?**
Yes — this preview is public on purpose. The $29 pack saves you the assembly time and includes the demo walkthrough script. The $499 diagnostic is what most buyers actually need: someone to look at *their* POS and tell them what to automate first.

## Good first use cases

- Missed catering lead follow-up
- DM/SMS order clarification
- Low-stock reorder alerts
- Daily manager digest
- Review response triage
- Loyalty/winback segmentation

## Next step

- **Operator / GM:** → [Book the 48-hour diagnostic ($499)](https://iganapolsky.gumroad.com/l/qsr-ai-automation-diagnostic)
- **POS builder / consultant:** → [Get the template pack ($29)](https://iganapolsky.gumroad.com/l/qsr-ai-ops-pack) and resell setup work to your restaurant clients
- **Just browsing:** clone the repo, import a workflow into n8n, and run a fixture through it

## Disclaimers

These are starter systems. Buyers must test menu logic, tax rules, allergy warnings, refunds, privacy policies, and POS integrations before using any automation in production. This project is not affiliated with Subway, Yum Brands, Restaurant Brands International, DoorDash, Uber Eats, Toast, Square, n8n, or OpenClaw.
