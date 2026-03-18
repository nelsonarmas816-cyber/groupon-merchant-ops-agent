# Merchant Ops Triage Agent · Groupon Madrid

AI-first intelligent request routing agent built for the Groupon 
Chief of Staff – Global Operations assignment (Option B: Merchant 
Ops AI Transformation).

## What it does

A working AI agent built directly on the Anthropic Claude API 
using native tool use and multi-step reasoning. It ingests merchant 
requests, enriches them with merchant context, and autonomously 
decides the optimal routing — no frameworks, no backend, runs 
entirely in the browser.

**Two modes:**
- **Single Request Triage** — classifies, enriches, and routes 
  individual requests with full reasoning steps visible
- **Batch Queue Processing** — processes a queue of 24 real 
  pending/escalated requests from the assignment dataset and 
  produces a prioritised work queue

**Three tools (native Claude tool use):**
- `lookup_merchant_profile` — retrieves tier, GMV, churn risk, NPS
- `get_request_history` — fetches recent escalations and SLA breaches
- `flag_account_manager` — fires an alert for high-risk merchants

**Five routing outcomes:**
Auto-Resolve · BPO Standard · In-House Specialist · 
Manager Escalation · Urgent Escalation

## How to run locally

1. Download `merchant_triage_agent.html`
2. Open the file in a text editor
3. Find this line near the top of the script section:
```javascript
   const API_KEY = "YOUR_ANTHROPIC_API_KEY_HERE";
```
4. Replace `YOUR_ANTHROPIC_API_KEY_HERE` with your own 
   Anthropic API key from console.anthropic.com
5. Save the file and open it in Chrome or Firefox
6. No server, no install, no dependencies needed

> **Note:** A working demo version with API key included is 
> provided separately in the submission zip file.

## Tech stack

- Plain HTML + CSS + vanilla JavaScript (no frameworks)
- Anthropic Claude API `/v1/messages` — claude-sonnet-4-6
- Native tool use via the `tools` parameter
- Merchant data embedded directly in the file (no backend)

## Assignment context

- **Role:** Chief of Staff – Global Operations, Groupon Madrid
- **Option:** B — Merchant Ops AI Transformation
- **Dataset:** merchant_requests.csv (8,000 rows) + 
  merchant_profiles.csv (1,200 rows)
- **Candidate:** Sebastian
