Build a Personal Life Analysis Consultant
Learn structured report generation with Claude

1. Objective outcome:
Complex reports require structured data collection, multi-step reasoning, and organized presentation. Today you'll learn how Claude can transform raw inputs into comprehensive reports that combine analysis, forecasting, and actionable recommendations.

2. What I Built

DadOps is a single-file mobile-first web application for expectant fathers — specifically designed for the UAE and South Africa markets.

The core problem it solves: expectant dads feel helpless because they cannot grow or deliver a baby. Expectant mothers feel overwhelmed because their partners do not know what to do. DadOps gives dads a structured, actionable system for everything they can control.

3. What I Learned
The initial prompt followed a structured architecture: Role, Context, Instructions, Format, and Structure. Each layer directed Claude to draw from a specific domain — application development, logistics planning, and predictive analytics simultaneously — rather than defaulting to a generic deliverable.

The clearest demonstration of input quality driving output quality is its absence. Vague prompts produce vague results, and constant rework follows. That is an expensive and frustrating loop. Structured thinking at the outset produces structured deliverables. This build confirmed that principle at every layer: specifying a warmth-based readiness indicator produced the SVG arc gauge; specifying regional cultural context produced content that no template would have surfaced; specifying the diary format produced the highlighted, entry-capturing journal. The prompt did not ask Claude to make those decisions — it made them, and Claude executed.

The ceiling of the output was set before a single line of code was written.

Multi-step reasoning was most visible in the Build Log — the journal section that tracks how fathers are coping with one of the most significant life transitions they will experience. Claude adapted its prompts by trimester stage, called the API with contextual state (weeks remaining, region, partner name), and generated responses specific to what the father had actually written. That is genuine layered reasoning: not templated output, but organised analysis that changes based on structured input.

Human steering determined the emotional register. The first iteration used a military-operations aesthetic — rugged, but wrong in tone for an audience that is anxious, not combative. The pivot to a DIY home theme was not a cosmetic update. It was a reframe: men as builders. Expectant dads can be understood as people who construct things — homes, routines, support structures, family foundations. That single insight changed the visual language, the vocabulary throughout the app, and the underlying emotional logic of the product. Claude executed the pivot precisely once instructed. The decision to make it required a human.

The five clarifying questions compressed what would otherwise have been multiple revision cycles into one focused build. Most critically, they forced a precise answer on regional context. UAE and South Africa are not interchangeable markets. The prayer mat and Emirates ID in the hospital bag, the Aqiqah ceremony planning, and the MOI birth registration process are entirely different from the power bank for load shedding, the medical aid pre-authorisation, and the Ubuntu welcoming tradition. A single generic "Africa / Middle East" region would have diluted all of it into uselessness.

Clarifying questions are not a product limitation — they are a prompt technique. Asking Claude to interrogate the brief before building forces a requirements-gathering phase that most people skip when working with AI. In this build, five specific answers became the functional specification. The gap between the initial brief and the better output lived in those five questions.

4. Initial Prompt:
Role: You are an expert applications developer, logistics planner and predictive analytics 
expert with 15 years of experience in preparation for the arrival of a new baby.

Context: The audience are fathers to be. Expectant dads often feel helpless when it comes 
to preparation for the arrival of a new baby, they can't grow a baby, they can't deliver 
the baby, they generally feel useless. Expectant mothers often feel overwhelmed with 
everything they need before a child arrives, forgetting important things they need and 
getting frustrated that partners don't know what to do to lighten the load. But what if 
there was an application that supports expectant dads-to-be with things they can control?

Instructions: Create a MVP (mockup) of the Dads support app, let's give it a clever name. 
The app tracks all the important items needed for the birth of the baby. There will be a 
tab for advice on how to support their partner. It will be region-specific and take the 
cultural context into account.

Format: The app will be a dark/light theme that is playful (For new dads) with a rugged 
edge. There should be a tab for tracking items and a dashboard that shows the time to 
delivery with a 'readiness' indicator (Red to green in a warmth chart). There should be 
a tab to track reflections, with AI-powered guidance on providing support to dads. The 
inputs should be highlighted when clicked on and captured in a 'diary' format.

Structure: Take your time, this is an extensive project and needs step by step reasoning. 
You must pull information from validated sources for pregnancy, birth and related topics.

We will create an MVP of a 'dad support app.'
