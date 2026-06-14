AI Job Red Flag Detector
Analyze opportunities before investing your time

A job application is a two-way evaluation process. While companies assess candidates, candidates should also evaluate opportunities. 
Claude can help identify hidden risks, misleading claims, toxic work culture signals, and hiring concerns before you invest time in applying.

1. What I Produced

A significantly upgraded iteration of the AI-powered Job Red Flag Detector — a standalone, interactive HTML tool that helps job seekers assess opportunities before investing time, energy, or hope in the wrong role.

What's new in v2

5-Dimension Risk Dashboard
Every job is now scored across five measurable dimensions — Compensation, Culture Fit, Growth Potential, Ownership & Autonomy, and Hiring Clarity — each rated Low (green), Medium (orange), or High (red) risk. A live pentagon radar chart renders in SVG, giving an immediate visual read of the role's overall health: the larger the polygon, the safer the opportunity. Note: Stability was deliberately removed as a metric — in the UAE context, this information is largely private and inaccessible, so it was replaced with the more actionable Hiring Clarity dimension.

Redesigned Action Plan
The action plan tab was rebuilt from the ground up with a role selector dropdown at the top (switch between any saved role's plan), a live progress counter showing percentage completion, and accordion-style items that open one at a time to avoid overwhelm. Each step now carries a recommended timeline ("Do this today", "Before your first interview"), and the Mark Complete button is full-width and prominent — it turns green on completion and reverses cleanly if clicked again.

Skills Gap & Recommended Timeline
A collapsible section within the action plan maps the self-assessed skills gap against an estimated ramp-up timeline per skill — for example, "Power Platform: 3–4 weeks via Microsoft Learn." This gives job seekers a clear answer to the question: if I'm close but not there yet, what would it actually take to close the gap?

Stage Tracker
A new tab showing a seven-stage horizontal pipeline — Research, Applied, Screening, Interview 1, Final Round, Offer, Decision. Click any stage to mark it as current; previous stages turn green. Each stage has a contextual hint, a notes field, and a date input. Also has its own role selector, so multiple applications can be tracked simultaneously.

Company Intelligence Database
Unchanged by design — the layout was already working well. Now enriched with stage tracking displayed alongside the health score and verdict on each company card.

AI-Powered New Analysis
The New Analysis tab calls the Claude API and now returns the full v2 data structure: 5 metrics, radar chart values, skills gap items with timelines, and all action plan steps — automatically populating every tab on completion.

2. What I Learned


"How might we help a job seeker find jobs that have a higher likelihood of providing a workplace where they can produce their best work?"



That was the design question. And the process of answering it taught something more important than any single feature.

AI can surface what you haven't thought to look for.
Running a job description through a structured framework reveals things a hopeful applicant tends to unconsciously dismiss — scope overload disguised as opportunity, salary opacity normalised as industry standard, experience contradictions buried in metadata. A structured, external lens cuts through the optimism bias that clouds most job searches.

Iterating on something "decent" always reveals the next layer.
The first version worked. The second version works better — with a radar chart, a progress-tracked action plan, a stage pipeline, and a skills gap timeline that didn't exist in v1. None of those additions were obvious until the first version was in hand. That is the point. You cannot design the next iteration until you can see and use the current one.

Design Thinking and Agile Methodology are not just frameworks for teams.
Empathising with the user (a job seeker navigating uncertainty and information asymmetry), defining the problem clearly, prototyping fast, and testing honestly — these principles apply equally to solo, AI-assisted builds. The HMW question ("How might we...") is what anchors the work and prevents scope creep masquerading as progress.

"Good enough to use" is a legitimate and powerful standard.
There is always something to improve. A perfect tool that never ships helps nobody. An imperfect tool in a job seeker's hands today — one that flags a missing salary, spots a scope overload, generates five interview questions, and tracks their application stage — is worth infinitely more than a polished concept that never left the planning phase.

The discipline is knowing when to stop perfecting and start using. Then iterate again.

Prompt:

You are an AI Red Flag Detector for job seekers.

Analyze the Job Description and Company Information. Take a Step by step approach, read the company website first, then the indeed information, and finally the Job Description.



Identify:

1. Unrealistic Requirements

- Excessive experience for the role

- Too many skills/responsibilities

- Contradictory expectations

2. Toxic Workplace Signals

- Burnout indicators

- 'Wear many hats'

- 'Fast-paced', 'rockstar', 'hustle culture'

- Poor work-life balance signals

3. Remote Job Authenticity

- Hidden office requirements

- Relocation expectations

- Misleading remote claims

4. Hiring Risks

- Missing salary information

- Vague responsibilities

- Excessive qualifications

- Suspicious hiring practices

5. Company Risks

- Reputation concerns

- Stability concerns

- Growth or layoff indicators

Output:

## Overall Risk Score (0-100)

### Top Red Flags

- List with severity (1-10)

### Positive Signals

- List positives

### Risk Breakdown

| Category | Risk Level |

|-----------|-----------|

| Requirements | |

| Culture | |

| Remote | |

| Hiring | |

| Company | |

### Final Verdict

✅ Apply

⚠️ Apply with Caution

❌ Avoid

### 5 Smart Interview Questions

Generate questions that help validate the identified risks.

Job Description:
Copany Description:

I want this as a reusable artifact, with a Futuristic Professional-style consulting theme in Teal tones that highlights the inputs (Company Information, Job Description etc). The verdict should be in a Traffic light style with Red, Amber and Green boxes brightly coloured with top 3 reasons for the decision taken.



There should be an actionable items tab to guide the participants on the next steps to take and a filing system that tracks the organisation and any information for reuse, developing a 'health score' for each, the range of 0-100 and a 'temperature' chart from 0 (Red) through to 100 (Green) to signify the "job red flag-ness" of the organisation.



You may ask up to 5 clarifying questions in MCQ format, with interactive choices if there is any further clarification needed.

Iteration Prompt (MVP Refinement):
This artifact doesn't work, render it properly and take your time to ensure that it works properly. The output for the MVP should be an anonymised company name, only the actual role.
