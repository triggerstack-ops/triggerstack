<p align="center">
  <img src="https://img.shields.io/badge/n8n-2.10.3%2B-6366F1?style=for-the-badge&logo=n8n&logoColor=white" alt="n8n 2.10.3+">
  <img src="https://img.shields.io/badge/workflows-4-f43f5e?style=for-the-badge" alt="4 Workflows">
  <img src="https://img.shields.io/badge/nodes-64-06b6d4?style=for-the-badge" alt="64 Nodes">
  <img src="https://img.shields.io/badge/monthly%20cost-$0-10b981?style=for-the-badge" alt="$0/month">
  <img src="https://img.shields.io/badge/price-$27-f59e0b?style=for-the-badge" alt="$27">
</p>

<h1 align="center">⚡ TriggerStack</h1>
<h3 align="center">Lead Gen Agency Toolkit for n8n</h3>

<p align="center">
  4 n8n workflows that scrape leads from 5 platforms, enrich with real emails & socials,<br>
  send automated cold email sequences, and track every deal in a CRM pipeline.<br>
  All running on free tools. $0/month.
</p>

<p align="center">
  <a href="https://triggerstack-ops.github.io/triggerstack/"><strong>🌐 Landing Page</strong></a> · 
  <a href="https://payhip.com/b/MOhmU"><strong>🛒 Get the Toolkit — $27</strong></a>
</p>

---

## The Problem

You know the routine:

| Time | What you're doing | How it feels |
|------|-------------------|-------------|
| 8:00 AM | Searching Google Maps for businesses | Tedious |
| 9:00 AM | Copy-pasting names and phones into a spreadsheet | Mind-numbing |
| 10:00 AM | Visiting each website trying to find an email | Frustrating |
| 11:00 AM | Writing cold emails one at a time | Exhausting |
| 12:00 PM | Realizing you forgot to follow up on last week's leads | Defeated |

**~4 hours of manual work. Every. Single. Day.** For maybe 15 leads, half without emails.

## The Solution

TriggerStack replaces your entire morning with 4 automated workflows that run at 3 AM:

| Time | What TriggerStack does | You |
|------|------------------------|-----|
| 3:00 AM | Scrapes 100+ leads from 5 platforms | Sleeping |
| 5:00 AM | Enriches every lead with real emails, socials, tech stack | Sleeping |
| 8:00 AM | Sends personalized cold emails to hot leads | Waking up |
| 8:15 AM | Pipeline updated, stale deals flagged | Checking results |
| 8:30 AM | Done. | Living your life. |

**30 minutes of review instead of 4 hours of grinding.**

---

## The 4 Workflows

### 🗺️ Workflow 1 — LeadHarvester Pro `25 nodes`

Scrapes **Google Maps, Yelp, Yellow Pages, BBB, and Facebook** simultaneously. Smart deduplication merges the same business across platforms into one record. Every lead gets scored 0–100 and tiered as Hot, Warm, or Cold. Exports to Google Sheets, Airtable, and CSV.

- 5 platforms scraped in parallel
- Cross-platform deduplication with data merging
- 0–100 lead scoring with Hot/Warm/Cold tiers
- Error-resilient: each scraper fails independently

### 🔍 Workflow 2 — EnrichIQ `8 nodes`

Visits each lead's actual website and extracts data from the HTML. Finds **real email addresses** (not guessed patterns), discovers social profiles across 6 platforms, detects tech stack, and estimates company size. Fills in empty email fields automatically.

- Real email discovery from website HTML
- Social profiles: Facebook, Instagram, X, LinkedIn, YouTube, TikTok
- Tech stack detection: WordPress, Shopify, HubSpot, Google Analytics, etc.
- Company size estimation
- Enrichment bonus added to lead score

### ✉️ Workflow 3 — OutreachEngine `14 nodes`

Sends personalized cold emails to hot leads via Gmail SMTP. Runs a **3-email sequence**: initial outreach, gentle follow-up at day 3, and breakup email at day 6. Rate-limited to protect deliverability. Updates outreach status in Google Sheets after every send.

- 3-email automated sequence with auto follow-ups
- Personalized with business name, category, and rating
- Smart rate limiting (random delays between sends)
- Batch processing respects Gmail's 500/day limit

### 💼 Workflow 4 — PipelinePro CRM `9 nodes`

Tracks every deal through **7 pipeline stages**: New Lead → Contacted → Meeting Booked → Proposal Sent → Negotiation → Closed Won → Closed Lost. Flags stale deals, calculates priority scores, suggests next actions, and emails you alerts.

- 7-stage deal pipeline with automatic stage tracking
- Configurable stale thresholds per stage
- Action priority scoring (lead score + deal value + staleness)
- Email alerts for deals that need attention

---

## How It Works

All 4 workflows share **one Google Sheet** as the central data hub:

