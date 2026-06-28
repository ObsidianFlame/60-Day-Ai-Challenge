Build a Hospital Admission Readiness Simulator
Experience hospital admissions through an interactive healthcare workflow

What i built:
Day 28 is a Hospital Admission Readiness Simulator. You play the role of an Admission Coordinator and work through the full pre-admission workflow for a single patient case. 
You set up the scenario by selecting a diagnosis, admission type, PA status, and provider details. The tool validates your combination clinically before you proceed — Acute MI cannot be Observation, Elective Surgery cannot be Emergency — and tells you why in plain clinical language, not just an error flag. 
From there you work through PA resolution, insurance verification, documentation upload, bed assignment, consent, physician orders, and patient arrival coordination. Each action feeds a live consequence log explaining what that step unlocks downstream. 
A care coordination panel shows all five team members — Attending, Case Manager, Nursing, Utilization Review, and Discharge Planner — and activates each one as the relevant action is taken. Utilization Review specifically names concurrent review, denial risk identification, InterQual, and Milligan. 
The score is weighted across six components with Prior Auth carrying the heaviest load at 25%, and a Denied PA combined with ICU admission creates a hard ceiling that administrative tasks alone cannot break. The final decision requires 90% readiness to admit.
