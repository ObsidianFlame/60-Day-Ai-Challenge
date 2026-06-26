Build a Prior Authorization Workflow Simulator
Learn healthcare workflows through interactive gameplay

What I built:
I built a Prior Authorization Workflow Simulator — a fully offline, drag-and-drop kanban game that teaches the US healthcare PA process by making you live it. You drag patient case cards through three lanes: Patient, Provider, and Payer. You collect documents, submit to the insurer, and wait for a decision. 
If it gets denied — and sometimes it does — a randomised denial pathway activates. 
Simple, Medium, or Complex. Peer-to-peer review. Formal appeal. External IRO review. Each stage has a two-phase reveal: read the clinical context, then hit "Conduct Review" to find out if the denial holds. 
Fourteen years working in hospitals taught me how much time clinicians lose to this process. This simulation gives people a way to understand it in ten minutes.

What I learned:
Prior Authorization looks broken from the outside. Once you model it, you realise it is broken by design. Only 11.7% of denied claims are ever appealed, and 81.7% of those appeals succeed. 
The system does not fail despite the friction. It succeeds because of it. Building the randomised denial depth taught me that uncertainty is not a bug in the gameplay — it is the most honest thing the simulator does. And the bug that broke the build gave me the most transferable lesson of the day: correct components do not guarantee a working system.
The failure was not inside the code. It was between two pieces of code that never spoke to each other. That shows up in clinical handoffs and project governance just as often as it shows up in software. Check the boundaries. Not just the parts.
