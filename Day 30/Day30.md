Build a Supply Chain Optimizer
Optimize an existing supply chain like a real operations leader

What I built:
Today I built a Supply Chain Optimizer that teaches healthcare supply chain fundamentals through hands-on decision making rather than static slides. 
You pick a healthcare sub-sector (pharma, medical devices, PPE, diagnostics, or vaccines), get assigned a randomly generated company, then work through five real operational decisions: sourcing, factory location, warehouse strategy, transportation, and inventory levels. 
Every choice comes with a plain-English explanation of the concept, why it matters, and a healthcare-specific consequence, things like cold chain exposure, batch recalls, or regulatory audit complexity. 
Five live metrics update after each decision: cost efficiency, delivery speed, risk resilience, customer satisfaction, and sustainability, all displayed on a vitals-monitor style header with an animated ECG line running behind it. 
An illustrated supply chain scene builds itself in real time as you decide, supplier through to patient. The build also maps every decision to the UN's Sustainable Development Goals, including the moments where two goals pull against each other, like high safety stock supporting patient access while working against waste reduction on perishable products. 
It closes with a dynamic scorecard: overall score, strengths, weaknesses, biggest risk, and three improvement suggestions generated from your actual weak points rather than generic tips.

What I learned:
Going in, I assumed a centralised warehouse hub would be the most efficient and resilient choice, one big facility, tighter control, lower overhead. The simulator proved that wrong. Regional hubs, smaller and closer to the end user, came out ahead on delivery speed and customer satisfaction, and improved risk resilience too, despite carrying a real cost efficiency penalty. 
That's the trade-off: centralisation looks efficient on a spreadsheet, but it concentrates risk and adds distance to the people actually waiting on the product. In healthcare, it's the gap between a hospital restocking on time or not. 
The deeper lesson is that resilience and customer experience often have to be bought, and the real skill isn't avoiding that cost, it's deciding where it's worth paying it to protect sustainable cash flow, the thing that actually keeps an organisation alive long enough to make its next decision. 
This challenge also confirmed that building tools in a domain I actually know, healthcare, surfaces sharper lessons than a generic exercise would; the trade-offs feel consequential rather than theoretical. And on the build side, today reinforced that I need explicit checkpoints in my prompting going forward: chain-of-thought structure, multiple passes, and having the AI verify and fix its own code before I treat anything as shippable.