```
┌─────────────────┐     ┌───────────┐     ┌────────────────┐     ┌──────────────┐
│ LeadHarvester   │────▶│ EnrichIQ  │────▶│ OutreachEngine │────▶│ PipelinePro  │
│ Pro             │     │           │     │                │     │ CRM          │
│                 │     │           │     │                │     │              │
│ Scrapes 5       │     │ Finds     │     │ Sends 3-email  │     │ 7-stage      │
│ platforms       │     │ emails,   │     │ cold sequence  │     │ pipeline     │
│ Scores leads    │     │ socials,  │     │ Auto follow-up │     │ Stale alerts │
│ 0–100           │     │ tech stack│     │ Rate-limited   │     │ Priority     │
└─────────────────┘     └───────────┘     └────────────────┘     └──────────────┘
      3:00 AM               5:00 AM           Every 8 hrs          Every 6 hrs
```

## Free Tool Stack

| Tool | Used By | Free Tier |
|------|---------|-----------|
| **n8n** | All 4 workflows | Self-hosted = unlimited. Cloud = 5 workflows free |
| **SerpAPI** | LeadHarvester Pro | 100 searches/month → ~400+ leads |
| **Google Sheets** | All 4 workflows (shared hub) | Unlimited |
| **Gmail SMTP** | OutreachEngine + PipelinePro | 500 emails/day |
| **Website fetching** | EnrichIQ | Built into n8n, unlimited |

**Total monthly cost: $0**

---

## What's in the Toolkit

| File | Description |
|------|-------------|
| `LeadHarvester_Pro_Workflow.json` | 5-platform scraper with lead scoring (25 nodes) |
| `EnrichIQ_Workflow.json` | Email & social enrichment (8 nodes) |
| `OutreachEngine_Workflow.json` | 3-email cold sequence (14 nodes) |
| `PipelinePro_CRM_Workflow.json` | 7-stage CRM pipeline (9 nodes) |
| `LeadHarvester_Pro_Setup_Guide.docx` | 30-page step-by-step setup guide |
| `Bonus_Workflows_Setup_Guide.docx` | Setup guide for EnrichIQ, OutreachEngine, PipelinePro |
| `LeadHarvester_Troubleshooting_Guide.docx` | Every real error encountered + fix |
| `LeadHarvester_Loom_Script.docx` | Video walkthrough script |
| `TriggerStack_Master_Template.xlsx` | 64-column Google Sheets template with dashboard |
| `TriggerStack_Airtable_Import.csv` | Ready-to-import Airtable template |
| `README.md` | Quick-start reference |

## Compatibility

| Requirement | Details |
|-------------|---------|
| **n8n version** | 2.10.3 or higher (tested through 2.12.x) |
| **Node IDs** | RFC 4122 UUIDs (v2.x native) |
| **HTTP Request** | typeVersion 4.2, genericCredentialType |
| **Code nodes** | typeVersion 2, task-runner safe |
| **Publish/Save** | Imports as inactive draft, publish when ready |
| **Error handling** | `onError: continueRegularOutput` on all scrapers |

> ⚠️ **This toolkit requires n8n 2.x.** It will not work on n8n 1.x.

---

## Quick Start

```bash
# 1. Self-host n8n (if you don't have it)
docker run -d --name n8n -p 5678:5678 \
  -v n8n_data:/home/node/.n8n \
  docker.n8n.io/n8nio/n8n:latest

# 2. Open n8n
open http://localhost:5678
```

Then:
1. **Import** → Three-dot menu → Import from File → select each `.json`
2. **Credentials** → Add HTTP Query Auth credential with your [SerpAPI](https://serpapi.com) key
3. **Connect** → Point Google Sheets nodes to the master template
4. **Configure** → Edit the Settings node: search query + location
5. **Test** → Click "Test Workflow"
6. **Publish** → When it works, click Publish to activate schedules

**Time to first leads: ~25 minutes.**

---

## The Math

| Metric | Value |
|--------|-------|
| Time saved per day | ~4 hours |
| Time saved per month | ~80 hours |
| Value at $25/hr | **$2,000/month** |
| Toolkit cost | **$27 one-time** |
| Monthly running cost | **$0** |
| ROI on day 1 | **74x** |

---

## Who This Is For

- **Freelancers** who need a steady flow of local business leads
- **Agency owners** running lead gen for multiple clients
- **Sales teams** that want to automate cold outreach
- **n8n users** who want production-ready workflows (not broken v1.x templates)
- **Anyone** tired of paying $150+/month for tools that only scrape Google Maps

## Who This Is NOT For

- People looking for a free template (this is a paid product)
- n8n 1.x users (you must upgrade to 2.10.3+)
- People who expect leads without any setup (25 min setup is required)

---

<p align="center">
  <a href="https://payhip.com/b/MOhmU">
    <img src="https://img.shields.io/badge/GET%20THE%20TOOLKIT-$27%20→-f43f5e?style=for-the-badge&logoColor=white" alt="Get the Toolkit">
  </a>
</p>

<p align="center">
  <a href="https://triggerstack-ops.github.io/triggerstack/">🌐 Landing Page</a> · 
  <a href="https://payhip.com/b/MOhmU">🛒 Payhip</a>
</p>

<p align="center">
  <sub>Built by <strong>TriggerStack</strong> · Automation templates that actually work.</sub><br>
  <sub>Compatible with n8n 2.10.3 through latest · 30-day money-back guarantee</sub>
</p>
