Claude can act as a data analyst capable of processing CSV datasets, calculating business metrics, generating visualizations, and building complete HTML dashboards. 
This workflow mirrors real-world analytics projects used in consulting, finance, operations, and business intelligence.

What I built
On Day 17 of my 60 Days of Claude AI Coding Challenge, I built a fleet operations dashboard for a fictional logistics company running 52 vehicles across five fuel types. 
Starting from a raw CSV, I worked with Claude to enrich the dataset to 24 columns — adding vehicle lifespan, replacement costs, TCO components, emissions bands, utilisation rates, and a composite risk index — before building a full four-tab interactive HTML dashboard from it. 
The dashboard covers everything from KPI cards and SVG charts to a replacement priority queue, an operational intelligence matrix ranking each fuel type across five dimensions, and a Fleet Risk Index scoring all 52 vehicles from 0 to 100. 
No external chart libraries. Pure SVG, pure code.

How this can be used in the real world
Any organisation running a physical asset fleet — logistics, healthcare, construction, facilities management, government — can use this workflow to move from raw vehicle data to a live operations dashboard in a single session. 

Prompts:
- To make the dataset more complex:
Day 17- Vehicle Cost & Fuel Analysis Dashboard.
The task today: Claude can act as a data analyst capable of processing CSV datasets, calculating business metrics, generating visualizations, and building complete HTML dashboards. This workflow mirrors real-world analytics projects used in consulting, finance, operations, and business intelligence.

We have been given a data set of vehical cost and fuel (attached here).
It is to create an interactive dashboard that can gauge insights as the following:
1.1. CSV Analysis: Analyze structured datasets without writing code.
1.2. Dashboard Creation: Generate complete HTML dashboards from raw data.
1.3. Business Metrics: Calculate meaningful KPIs and insights.
1.4. Visualization: Create charts and dashboards using SVG graphics.

I want to take this a step further before we begin. I want you to generate another column with the Average lifespan of each vehicle (can be arbitary between 5 and 15 years). Then add an extra column for replacement cost for each vehicle.
The intention of this is to go beyond the basic requirements of this task to analyse vehicle cost and fuel analysis. I want to include the  lifespan and replacement cost for each vehicle to create a 'fleet management database' related to operations management. Add a column for short-, medium- and long-haul vehicles (can be arbitrarily assigned to the above dataset)
What else would increase the complexity of this dataset to get meaningful insights from the above objectives?

NOTE: We are only creating a complex dataset currently, the actual interactive dashboard comes next.

You may ask as many clarifying questions as you need. 
Is this clear enough?

Add: 
Financial Layer:
Remaining Lifespan yrs
Insurance Annual INR
Total Cost of Ownership INR

Operational Layer:
Vehicle Type
Utilisation Rate pct
Route Type

ESG & Compliance Layer
Emissions band
Replacement Priority
