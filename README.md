<div align="center">

# 🎮 GameLaunchAI

### Launch diagnosis for mobile game teams.
### Know what's broken. Know what to fix first.

**Before you spend your first dollar on UA — get a diagnosis, not a report.**

[Demo](https://gamelaunchai.vercel.app) · [Documentation](#how-it-works) · [中文文档](#中文)

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](https://opensource.org/licenses/MIT)
[![MCP Compatible](https://img.shields.io/badge/MCP-Compatible-purple.svg)](#mcp-support)

</div>

---

## The Problem

You built a mobile game. Now what?

- You have $3,000 for UA. Is that a **test budget** or a **launch budget**? (Hint: it matters.)
- Your D1 retention is 32%. Should you **buy more traffic** or **fix the product first**?
- Your rewarded ads bring in $0.04 ARPDAU. Is that **good for your genre**, or are you **leaving money on the table**?
- You're in soft launch. **Is it time to scale, or time to stop?**

80% of mobile games on Steam earn less than $5,000. Not because the games are bad — because the **launch decisions** are wrong.

**GameLaunchAI doesn't give you a 30-page report. It gives you a verdict and your next 3 actions.**

---

## What It Does

GameLaunchAI is an open-source AI diagnosis tool for mobile game teams. Input your game data, get a clear **go / no-go decision** and **specific next steps**.

### Three core diagnoses:

🎯 **UA Viability Check** — Should you spend that budget?
> Input your game type, market, budget, and early metrics. Get back: is this a measurement budget or a launch budget? What should you test first? Should you keep spending or stop?

💊 **Monetization Sanity Check** — Are your ads killing your game?
> Input your ad placements, reward design, retention data, and ratings. Get back: which ad slots are hurting retention, which rewards are getting abused, and whether you need rewarded-only, hybrid, or ad-free pack.

🚦 **Soft Launch Readiness** — Go or no-go?
> Input your stage, GEO, D1/D7 retention, revenue structure, and CPI. Get back: have you hit the gates for the next phase? Should you fix the product or keep testing UA? Is it time to scale?

### Every diagnosis includes:

- ✅ **Go / No-go verdict** — A clear decision, not a hedge
- 🔍 **Root cause attribution** — Is the problem in creative, store page, retention, monetization, or UA strategy?
- 📋 **Next 3 actions** — Specific, executable steps. Not "improve your retention." More like "remove the forced interstitial after level 3 and retest D1 over 5 days."

---

## Who It's For

**Solo devs & small teams (1-5 people)** building casual, puzzle, idle, or light F2P mobile games with budgets under $10K. You know you need to spend money on UA — you just don't know if it's worth it yet.

**Small F2P teams (5-20 people)** preparing for soft launch. You're looking at retention curves and CPI numbers and trying to figure out: fix the product, or keep testing?

---

## How It Works

```
You describe your game     →  Stage classifier puts you in
and enter your metrics         pre-launch / beta / soft launch / live
                                        ↓
                           3 specialized AI agents diagnose:
                           • UA viability
                           • Monetization health  
                           • Launch readiness
                                        ↓
                           Problem attributor identifies root cause:
                           Creative? Store page? Retention? 
                           Monetization? UA strategy?
                                        ↓
                           Output: Verdict + Root cause + Next 3 actions
```

The AI agents are powered by your LLM of choice — **bring your own API key** (Claude, OpenAI, or Gemini).

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

## Roadmap

### MVP (current focus)
- [x] Product research & pain point analysis
- [ ] UA Viability Check agent
- [ ] Monetization Sanity Check agent
- [ ] Soft Launch Readiness agent
- [ ] Problem Attribution engine
- [ ] CLI tool
- [ ] Web demo

### V2 (after MVP validation)
- [ ] Market Fit Analysis (which GEOs to prioritize)
- [ ] Deal Analyzer (self-publish vs. publisher ROI comparison)
- [ ] Launch Checklist (standardized pre-launch QA)
- [ ] MCP server support (Claude Desktop, Cursor integration)
- [ ] Revenue prediction model
- [ ] Diagnosis history & progress tracking

---

## Tech Stack

| Layer | Tool | Why |
|-------|------|-----|
| Agent framework | CrewAI | Multi-agent orchestration, Python-native |
| Backend | Python + FastAPI | AI ecosystem, easy deployment |
| Frontend | React + Next.js + Tailwind | Best AI code generation support |
| LLM | Claude / OpenAI / Gemini | User's choice, bring your own key |
| Deploy | Vercel + Railway | Free tier available |
| Protocol | MCP compatible (planned) | Works with AI agent ecosystem |

---

## Why Open Source?

Because indie devs and small teams **can't afford** expensive consulting or SaaS tools. If your game earns less than $5,000 (80% of mobile games), you shouldn't have to pay $99/month for launch advice.

The core diagnosis engine is free and open source. You bring your own LLM API key, you run it locally, you own your data.

**[Pro tier](https://gamelaunchai.com)** (coming soon): Expert-tuned prompts with real industry benchmarks, cloud API, and 1-on-1 advisory sessions with a game marketing professional.

---

## MCP Support

> 🔜 Coming in V2

GameLaunchAI will be available as an MCP server, so AI assistants like Claude Desktop, Cursor, and OpenClaw can run diagnoses directly:

*"Hey Claude, use GameLaunchAI to check if my puzzle game is ready for soft launch. D1 retention is 38%, D7 is 12%, CPI in Philippines is $0.35."*

---

## Contributing

Contributions welcome! Whether you're a game developer with industry insights or a coder who wants to improve the diagnosis logic.

See [CONTRIBUTING.md](CONTRIBUTING.md) for guidelines.

**Especially valuable contributions:**
- Mobile game benchmark data (anonymized)
- New diagnosis rules based on real launch experience
- Bug reports from actual game projects
- Translations for the web demo

---

## License

MIT License — free for personal and commercial use.

---

<a id="中文"></a>

## 中文

### GameLaunchAI 是什么？

移动游戏发行决策诊断工具。**在你花第一笔买量预算之前，AI帮你诊断问题、判断go/no-go、告诉你下一步该做什么。**

不是行业资讯产品。不是BI看板。不是广告平台。
而是一个 **launch-readiness 与 monetization 诊断工具**。

### 三个核心诊断

🎯 **买量可行性诊断** — 这笔预算该不该花？先测什么？
💊 **变现健康度诊断** — 哪些广告位在伤害留存？reward设计会不会被滥用？
🚦 **Soft Launch准入诊断** — 数据够不够进下一阶段？该修产品还是继续测？

### 每次诊断输出

- ✅ 明确的 **go / no-go 结论**
- 🔍 **问题归因**：问题出在创意、商店页、留存、变现还是买量策略？
- 📋 **下一步3个具体动作**（不是空话，是可执行的步骤）

### 目标用户

- Solo开发者和小团队（1-5人），做休闲/益智/放置类手游，预算有限
- 准备soft launch的小型F2P团队（5-20人），需要判断何时继续、何时停止

### 使用方式

开源免费，用户自带LLM API Key在本地运行。

---

### 进度

🚧 **正在开发中** — Star 这个项目，关注进展！

---

<div align="center">

**Built by [Kai](https://twitter.com/KaiGameBiz)** — a game marketer who got tired of watching great games fail at launch.

*Not a coder. Not a data scientist. Just someone who knows where mobile games go wrong — and built an AI tool to help.*

</div>
