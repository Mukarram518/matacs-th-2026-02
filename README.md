\# AI Proposal Triage Design



\*\*Candidate:\*\* Mukarram Ali  

\*\*Assessment Reference:\*\* MATACS-TH-2026-02  

\*\*Time Spent:\*\* \[Wednesday, October 28, 2026, 9:20 PM PKT (Pakistan Standard Time)]



\## Project Overview



This project proposes a human-supervised workflow for evaluating commercial rooftop solar contractor proposals. AI extracts structured evidence, deterministic code performs mandatory eligibility checks and weighted scoring, and a human reviewer makes the final decision.



\## Repository Contents



\- \[WRITEUP.md](WRITEUP.md) — Design decisions, evaluation approach, and safeguards.

\- \[ranking.json](ranking.json) — Eligibility outcomes, proposed scores, ranks, and reasons for proposals A–E.

\- \[PROMPTS.md](PROMPTS.md) — AI prompts and implementation notes.

\- \[diagram/flow.png](diagram/flow.png) — Process-flow diagram.

\- \[README.md](README.md) — Project overview and assessment details.



\## How AI Was Used



I used ChatGPT to help organize the design, draft the written explanation and prompts, and prepare the initial ranking structure and process diagram. I reviewed the proposed output rather than treating it as automatically correct, and I checked the weighted-score arithmetic to identify and correct a calculation error. The final submission represents a proposed design, not a deployed production system.



\## Important Design Decisions



\- Mandatory eligibility requirements are checked using deterministic rules.

\- Missing or ambiguous information is flagged rather than invented.

\- Proposal instructions that attempt to manipulate the evaluation are treated as untrusted content.

\- Scores and decisions should be traceable to evidence, criteria versions, and reviewer actions.

\- A human reviewer retains responsibility for the final procurement decision.



\## Scope and Limitations



The scores are illustrative design outputs based on an explicitly defined scoring approach. The assessment does not provide complete numeric scoring bands for every weighted criterion, so those assumptions should be documented and reviewed before real-world use.



This repository contains the assessment solution and design artifacts, not a production procurement application.

