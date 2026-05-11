# POS Compatibility Map

Use this to decide whether a restaurant/POS automation should start with order intake, missed follow-up, inventory, reviews, or manager reporting.

## Best First Integration Surfaces

| Surface | What to look for | Best first workflow |
| --- | --- | --- |
| Order export | CSV, API endpoint, webhook, emailed order summary | Order intake normalizer |
| Customer/contact export | phone, email, visit date, order count | Loyalty winback segmenter |
| Inventory export | item, on hand, par level, vendor pack size | Inventory reorder watch |
| Review feed | Google/Yelp/manual inbox, rating, review text | Review triage desk |
| Shift notes | manager notes, incidents, equipment, opening tasks | Daily store ops digest |
| Missed call/DM/SMS | message body, phone, timestamp, intent | Missed lead follow-up |

## Low-Risk Pilot Rules

Start with workflows that prepare, summarize, and route information.

Avoid the first pilot touching:

- autonomous refunds
- allergy guarantees
- tax calculations
- automatic menu item availability changes
- staff scheduling decisions
- direct customer promises without human review

## Diagnostic Output

A useful compatibility diagnostic should produce:

- the first workflow to install
- the exact data source
- the approval point
- the failure mode to guard against
- the setup checklist
- the first measurable result

Example measurable result:

```text
Every catering inquiry gets a structured summary and manager follow-up reminder within 5 minutes.
```
