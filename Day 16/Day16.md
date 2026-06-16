What I Built

A Stock Fundamental Research Skill — a SKILL.md file that gives Claude a complete financial analyst methodology — tested live against three JSE-listed companies across two output modes: Quick Take (single stock analysis) and Compare (multi-stock peer comparison).

echnical Stack


SKILL.md — stock-fundamental-research encoding methodology, output modes, data source hierarchy, interpretation rules, mandatory constraints
Data sources — StockAnalysis.com (S&P Global Market Intelligence), afx.kwayisi.org, TradingView, Wikipedia
Chart.js (v4.4.1 via cdnjs) — interactive grouped bar charts, 52W price range indicator
Canva MCP connector — generate-design → create-from-candidate → export-design (PNG, 1080×1350px)
Tools — web_search, web_fetch, visualize:show_widget, message_compose_v1, Canva:generate-design, Canva:export-design

What I Learned — 3 Reflective Questions

Mapped to the Day 16 objectives: skill architecture, live data research, peer comparison analysis, and MCP tool integration.


1. How did working with a structured skill file change the quality of output compared to how you'd normally prompt Claude for research?

(Objective: Skill Architecture — how a SKILL.md encodes methodology and changes workflow quality)

The output was cleaner, more consistent, and required significantly less friction on repeat runs. Working through a one-off research prompt requires explaining context, format, rules, and scope every single time. The skill file made all of those decisions once — and then applied them reliably across both the Quick Take on Dis-Chem and the 3-way comparison with Clicks and Shoprite — without restating requirements between sessions.

The deeper shift was not in the output quality, but in the thinking required before it. The structured skill file forced a precise reckoning with what output was actually needed: the context it needed to serve, the method of reasoning that should produce it, and the sequence it should follow. That pre-thinking is the step most people skip when working with AI, and it is precisely where the quality ceiling is set. The skill is essentially a requirements specification written once, in advance. Every subsequent run inherits that specification automatically.

The practical result was a workflow that could run repeatedly — looking at individual stock metrics, then comparing fundamentals across organisations — that produced consistent, structured, usable outputs each time without restarting from scratch. That is the definition of a repeatable process. The skill file made it one.


2. Did the CLS finding — fundamentals intact despite a 35% price drop — shift how you think about using AI for research in a domain where you already have prior knowledge?

(Objective: Live Data Research — AI-generated analysis intersecting with prior knowledge and existing opinion)

It shifts the analysis in a meaningful way. Media coverage follows price action — a falling stock generates negative narrative, and that narrative reinforces the price move in a feedback loop that a retail investor can easily be caught inside. The skill-structured approach cuts directly to the fundamentals: P/E, FCF, ROE, ROCE, HEPS guidance — the numbers that an equity analyst would start with before forming any view at all.

The Clicks signal illustrates this clearly. A –35% price move reads as bad news in any headline. The fundamentals read differently: 47% ROE, R4.3B FCF, HEPS guidance of 4–9%, RSI of 28.93. Those are not the numbers of a broken business — they are the numbers of a de-rated one. Whether that represents opportunity or a value trap is a judgment call that requires human expertise. But the skill surfaced the divergence between narrative and fundamentals rapidly and clearly.

The most important caveat is also the most significant risk. The quality of the insight is bounded entirely by the accuracy of the base knowledge embedded in the skill. If the interpretation rules are miscalibrated — if what constitutes "strong" ROE is set at the wrong threshold, or the FCF interpretation is inverted — the skill will surface false signals with exactly the same confidence as real ones. Domain expertise does not disappear when using AI for research; it migrates upstream into the design of the skill itself. The biggest risk is uncovering insights that do not exist because the knowledge used to build the skill was inaccurate or incomplete.


3. What did the Canva MCP workflow reveal about where AI tool integrations actually are right now, and how would you design around those gaps?

(Objective: MCP Tool Integration — real-world reliability and resilient AI workflow design)

The Canva integration surfaced the current reality of MCP tool connections precisely: the promise is seamless, the execution requires active management. The workflow encountered 403 forbidden errors, an account mismatch between the MCP-authenticated Canva session and the browser login, and export links that expired within hours of generation. What appeared to be a one-step workflow — generate infographic, access it — required three diagnostic loops and a workaround: exporting the PNG directly through the Canva API rather than relying on the saved design URL.

What this reveals is not a reason to avoid MCP integrations, but a reason to design around their failure modes before shipping. AI tool integrations need perfect routing and continuous monitoring. A single change — an authentication token rotating, an account scope shifting, a generated link expiring — can break a productivity flow entirely and trigger rework cycles that cost more time than the automation saved.

The correct design response is to treat every MCP integration exactly like a critical dependency in a production system: define what failure looks like at each step, build a fallback path for each failure mode, and test the fallback before it is needed — not after the primary path has broken. In this case, the fallback was direct PNG export, which worked immediately once the primary URL-access path failed. A decision and workflow matrix approach — where different paths converge on the same output regardless of which step fails — is the right architecture for any AI workflow that depends on external tool integrations. Resilience is a design requirement, not an afterthought.
