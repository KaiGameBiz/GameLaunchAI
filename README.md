<div align="center">

# 🎮 GameLaunchAI

### Launch diagnosis for mobile game teams.
### Know what's broken. Know what to fix first.

**Before you spend your first dollar on UA — get a diagnosis, not a report.**

[Demo](https://gamelaunchai.vercel.app) · [Documentation](#how-it-works) · [中文文档](#中文)

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](https://opensource.org/licenses/MIT)
[![MCP Compatible](https://img.shields.io/badge/MCP-Compatible-purple.svg)](#mcp-support)
[![Mobile Game](https://img.shields.io/badge/Focus-Mobile_Game-green.svg)](#)

</div>

---

## The Problem

You built a mobile game. Now what?

- You have $3,000 for UA. Is that a **test budget** or a **launch budget**?
- Your D1 retention is 32%. Should you **buy more traffic** or **fix the product**?
- Your rewarded video brings in $0.04 ARPDAU. Is that **good for your genre**?
- Your IAP conversion is 1.8%. Is your paywall **too early, too late, or missing items**?
- You're in soft launch in Philippines. **Is it time to scale to US, or time to stop?**

Most mobile games fail not because the game is bad — but because the **launch decisions** are wrong. Wrong budget allocation, wrong monetization design, wrong market timing.

**GameLaunchAI doesn't give you a 30-page report. It gives you a verdict and your next 3 actions.**

---

## What It Does

GameLaunchAI is an open-source AI diagnosis tool for **mobile game** teams. Input your game data, get a clear **go / no-go decision** and **specific next steps**.

### Three core diagnoses:

#### 🎯 UA Viability Check
> Should you spend that budget?

Input your game type, target market, budget, and early metrics. Get back: is this a measurement budget or a launch budget? What should you test first — creative, store page, or the product itself? Should you keep spending or pause?

#### 💊 Monetization Health Check
> Is your monetization design helping or hurting?

The deepest diagnosis. Covers all three mobile monetization pillars:

| Pillar | What it checks |
|--------|---------------|
| **IAA (ads)** | Ad placement health, retention impact per slot, reward economy balance, ad cap optimization, eCPM benchmarks |
| **IAP (in-app purchase)** | SKU sufficiency, price ladder design, conversion funnel, ARPPU, revenue growth sustainability |
| **Hybrid** | IAP/IAA cannibalization risk, ad-free pack pricing, optimal monetization mix for your genre |

Every ad slot gets a health rating: 🟢 healthy, 🟡 caution, 🔴 hurting retention.

#### 🚦 Soft Launch Readiness
> Go or no-go?

Input your stage, GEO, D1/D7 retention, revenue structure, and CPI. Get back: have you hit the gates for the next phase? Should you fix the product or keep testing UA? Are you ready to expand to higher-CPI markets?

### Every diagnosis includes:

- ✅ **Go / No-go verdict** — A clear decision, not a hedge
- 🔍 **Root cause attribution** — Is the problem in creative, App Store listing, retention, monetization, or UA strategy?
- 📋 **Next 3 actions** — Specific and executable. Not "improve retention." More like "move the interstitial trigger from level 3 to level 5, expected D7 lift: 3-5 points."
- 📊 **Benchmark comparison** — Your metrics vs. industry baselines for your genre and region

---

## Who It's For

**Solo devs & small teams (1-5 people)** building casual, puzzle, idle, or light F2P mobile games with UA budgets under $10K. You need to know if that first spend is worth it.

**Small F2P studios (5-20 people)** preparing for or in soft launch. You're looking at retention, CPI, and ARPDAU curves trying to figure out: fix the product, or start scaling?

**Not for**: PC/console developers, web games, premium/paid games, large studios with dedicated publishing teams.

---

## Free vs Pro

The core diagnosis engine is **free and open source**. You bring your own LLM API key and run locally.

| | Free (Open Source) | Pro | Advisory |
|---|---|---|---|
| **UA Viability Check** | ✅ Full | ✅ Full | ✅ Full |
| **IAA diagnosis** | ✅ Ad health + reward risk | ✅ + eCPM benchmarks + network optimization | ✅ |
| **IAP diagnosis** | Preview only | ✅ SKU analysis + funnel + revenue health | ✅ |
| **Hybrid diagnosis** | Preview only | ✅ Cannibalization check + model recommendation | ✅ |
| **Soft Launch Readiness** | ✅ Full | ✅ Full | ✅ Full |
| **Benchmark data** | 3 genres × 3 regions | 12+ genres × 15+ regions, quarterly updates | Same |
| **Output detail** | Directional advice | Specific numbers + competitor references | Same |
| **1-on-1 with game marketer** | — | — | ✅ Strategy sessions |
| **Ad platform deal advice** | — | — | ✅ Negotiation guidance |
| **API key** | Yours (self-hosted) | Included (cloud) | Included |
| **Price** | $0 | Coming soon | Coming soon |

> Free version: valuable enough to star. Pro version: precise enough to pay for.

---

## How It Works

```
You describe your mobile game    →  Stage classifier determines:
and enter your metrics               pre-launch / beta / soft launch / live
                                              ↓
                              3 specialized AI agents diagnose:
                              • UA viability
                              • Monetization health (IAP + IAA + hybrid)
                              • Launch readiness
                                              ↓
                              Problem attributor pinpoints root cause:
                              Creative? App Store listing? Retention?
                              Monetization design? UA strategy?
                                              ↓
                              Output: Verdict + Root cause + Next 3 actions
                                      + Benchmark comparison
```

Powered by your LLM of choice — **bring your own API key** (Claude, OpenAI, or Gemini).

---

## Quick Start

```bash
# Clone the repo
git clone https://github.com/KaiGameBiz/GameLaunchAI.git
cd GameLaunchAI

# Install dependencies
pip install -r requirements.txt

# Set your API key
export ANTHROPIC_API_KEY=your_key_here
# or: export OPENAI_API_KEY=your_key_here

# Run a diagnosis
python diagnose.py
```

> 🚧 **Under active development** — Star this repo to follow progress!

---

## Example Output

```
═══════════════════════════════════════════════════
🚦 VERDICT: CAUTION
═══════════════════════════════════════════════════

📊 DIAGNOSIS SUMMARY
Your casual puzzle game is in soft launch (Philippines).
D1 retention (32%) is below the casual baseline (35-45%).
ARPDAU ($0.035) is in the low range for IAA-only casual.

🔍 ROOT CAUSE: RETENTION
Your D1 is the bottleneck. Improving first-session experience
will have cascading positive effects on D7, monetization,
and UA efficiency.

Confidence: HIGH (sufficient data provided)

📋 NEXT 3 ACTIONS

1. Redesign first 5 levels to reduce early churn
   Why: 68% of churned users drop before level 5
   Expected impact: D1 +5-8 points

2. Move interstitial trigger from after level 3 to after level 6
   Why: Early interstitials correlate with D1 drop in casual
   Expected impact: D1 +2-3 points, ARPDAU -$0.002 (net positive)

3. Test 2 new creatives showing actual gameplay (not cinematic)
   Why: Gameplay creatives attract higher-intent users
   Expected impact: CPI may rise 10% but D1 improves 15%+

⚠️ DO NOT:
- Do NOT increase UA spend until D1 > 35%
- Do NOT add more ad placements to compensate for low ARPDAU

📊 BENCHMARKS
Your D1:  32%    → Casual baseline: 35-45%  ⚠️ Below
Your D7:  11%    → Casual baseline: 12-20%  ⚠️ Low end
Your CPI: $0.28  → PH casual avg:  $0.15-0.40  ✅ Normal
Your ARPDAU: $0.035 → IAA casual avg: $0.03-0.08  ✅ Normal range

📊 Benchmarks: Basic (3 genres × 3 regions)
   Pro: 12+ genres × 15+ regions, updated quarterly
   → gamelaunchai.com/pro
═══════════════════════════════════════════════════
Powered by GameLaunchAI | @KaiGameBiz
═══════════════════════════════════════════════════
```

---

## Roadmap

### MVP (current focus)
- [x] Market research & pain point analysis (47 signals from r/gamedev)
- [x] User persona definition & MVP scoping
- [ ] UA Viability Check agent
- [ ] Monetization Health Check agent (IAA + IAP + hybrid)
- [ ] Soft Launch Readiness agent
- [ ] Problem Attribution engine
- [ ] CLI tool
- [ ] Web demo

### V2 (after MVP validation)
- [ ] Market Fit Analysis (which GEOs to prioritize)
- [ ] Deal Analyzer (self-publish vs. publisher ROI math)
- [ ] Launch Checklist (standardized pre-launch QA)
- [ ] App Store listing localization QA
- [ ] MCP server (Claude Desktop / Cursor integration)
- [ ] Revenue prediction model
- [ ] Diagnosis history & progress tracking

---

## Tech Stack

| Layer | Tool | Why |
|-------|------|-----|
| Agent framework | CrewAI | Multi-agent orchestration, Python-native |
| Backend | Python + FastAPI | Richest AI ecosystem |
| Frontend | React + Next.js + Tailwind | Best AI code generation support |
| LLM | Claude / OpenAI / Gemini | User's choice, bring your own key |
| Deploy | Vercel + Railway | Free tier available |
| Protocol | MCP (planned) | Agent ecosystem integration |

---

## Why Open Source?

Because the mobile game teams who need this most — solo devs and small studios with $3K budgets — **can't afford** $99/month SaaS tools.

The core diagnosis engine is free. You bring your own API key, run locally, own your data. If it helps you make one better launch decision, that's worth a star.

**[Pro tier](https://gamelaunchai.com)** (coming soon): Expert-tuned prompts with granular industry benchmarks, full IAP/hybrid analysis, cloud API, and 1-on-1 advisory with a mobile game marketing professional.

---

## Contributing

Contributions welcome! Especially valuable:

- **Mobile game benchmark data** (anonymized) — help make diagnoses more accurate
- **Diagnosis rules** from real launch experience — "when X happens, the root cause is usually Y"
- **Bug reports** from actual mobile game projects
- **Translations** for the web demo

See [CONTRIBUTING.md](CONTRIBUTING.md) for guidelines.

---

## License

MIT License — free for personal and commercial use.

---

<a id="中文"></a>

## 中文

### GameLaunchAI 是什么？

专注于**移动游戏**的发行决策诊断工具。

**在你花第一笔买量预算之前，AI帮你诊断问题、判断go/no-go、告诉你下一步该做什么。**

### 三个核心诊断

🎯 **买量可行性诊断** — 这笔预算该不该花？先测什么？在哪个市场测？

💊 **变现健康度诊断** — 覆盖移动游戏三大变现支柱：
- **IAA诊断**：广告位健康度、留存影响、reward经济平衡、eCPM对标
- **IAP诊断**：付费项目充足性、转化漏斗、收入增长合理性
- **混合变现诊断**：IAP/IAA是否互相蚕食、最优变现组合推荐

🚦 **Soft Launch准入诊断** — 数据够不够进下一阶段？该修产品还是继续测？

### 每次诊断输出

- ✅ 明确的 **go / no-go 结论**
- 🔍 **问题归因**：创意、商店页、留存、变现设计、还是买量策略？
- 📋 **下一步3个具体动作**（可执行的步骤，不是空话）
- 📊 **行业基准对比**（你的数据 vs 同品类同地区基准）

### 目标用户

专为移动游戏小团队设计：
- Solo开发者和小团队（1-5人），做休闲/益智/放置类F2P手游
- 准备soft launch的F2P团队（5-20人），需要数据驱动的go/no-go判断

### 进度

🚧 **正在开发中** — Star 这个项目，关注进展！

---

<div align="center">

**Built by [Kai](https://twitter.com/KaiGameBiz)** — a mobile game marketer who got tired of watching small teams waste their launch budget.

*Not a coder. Just someone who knows where mobile games go wrong — and built an AI tool to help.*

</div>
