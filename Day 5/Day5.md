Context Engineering is the practice of providing relevant information, constraints, background, goals, and user-specific details to AI before asking it to perform a task. The quality of context often matters more than the prompt itself.
Anthropic views Context engineering as the progression of Prompt engineering to achieve optimal outcomes.
It is the strategy of using Ai in the most token-optimized way possible.
While Prompt engineering focuses on the best way to write a prompt while context engineering focuses on maximising the context state, utilising efficiencies across multiple rounds of inference (including tools, Model Context Protocols [MCPs], memory etc.)
Context Prompting is an iterative process that focuses on curating what will go into the context window for an evolving landscape.

What I did:
Created 2 distinct 30 day learning plans, using Prompt templates, with some of my own additions and some unique brand guidelines to make it closer to my personal brand.

Prompts:
PROMPT A (WITHOUT CONTEXT)

Create a 30-day learning roadmap.

Include:
- Weekly milestones
- Daily tasks
- Resources
- Projects
- Final outcome

Make it practical and beginner-friendly.

━━━━━━━━━━━━━━━━━━━━━━

PROMPT B (WITH CONTEXT)

Create a 30-day learning roadmap.

Context:
- Current Situation: [Student/Professional/Freelancer]
- Current Skills: [Add Skills]
- Goal: [Target Goal]
- Available Time: [Hours per Day]
- Experience Level: [Beginner/Intermediate]
- Preferred Learning Style: [Videos/Projects/Reading]

Include:
- Weekly milestones
- Daily tasks
- Resources
- Projects
- Final outcome

Make it practical and beginner-friendly.
   
Context rot occurs as LLM's struggle to recall information the longer a context becomes.
LLM's are set up in a predictive manner, so as that each token attends to the previous token, creating an exponential drain on the available 'attention span' of AI.

Key learnings:
AI loses context the longer a chat/interaction progresses, leading to degradation and hallucinations.
We must be aware that this 'attention' from LLM's is a finite resource that needs to be managed effectively in order to get the output we want.
It's all based on token-usage, by curating the context and managing the length of conversations, we can essentially get better outputs.

It's especially important when building AI agents, as they have multi-step, iterative decision-making processes that need context to create effective outputs.
Prompts must be specific enough to guide behaviour, but flexible enough to provide the model with strong heuristics to guide behaviour.
Aim for the minimal set of informetion that produce the desired behaviour. Iterative testing is the name of the game, get started with relatively clear instructions, then iterate as you go along to get the desired output.

Another interesting lesson: If an AI engineer cannot confidently say which tool should be used in which context, it is impossible for an AI agent to make such a decision.
Prompters/Coders/Engineers should be clear on which tools they use in terms of functionality, with as minimal overlap as possible.
You need to use example cases for AI to understand what your desired output is.

A simple definition for agents: LLMs autonomously using tools in a loop.
Agents mirror human cognition in the sense that they don't memorise the entire context, they use external organisation to retrieve information when needed.
How you name files and folders is vital, it helps the Agent understand the context without loading all the information. Structured correctly, you can have agents maximise token-efficiency by utilising only the information they need, when they need it.

Remember: "do the simplest thing that works" 

Techniques that maximise Agent's usage of context:  compaction, structured note-taking, and multi-agent architectures.
  - Compaction: taking a conversation nearing the context window limit, summarizing its contents, and reinitiating a new context window with the summary. Start by maximizing recall to ensure your compaction prompt captures every relevant piece of information from the trace, then iterate to improve precision by eliminating superfluous content.
  - Structured Note-taking: Structured note-taking, or agentic memory, is a technique where the agent regularly writes notes persisted to memory outside of the context window.
  - Multi-agent Architecture: Rather than one agent attempting to maintain state across an entire project, specialized sub-agents can handle focused tasks with clean context windows. 

Compaction maintains conversational flow for tasks requiring extensive back-and-forth;
Note-taking excels for iterative development with clear milestones;
Multi-agent architectures handle complex research and analysis where parallel exploration pays dividends.

the guiding principle remains the same: find the smallest set of high-signal tokens that maximize the likelihood of your desired outcome.

Compare both outputs and identify:
1. Which roadmap feels more personalized: The context-prompted roadmap feels far more personalised, although an interesting outcome was that the original vague prompt produced a '30 day learning tracker' on 'anything' I wanted to learn, however it consumed significant context and was extremely token heavy. However by utilising Context prompting, the context use and token utilisation was far lower (42% compared to 18%) according to rough estimates.
2. Which roadmap would you actually follow? I would follow the context-prompted output, it's much more specific and personalised to my unique situation.
3. What role did context play in improving the result? Context ensured that tokens-usage was far lower than the original prompt, as well as the context window usage was far lower, something i did not expect to produce an output that was far more complex.
