What I built:
A five-tab JCI Accreditation Readiness Intelligence Dashboard built entirely on synthetic data — no real patient records, no clinical databases, fully compliant with UAE Federal Law No. 2 of 2019 and UAE PDPL. 
The hospital in the build (Meridian Medical Centre) is fictitious. Every data point is labelled [SYNTHETIC].
The dashboard accepts a declared hospital operational profile and scores 14 JCI chapters across 486 measurable elements, cross-referencing every finding against equivalent DHA and DOH regulatory standards to produce a dual-framework gap map — something no off-the-shelf accreditation tool currently does for the GCC market.
Built in one session: two animated SVG score gauges (JCI Readiness 67/100, UAE Compliance 73/100), a chapter readiness heatmap, a six-axis quality radar, a standards priority ranking, a 10-finding critical gap register with DHA/DOH crosswalk references, a 14-chapter × 12-department compliance matrix, a synthetic hospital digital twin profile, and a live improvement simulator where dragging sliders for the three highest-leverage chapters updates the projected JCI score and months-to-readiness in real time. 
Plus dark/light mode, Notion integration, and a full synthetic data package written to the Business Ideas database before a single line of HTML was written.

What I learned:
The prompt template is a reusable architecture. Scores, heatmaps, rankings, matrices, simulators, final verdict. Swap clinical vocabulary for digital vocabulary and it maps almost perfectly. That is a methodology worth saving, not just a build worth sharing.
Synthetic data forced better thinking. Because real patient records were off the table, every number had to be justified before it was placed. Separating Facts from Estimates is not a disclaimer. It is a discipline. A dashboard that shows its working is more credible than one that does not.
The WOW insight was the most useful output of the whole session. A 27-point gap between GLD (80) and MMU (53) tells you something specific: leadership aligned, ward-level execution not. That is the kind of pattern a quality team pays a consultant to find. Claude found it by analysing a data structure, not a database.

Prompt:
Build a JCI Accreditation Readiness Intelligence Dashboard for a UAE hospital. 
Input: a declared operational profile. Build a synthetic database for a hypothetical hospital in the GCC that wants to be accredited by the JCI.
Output: dual scoring (JCI Readiness and UAE Regulatory Compliance, 0–100), a chapter readiness heatmap, a gap register cross-referenced against DHA/DOH standards, and a live improvement simulator. 
All data synthetic. Label [SYNTHETIC] throughout. No real patient or clinical records.
