Waht I learned:
I built a four-stage Football Intelligence Hub powered by a real data workbook containing historical World Cup performance, live 2026 group stage results through 17 June, contender form scores, and player ratings. 
Stage 0 captures the user's knowledge level and adapts every output that follows. Stage 1 delivers an AI prediction report — winner, runner-up, and dark horse — each with a confidence score, supporting evidence pulled directly from the data, and identified risks. 
Stage 2 runs a personalised Football IQ Quiz, grades a Football Awareness Score out of 100, and assigns a fan classification. Stage 3 is a 12-question personality assessment that computes Messi and Ronaldo compatibility percentages, assigns a football personality archetype, and makes four tailored recommendations. 
A final profile card consolidates all outputs. I also debugged three logic failures after the first build — a quiz grading error that marked every answer wrong, a token limit that silently truncated Stage 1 JSON, and a DOM selection loop that used the wrong reference.

What I learned
The most instructive moment was the quiz bug. The API returned correct answers as letters — A, B, C, D — and the code searched for those letters inside an array of full text strings. 
indexOf("A") in an array of sentences always returns -1. Every answer was wrong. The score was always zero. 
The build appeared to run but produced completely invalid results with no error message. That is the category of failure that is hardest to catch: the system works, the data flows, but the output is silently wrong. 
Embedding the workbook as context in the prompt also reinforced something I already believed — the same model produces generic analysis with an empty prompt and specific, evidence-referenced outputs when the data is properly structured inside it. 
The model does not improve; the prompt quality does.
