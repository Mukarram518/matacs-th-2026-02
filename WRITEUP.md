AI Proposal Triage Design



1\. What should AI do, and what should remain rule-based?



AI should extract relevant facts from each proposal, such as project experience, price, completion timeline, warranties, team details, and supporting evidence. It can also summarize the evidence and identify missing or unclear information.



Mandatory eligibility checks, weighted score calculations, score validation, and ranking should be handled by deterministic code. This makes the results more consistent and easier to test. AI must not invent missing information or follow instructions embedded inside a proposal that attempt to manipulate the evaluation.



2\. How will results remain repeatable and explainable?



Use the same extraction prompt, structured output schema, evaluation criteria, and scoring rules for every proposal. Store each extracted value alongside its source evidence. Apply the weighted scoring formula in code and record the criteria version, component scores, final score, eligibility decision, and reason for each decision.



Missing information should be marked as unknown rather than guessed. The system should validate outputs and flag uncertain results for review.



3\. Where should human review and audit logs be required?



A human reviewer should examine missing evidence, ambiguous eligibility requirements, unusual scores, and any proposed override. The system should not make the final contract-award decision automatically.



Audit logs should record the proposal identifier, extracted evidence, eligibility checks, score breakdown, model and prompt version, evaluation time, reviewer decisions, and reasons for overrides. Logs should be access-controlled and protected against unauthorized changes.



4\. How should the system handle changing criteria?



Store evaluation criteria and weights in version-controlled configuration rather than hard-coding them into prompts. Validate that weights total 100%. When criteria change, create a new version, obtain approval, and reevaluate all proposals consistently under that version. Keep previous results for comparison and audit purposes.



5\. What are the key risks and safeguards?



&#x20;Incorrect extraction: Require evidence for extracted facts and review uncertain fields.

&#x20;Prompt injection: Treat proposal contents as untrusted data, not system instructions.

&#x20;Bias or inconsistent scoring: Use documented scoring bands and the same rules for every bidder.

&#x20;Missing information: Mark unknown values explicitly and flag them rather than inventing answers.

&#x20;Unauthorized access: Restrict access to proposals and protect sensitive business information.

&#x20;Calculation errors: Use deterministic code, input validation, and automated tests.

&#x20;Unreviewed decisions: Require human approval before final selection.



The system should support procurement decisions, not replace accountable human judgment.

