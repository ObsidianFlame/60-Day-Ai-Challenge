What I built:
For Day 27 of the 60 Day Claude AI Coding Challenge, I built a fully offline, single-file Prior Authorization Story Simulator. 
It follows two characters — Patient P and Priya, a Healthcare Operations Specialist — through all eight stages of a real PA case: from diagnosis and submission, through denial and appeal, to final approval. 
The simulator runs entirely in the browser with no API calls and no external dependencies. It includes 24 intermediate-level quiz questions (three per scene, with four options each), a live Operations Dashboard tracking days elapsed, staff hours, denial risk, and cumulative admin cost, and a ghost timeline that shows from Scene 1 what the case could have looked like with complete documentation from the start. 
After completing all eight scenes, the learner can replay the full story as Priya — making the HCA decisions themselves and seeing the operational consequences of wrong choices. 

What I learned:
The inclusion of a ghost timeline was Critical Path Method made visible. CPM is a core project management principle, the idea that in any sequence of dependent tasks, the path with zero float determines how long the whole thing takes. 
Modelling the ideal PA journey alongside the actual one forced me to calculate, scene by scene, exactly which delays were structural and which were entirely preventable. 
Poor documentation at submission does not cost a day, it costs nine. The colour coding reinforced this as a feedback loop: red means you are off the critical path, not just behind schedule.
Building the Replay as Priya mode was an exercise in Design Thinking. Once the learner sits in the HCA's seat and makes the decisions, the patient's 13-day wait stops being a statistic and becomes a consequence of their own choices. 
That shift in perspective is the entire point. Pain points only become actionable when the person responsible for the process has actually felt them from the other side.
Some issues only appeared at runtime, when a condition was met. I see this in business constantly. Processes that look clean in a policy document contain decision points that were never written down and exist only in someone's head. No audit log. No version control. No way to reconstruct what happened or make an informed decision about what to change. The class was hidden in the code the same way the decision is hidden in the workflow.
