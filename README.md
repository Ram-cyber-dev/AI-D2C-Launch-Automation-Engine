# 🚀 AI D2C Launch Kit PRO — Multi-Agent Production Engine

An end-to-end n8n automation with 4 AI agents that converts one product form submission into a complete D2C launch campaign in 90 seconds.

## 🎯 What It Does

Takes a single product launch form and automatically generates:
- **Bain-level market intelligence** — competitor analysis, market gaps, SWOT, positioning
- **60+ marketing assets** — marketplace copy, 18 emails, ads, social posts, influencer strategy
- **AI-generated product visuals** — uploaded to Google Drive campaign folder
- **QA scorecard** — 7-dimension quality review with deploy readiness flag
- **A/B test variants** — 3 headline variants with predicted CTR and recommendation
- **Hindi cultural adaptation** — tagline, headlines, WhatsApp, Instagram in Hindi
- **WhatsApp Commerce Bot** — complete sales flow with objection handlers and UPI payment
- **Dual email delivery** — mega kit to agent + executive brief to brand owner
- **Google Sheets CRM** — every campaign logged automatically

## 🤖 4 AI Agents

| Agent | Role | Model |
|-------|------|-------|
| Agent 1: Market Intelligence | Bain-level competitor + market analysis | Gemini 2.0 Flash |
| Agent 2: Senior Copywriter | 60+ assets across all channels | Gemini 2.0 Flash |
| Agent 3: Image Generator | Product hero + ad banner visuals | gpt-image-2 |
| Agent 4: QA Reviewer | 7-dimension quality scorecard | Gemini 2.0 Flash |

---

## 🏗️ Architecture (27 nodes)

```
Form → Parse+UTM → Agent1:Intel → Parse Intel → Agent2:Copy → Parse Kit →
Build Image Prompts → Create Drive Folder → Stage Folder → Split:2 Images →
Agent3:Image Gen → Extract Binary → Upload to Drive → Aggregate Gallery →
Agent4:QA → Parse QA → AB Test Generator → Parse AB Tests →
Hindi Translation → Parse Hindi → WhatsApp Commerce → Parse WhatsApp →
Log to Sheets → Build Mega Email → Send to Agent →
Build Owner Brief → Send to Owner
```

---

## ⚙️ Tech Stack

| Component | Technology |
|-----------|-----------|
| Automation | n8n (self-hosted) |
| Market Intel + Copy + QA | Gemini 2.0 Flash |
| Image Generation | gpt-image-2 (OpenAI) |
| A/B Testing + Hindi + WhatsApp | GPT-4o-mini |
| Asset Storage | Google Drive |
| CRM Logging | Google Sheets |
| Email Delivery | Gmail API |


## 🚀 Key Features

- **27 nodes** — most comprehensive workflow in the cohort
- **4 AI agents** in sequence — each feeds the next
- **Campaign ID + UTM** auto-generated for every launch
- **Google Drive folder** per campaign — organized, shareable, permanent
- **A/B Test Generator** — 3 variants scored before any spend
- **Hindi Translation** — cultural adaptation, not just translation
- **WhatsApp Commerce Bot** — complete sales flow with UPI payment
- **QA Gate** — deploy readiness scored before delivery
- **Error resilience** — fallbacks at every AI parsing stage


## 💡 Zero-Cost Optimization

Replaced:
- D2C launch agency (₹1–3 Lakhs, 5 weeks)
- Canva Pro for visuals
- Copywriter for 60+ assets
- Hindi translator
- WhatsApp chatbot developer
- QA review team

**Total cost: ₹0. Time: 90 seconds.**


## 🔧 Setup

1. Import `AI_D2C_Launch_Kit_PRO.json` into n8n
2. Configure credentials:
   - **Google Gemini** — Query Auth with Gemini API key
   - **OpenAI** — API key (gpt-4o-mini + gpt-image-2 access required)
   - **Gmail** — OAuth2
   - **Google Sheets** — OAuth2
   - **Google Drive** — OAuth2
3. Create Google Sheet: `D2C Launch Kits` with tab `D2C_Products_Tab_v2`
4. Create Google Drive folder: `AI Launch Kits` (parent folder for campaigns)
5. Add columns to sheet: Product, Brand, Category, Price, Launch Offer, Available On, Owner, Owner Email, Campaign ID, QA Score, Drive Folder, Positioning, Market Size, Projected M1 Revenue, Target CAC, Target ROAS, Images Generated, Languages, Brand Voice, Budget, Launch Date, Status, Generated At


## 🎬 Demo Product

**GlowVeda Vitamin C Serum** — 20% stabilised Vitamin C, ₹699 MRP, targeting women 22-38 in metro India. Competitors: Minimalist, The Derma Co, Plum.


## 👤 Author

Built by Ram
Founder, MissedCallRecovery.org — AI voice receptionist 
platform for US plumbing and HVAC businesses 
Building done-for-you AI systems for D2C brands and service businesses
Available for freelance AI automation projects 
[GitHub](https://github.com/Ram-cyber-dev)
