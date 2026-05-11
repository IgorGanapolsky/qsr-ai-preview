# 2-Minute Demo Walkthrough

Use this script for a quick buyer walkthrough.

## 0:00 - Problem

Most restaurants do not need a giant AI transformation. They lose money in small handoffs: missed catering inquiries, messy order notes, low-stock surprises, slow review responses, and managers chasing shift details manually.

## 0:20 - Architecture

This preview sits around the POS. It can start from exports, webhooks, API endpoints, email, SMS, Google Sheets, or Slack. The POS stays the source of truth.

## 0:40 - Workflow Tour

Show `workflows/n8n/`:

- order intake normalizer
- inventory reorder watch
- review triage desk
- daily store ops digest
- loyalty winback segmenter

## 1:10 - Agent Specs

Show `openclaw-agents/`:

- order triage agent
- inventory forecaster agent
- reputation agent

Explain that these are intentionally narrow agents with specific escalation rules.

## 1:35 - POS Compatibility

Show `docs/pos-compatibility-map.md`.

The paid diagnostic maps the buyer's actual POS surface to the first workflow worth building.

## 1:55 - Call To Action

For a POS builder or restaurant operator:

```text
Send me the API/export/webhook surface and I will map the first low-risk workflow to install.
```
