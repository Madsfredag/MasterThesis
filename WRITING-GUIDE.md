# Thesis writing guide

Working conventions for the thesis.

## Current report and editing workflow

The report is maintained in https://github.com/Madsfredag/MasterThesis.
Before editing, read the latest relevant chapter, Bibliography.bib and this
guide from the repository. Check the branch and commit to avoid mixing an
old draft with current work.

When editing in Overleaf, push changes through Integrations > GitHub before
requesting a review. Overleaf saves alone do not update GitHub. If changes
are made through GitHub, pull them into Overleaf before continuing there.

Work on one subsection at a time:

1. Agree on the purpose of the subsection and the points it must explain.
2. Read relevant research and identify which source supports each factual
   claim. Reuse existing references when they directly support the claim.
3. Write the subsection in clear English and add citations as it is written.
4. Check the text against the research questions, existing text and project
   decisions. Distinguish evidence, proposals and completed work.
5. Review the wording, compile the report and check citation order and
   layout. Update the bibliography and push the reviewed version.

## Writing style

Use clear academic English with short, direct sentences. Prefer concrete
verbs to phrases such as "forms part of the investigation". Keep one main
idea in each paragraph and explain why it matters.

Use first-person singular for research actions Mads carried out, such as
"I checked all 113 full-text decisions". Avoid referring to Mads as
"the author" in the report. Describe the research directly, without
commentary about how the text was drafted or repeated verification caveats.
Keep factual method descriptions and specific limitations concise.

For example:
- Avoid: "Whether these controls enable effective remediation while
  preventing unintended changes forms part of the investigation."
- Prefer: "The project will investigate whether these controls help the
  system resolve faults without making unintended changes."

Use British spelling consistently. Introduce abbreviations on first use.
Explain technical terms before relying on them. Do not use complicated
language merely to sound academic. Avoid semicolons in thesis prose.
Use full stops or rewrite the sentence instead. Explain abstract concepts
with a short concrete example where it helps the reader.

Use study names or "and colleagues" instead of "et al." in narrative
references, while retaining numeric citations. Introduce study-specific
labels such as RE1 and RE2 where they are used. Explain technical terms
and evaluation measures in the main text, with a brief reminder when needed,
rather than relying on a separate glossary.

Explain what a concept means in ordinary language before adding technical
detail. Use concrete phrases such as "different source IP addresses" and
"five minutes" where they make the example easier to follow. Include a
calculation only when it helps explain the concept, and state why the
result is useful. Keep qualifications close to the claim they clarify.

Use numbered sections for substantial topics. Use occasional bold paragraph
lead-ins to distinguish closely related concepts within a section, such as
Logs, Metrics and Distributed traces. Do not add a heading to every paragraph.

From Background section 2.4 onwards, choose the structure and length
according to the topic. Do not repeat a fixed number of bold lead-ins or
aim for similarly sized sections. Use connected prose when the explanation
develops one argument. Add a lead-in only where a change of topic helps the
reader. Give difficult concepts the space they need and remove repeated
setup already covered elsewhere. Do not add or cut material merely to
create artificial variation. Sections 2.1--2.3 retain their approved structure.

Every delivered section should be polished, researched and properly
referenced as text for the final report. Refer to completed text as a
section, not as a rough draft. Mark unresolved project details with
the visible TODO convention below.

## Unresolved decisions and missing text

Write established background so it can remain in the finished thesis.
Do not use vague sentences to stand in for project details that have not
been decided or confirmed. Put detailed project configuration in System
Design or Implementation where appropriate.

Whenever drafted text depends on a later decision, confirmation or result,
mark it visibly with the same LaTeX command:

~~~latex
\thesisTODO{Confirm the Azure resources and network route used in the
selected request path. Check this overview against the confirmed setup.
Describe the actual topology in System Design and add a cross-reference
here.}
~~~

The command prints a yellow box headed "TODO: TO BE COMPLETED" in the PDF.
Use it for missing sections and unfinished project-specific claims.
Each note must state what is missing and what must be done to finish it.
Keep notes short. Place a note where the text needs attention rather than
leaving an unmarked assumption elsewhere in the paragraph.

Do not turn unresolved choices into facts or promise an unagreed method.
General scientific qualifications and open research questions are not
unfinished text and do not need these markers.

Use a box only when text at that location needs a decision, confirmation
or result to be completed. If the task belongs in a later chapter, track
it in this guide instead. Keep the literature finding and its implications
in Chapter 3 without an inline project-planning note. The open tasks moved
from Chapter 3 are listed under "Follow-up work from State of the Art" below.

Search all project files for \thesisTODO{ to find the outstanding notes.
After the relevant decision or result is available, write or revise the
text and remove that note. Resolve every note before submission rather
than hiding the boxes globally.

## Evidence and references

Prefer research papers from 2020 onwards. Use standards and official
documentation where they are the appropriate source. Books are not the
default source. Internal Norlys specifications support company context and
requirements. They are not evidence that the proposed system is effective.

Read the relevant part of a source before citing it. Match each claim to
what the source actually establishes and retain qualifications and limits.
Keep a source note with the supported claim and its page or section when
useful. Reusing a source is appropriate when it supports a later claim;
reference density alone is not a measure of quality.

Reuse existing bibliography keys. Record actual website access dates in
urldate. Keep numeric references ordered by first citation using
sorting=none. Never invent a publication, result or visit date.

A systematic literature review requires an explicit search and selection
method. Collecting sources does not by itself constitute that review.
Pilot the queries and screening rules before formal screening. Record
later changes with their date, reason and effect on the evidence.

Put the review method, selection account, quality appraisal and detailed
study assessments in Appendix A, `Appendices/A-Systematic-Literature-Review.tex`.
Keep Chapter 3 focused on the thematic comparison and its implications.
Use a conventional methods structure. Do not include a day-by-day project
diary, chat history or commentary about drafting the thesis. Retain search
dates because they define the literature coverage, but do not date each section.

### Current direction after the supervisor meeting, 21 October 2026

Read [the meeting record](SUPERVISOR-MEETING-2026-10-21.md) before further
review or agent-selection work. The supervisors approved the following
review question for piloting (English translation):

> How do LLM-based agents use operational telemetry to diagnose faults in
> cloud and microservice systems, and what evidence supports the correctness
> and reliability of their diagnoses?

Prioritise finding and assessing evaluation methods that provide concrete
criteria for comparing agent approaches. Use the evidence to justify the
criteria and then the design choices. No final agent architecture, model,
evaluation framework or winner has been approved.

The current review uses the 16 October IEEE/ACM exports (793 unique
candidates), a bounded Google Scholar supplement (150 occurrences, 104 new
candidates), and two separately recorded citation additions. Search scope,
exact expressions and limitations are documented in Appendix A.

There is no fixed number of core studies or agent approaches. Include enough
evidence for a defensible answer and explain the assessment criteria and
selection reasoning. The earlier 5–15-study workload idea is not an inclusion
cap.

Consider conventional ML alternatives or components where appropriate, and
include an analysis in the report. No replacement of the LLM approach has
been decided. Extend the date range for relevant ML literature if justified,
and document any change to the search scope.

The full SLR remains in Appendix A. Put the substantive findings and the
knowledge used throughout the thesis in State of the Art. This chapter may
be 10–12 pages when justified by content, rather than constrained by the
earlier shorter outline. The agreed next meeting deliverable is the full
SLR for supervisor approval.

### Consolidated review record

Retrieval was renewed on 30 October 2026. The reconciled counts are 197 reports
sought, 84 not retrieved and 113 assessed: 76 retained, 34 excluded and
three companion reports. Do not silently remove retrieval failures or
count companions as independent confirmation. Access obstacles do not mean
that a paper is universally unavailable.

The current `Review/searches.csv` and `Review/screening.csv` replace the
superseded working tables. Earlier versions remain in Git history. The
assessment workbook, `SLR-screening-completed.xlsx`, holds full extractions,
retrieval attempts and verification records. Mads has confirmed that he
personally checked all 113 full-text decisions and 176 title/abstract
decisions. Preserve the completed verification fields and do not describe
this checking as pending. Appendix A contains the complete review method
and retained-report catalogue, and Chapter 3 contains the synthesis.

Do not reopen retrieval or rescreen the entire set of papers as routine editing.
Correct a specific evidenced error transparently. Keep source versions,
metric definitions, denominators and model/budget differences attached to
comparative claims. Distinguish checking by one reviewer from independent
double screening. Describe the actual tool assistance once in the method,
without turning the appendix into a project diary.

Chapter 5 explains how the PoC is designed, built and evaluated, referring
back to Chapter 3 where relevant. The Introduction does not need a
separate sentence announcing the review. Treat Background papers as
candidates, not automatically included studies. Keep actual search,
exclusion, extraction and amendment records. Establish research gaps
only after comparing the evidence.

## Chapter roles

| Chapter | Purpose |
| --- | --- |
| 1. Introduction | Motivate the problem and introduce the objective, problem statement, four RQs and scope. |
| 2. Background | Explain established concepts needed to understand the thesis. |
| 3. State of the Art | Summarise review coverage, compare the research findings and explain evidence-supported implications and gaps. Refer to Appendix A for the full review. |
| 4. Problem Analysis and Requirements | Analyse the Norlys use case, constraints, requirements and success criteria. |
| 5. Research Methodology and Evaluation Design | Explain the approach to designing, building and evaluating the PoC and how the RQs will be assessed. Refer back to the literature review where relevant. |
| 6. System Design | Explain and justify the proposed architecture and design choices. |
| 7. Implementation | Describe what was built and any deviations from the design. |
| 8. Evaluation and Results | Present the collected evidence and results. |
| 9. Discussion | Interpret the results, answer the RQs and discuss limitations. |
| 10. Conclusion and Future Work | Summarise supported conclusions and identify further work. |

The working Chapter 3 structure is:

- 3.1 Conventional ML and LLM-Based Diagnosis
- 3.2 Telemetry Correlation and Root-Cause Analysis
- 3.3 Security Telemetry and Feature Selection
- 3.4 LLM Agents for Operational Diagnosis
- 3.5 Automated Remediation and Human Oversight
- 3.6 Evidence for Evaluating Diagnostic Agents
- 3.7 Comparison and Research Gap

Section 3.1 is a focused contextual comparison of conventional ML and
LLM-based diagnosis, placed before the thematic review findings. It motivates
the LLM-focused question without assuming an LLM advantage. Its supporting
ML sources are not automatically included in the formal LLM review.
Keep the approved review question unchanged. The implementation and
evaluation focus on LLM-based diagnostic agents. Developing and benchmarking
a separate conventional ML diagnosis model is outside the scope. Retain the
literature comparison and justify the focus through task fit, without
claiming general LLM superiority. Statistical summaries can still support
diagnostic tools.

Refine topic headings based on the review findings. Appendix A holds the
full review documentation. Chapter 3 contains the synthesis needed for
the main argument.

Keep Background before State of the Art. Put detailed review records and
supporting experimental material in appendices where appropriate. These
chapter roles are a writing plan; chapters not yet present in the repository
still need to be created when work on them begins.

Keep the Norlys context brief in Introduction 1.1. Put the specification's
detailed boundaries in Scope and Delimitations and its detailed requirements
in Chapter 4. Retain citations when attributing company-specific claims.

The four RQs cover telemetry correlation, security-relevant data/features,
diagnostic effectiveness and remediation. Do not refer to RQ numbers before
introducing the questions.

### Agreed Chapter 4 structure and traceability

Chapter 4 is now included as `Chapters/04-Problem-Analysis-and-Requirements.tex`
with the following agreed sections:

1. Norlys Use Case and Project Boundary
2. Analysis of the Main Challenges
3. Functional Requirements
4. Non-functional Requirements and Constraints
5. Acceptance Criteria and Traceability

Preserve the argument: **Norlys problem → research findings → requirements →
evaluation method → design → implementation → results**. Chapter 4 derives
requirements from the Norlys specifications and the relevant findings in
Chapter 3 without repeating the review. Its traceability table uses:
**Requirement ID · Requirement · Source/rationale · Relevant RQ · Acceptance
criterion · Verification method**. Keep the stable F1–F9 and N1–N5 identifiers
when referring to requirements in later chapters.

Chapter 4 states what must be satisfied and what observable evidence would
demonstrate it. Chapter 5 defines scenarios, repetitions, scoring, budgets
and comparison procedures. Agent roles and architecture remain choices for
Chapter 6. Chapter 7 records the implementation and deviations. Connectivity
prototypes are feasibility work, not evidence that the requirements have
already been met or that diagnostic effectiveness has been established.

Operator interaction, approval, recovery and rollback remain requirements.
Mads has selected a dedicated web interface within the PoC project in place
of Cybertron integration. Chapter 4 explicitly records this adaptation of
Norlys AC-6 and retains its functional workflow and access separation.
A console alone does not satisfy the interface requirement. Keep the test
API, investigator and operator interface conceptually distinct, with the
operator controls accessible when the test API fails. The project uses Norlys'
designated development landing zone. Keep the model deployment under that
landing zone's control.

Chapter 4 opens with the operational problem and then introduces its contents.
Do not begin with a list of other chapters. Keep its prose focused on the use
case, analysis and normative requirements, without development updates,
connectivity-test results, console interfaces or repeated pending-decision
notes. Requirements state what the system must satisfy, not what has already
been implemented. Follow-up configuration and evaluation decisions belong
in this guide and their eventual chapters. This does not permit an unresolved
claim to be presented as a verified fact.

Use a logical progression from requirements to design and implementation
without inventing a chronology. Remove irrelevant development history from
the analysis rather than claiming all requirements preceded exploratory work.
Global Secure Access is not part of the Cloudflare use-case framing. If
relevant, distinguish the experimenter's access route in the experimental
setup later.

The full Norlys fault catalogue remains the reference expectation. The
shared production components cannot become injection targets merely to
complete it. Agree the executable cases and remediation allowlist within
the permitted boundary, and record any reduction or deferral explicitly.
Chapter 5 must specify healthy and incomplete-evidence cases, independent
reference answers, reserved cases introduced by Norlys coworkers and an
exercised rollback. Apply the agreed development/evaluation split below.
Keep these requirements distinct from completed work.

### Development, evaluation and report updates agreed 9 November 2026

Mads agreed that known faults will be used to test and develop the project,
followed by final evaluation cases whose exact faults are unknown to him.
This distinction is now required by F9 and its acceptance criteria.

- **Development cases:** faults and healthy cases that Mads can inspect and
  use to check telemetry collection, request correlation, diagnostic rules,
  agent behaviour and permitted recovery. They may guide implementation
  changes. Development success is not a result on unseen evaluation cases.
- **Reserved evaluation cases:** Norlys coworkers prepare the cases and
  record the conditions, expected behaviour, injection and reset procedures,
  and independently verified effects. Exact case details and reference answers
  remain unavailable to Mads until all compared outputs are recorded.
  Fault categories and authorised boundaries can be known in advance. Do not
  equate an unseen instance with a previously unseen fault category.
- **Before final evaluation:** fix and version the compared configurations,
  including rules, code, prompts, tools and model settings, and the scoring
  procedure. Apply the separation to every compared approach. Fault labels
  remain outside their inputs, but realistic operational symptoms are retained.
  Use equivalent cases, evidence access and scoring. Hold the model and total
  resource limits constant when comparing the agent organisations.
- **After seeing reserved cases:** record any later improvement as a new
  version. Do not retune against those cases and call the resulting scores
  performance on unseen cases. Keep development and final results separate.
- **Interface adaptation:** implement request-call controls and the operator
  workflow in the project's own web interface. Preserve evidence review,
  approval, rejection, recovery, rollback, history and role separation.
  This is Mads' selected thesis scope adaptation, not a claim that Norlys
  has formally accepted a revised company delivery agreement. No company
  acceptance, completed implementation or new production permissions are implied.

**Writing and implementation sequence.** Complete the Chapter 4 revisions,
then write Chapter 5's research methodology and evaluation design before
Mads resumes the main implementation. Chapter 6 remains System Design and
must explain the component responsibilities, interfaces and design choices
that guide implementation. Chapter 7 documents what is actually built.
Existing connectivity and telemetry prototypes remain preliminary feasibility
work. Do not invent a chronology in which they did not occur.

Chapter 5 must turn F1--F9 and N1--N5 into a concrete assessment procedure:
case selection and independence, comparison methods, scoring, repetitions,
resource limits, recovery and rollback checks, and threats to validity.
The known/reserved case split is agreed. Exact case counts, fault targets,
budgets, scoring details and the final comparison protocol are not supplied
by that agreement and must not be invented as decisions already made.

**Keep the report aligned with the implementation.** When a requirement,
assumption, design or implementation changes:

1. Record the date, reason, affected requirement IDs and the relevant code or
   configuration version in this guide, with supporting evidence where available.
2. Update the affected requirements, acceptance criteria, design description
   and implementation account. Check effects on the four RQs and evaluation.
3. Record any change to the evaluation procedure before collecting the affected
   results. Preserve the procedure and versions used for earlier results.
4. Keep material deviations and their reasons visible. Describe the final
   system accurately without presenting a later change as the original plan.

Review this section before continuing Chapters 5--7 or implementation work.
Keep all five Chapter 4 sections and the stable requirement identifiers.

### Chapter 5 evaluation design, 9 November 2026

Mads requested Chapter 5 and removal of Chapter 4's passage about how to
maintain the report. That editorial instruction remains in this guide only.
Do not put report-writing obligations into the thesis requirements.
Chapter 4.5 now ends its explanatory text with the distinction between
operational controls and diagnostic limitations.

Chapter 5 is included as
`Chapters/05-Research-Methodology-and-Evaluation-Design.tex`. Its structure is:

1. Research Approach
2. Comparison Methods and Controls
3. Cases and Independent Reference Answers
4. Experimental Procedure
5. Outcome Measures and Analysis
6. Remediation and Recovery Evaluation
7. Validity and Reproducibility

The chapter advances the earlier analysis into an experimental procedure.
It does not repeat the SLR or redefine the RQs. The ACM SIGSOFT Engineering
Research and Benchmarking standards provide methodological guidance, cited
under `sigsoft2026empirical`. The specific protocol is a thesis proposal,
not a result prescribed by that source or a claim of supervisor approval.

**Method proposed in the chapter.** Functional verification is separated
from comparative diagnosis and live remediation. The proposed comparison
is an engineer-reviewed rule-based procedure, a single investigator and
a collaborating configuration. The two comparisons answer different
questions. The rule-based procedure does not measure actual human
performance or establish time saved for engineers. Its inclusion still
needs the discussion with Christian recorded below, and its rules need
engineering review. Do not report that discussion or review as completed.

Diagnostic comparison uses fixed, scoped collections of real case telemetry
and configuration observations, exposed through equivalent tools. Live
connector checks and repair tests remain separate. Retaining evidence
must comply with Norlys policy. This methodological choice is intended to
prevent later runs benefiting from additional ingestion or changed state.
Chapter 6 must explain how the shared evidence interface supports it.
Replay diagnosis time is not live end-to-end incident resolution time.

RQ2 has a focused evidence ablation on the single investigator, comparing
basic events, added security decision/policy context and added summaries.
The field groups and independent calculations must be specified from
development data and frozen before reserved tests. Alternate tools must
not silently restore the withheld fields. Evidence variants belong to
their base cases, not to new independent fault counts.

The proposed primary diagnostic outcome requires a correct component and
cause with supported evidence. Component-only, joint correctness, evidence,
healthy conclusions, false diagnoses, abstention and operational failures
remain separately reported. Case-level success fractions and paired
differences are the main analysis. Repeated model calls do not become
independent incident samples. No claim of statistically established
superiority or production-wide accuracy follows from this finite case set.

All diagnoses and repair plans are captured before reserved reference
answers are opened. Live repair trials use those plans without secretly
correcting them from the reference. Fixed reference plans test safety
controls separately and do not count as agent repair successes.
Rollback restores the specified prior state, which may itself be faulty.
Healthy reset after rollback is a distinct harness action.

**Three visible completion notes remain in Chapter 5:**

- Case allocation: authorised targets, numbers of distinct cases by family,
  healthy controls, evidence variants, eligible repairs and the responsible
  case custodian/reviewer. Do not disclose exact reserved faults to Mads.
- Pilot-supported parameters: repetitions, total resource limits, retries,
  ingestion waiting time, workload/concurrency, verification duration, run
  total and cost. Record values before the final evaluation. These cannot
  be filled from connectivity tests or invented results.
- Independent scoring review: sample size and selection seed, plus rubric
  calibration on development outputs. Proposed review is not completed review.

Chapter 6 now specifies the proposed architecture and shared interfaces.
Chapter 7 still needs the rule and agent implementations and actual
configuration. Chapter 6's model-selection evidence remains to be completed.
The pilot may inform numeric parameters after early implementation. The
method itself must guide that work, with all final parameters fixed before
reserved evaluation. Preserve the agreed separation between development
and evaluation and the existing production change boundary.

### Chapter 6 system design, 9 November 2026

Mads requested the complete System Design chapter. It is included as
`Chapters/06-System-Design.tex`, with eight sections:

1. Architecture and Component Boundaries.
2. Evidence Access and Data Contracts.
3. Correlation and Security Features.
4. Investigation Strategies and Orchestration.
5. Model Integration and Data Protection.
6. Remediation Plans and Controlled Execution.
7. Operator Interface and Investigation History.
8. Support for Controlled Evaluation.

This is a proposed implementable design, not evidence that the complete
system exists or that Norlys has authorised additional actions. Its
architecture and approval figures describe logical software interactions.
They do not invent the physical order of the shared firewalls.

The chapter was checked against Chapters 1--5, the current writing guide,
both Norlys source specifications, the AU report guide's analysis/design/
implementation guidance, the friend's thesis as a presentation reference,
and the API repository. The thesis base was commit
`11f951650e4a921cb0293ecea484ee608ded6306`.

**Design decisions to carry into implementation and review:**

- Separate the test API, investigation host and remediation executor.
  The own-project web interface belongs to the investigation host. Faults
  affecting a shared hosting environment need controls outside that boundary.
- Use explicit C# orchestration with domain records and repository adapters.
  Foundry provides inference. The telemetry collector remains an ingestion
  component. Agent roles do not each require a separate deployment.
- All three methods use one bounded evidence gateway, common diagnosis
  schema, correlation logic and run-level resource accounting. Live and
  retained-evidence adapters implement the same contract with no fallback
  from a fixed collection to live data.
- Distinguish empty queries, partial results, unknown or unavailable coverage,
  access errors and execution errors. Preserve event/retrieval times and
  identify the observed configuration's time.
- Record identifier-supported, inferred, ambiguous and unobserved path links.
  A matching connector flow is not automatically one HTTP request. The initial
  security features are defined in Chapter 6.3, including per-firewall record
  counts and fractions with explicit units and denominators.
- The collaborating candidate has a coordinator, network/security specialist
  and application/platform specialist. This groups the four source roles
  from the company sketch. Roles share tool capabilities, and the single
  agent receives equivalent substantive instructions. Sequential scheduling
  keeps parallel execution outside the first comparison. This design choice
  is not a demonstrated advantage or a new company-approved specification.
- Use application-managed model context and explicit tool dispatch. Model
  selection remains subject to the development pilot, with the chosen model
  and settings fixed across the final agent comparison.
- Private Blob Storage with JSON artefacts and conditional workflow updates
  is a proposed storage design. It does not claim that the required containers
  or permissions exist. Reference answers need a separate inaccessible store.
  Do not recreate shared infrastructure to implement these boundaries.
- Approval binds an exact plan version. A separate executor enforces the
  target/action allowlist, preconditions, durable execution intent, duplicate
  suppression, recovery and rollback. Unknown mutation outcomes are reconciled
  before retry. Approval and audit records cannot be merely best-effort logs.
- The request button uses an allowlisted request sender targeting the
  Cloudflare-facing endpoint. Sender routing and authentication must be
  verified. Internal-origin checks have a different meaning. The platform
  health-probe interval stays at 240 seconds.
- The final fault harness and reference store remain inaccessible to the
  investigator. Development controls must not expose fault names through
  agent-visible telemetry or context. Replay, live connector checks and
  live remediation have distinct records and claims.

**Verified repository evidence:** API main was
`3981527c8e5dbff1e4a763299c37590de122f7cd`. The
`agent-telemetry-foundation` branch was
`83185001aea5f7993db59598989d4255335fdab9` and now contains the `agent/`
source. Earlier statements that it existed only locally are obsolete.
The source has a separate .NET console project, Log Analytics repository,
model repository and domain records. It retrieves application requests and
related traces and has a separate model connectivity command. Reading this
source does not establish a successful run during this thesis edit.
An integrated diagnostic loop, Cloudflare/firewall tools, structured final
diagnoses, operator UI and remediation executor are not implemented in the
inspected agent code. The existing failure endpoint exposes
`Scenario=application-error`, so it cannot serve unchanged as an unseen
diagnostic case. No application code was changed during the chapter edit.

The API branch's `AGENT-DESIGN-DECISIONS.md` contains older setup statements.
Treat its model/hosting status as historical when it conflicts with newer
verified source or Mads' reported successful connection. Detailed code and
runtime evidence belongs in Chapter 7, rather than a retrospective claim
that all design work preceded feasibility experiments.

**Three visible completion notes remain in Chapter 6:**

- The model comparison needs eligible names/versions, development-pilot
  observations and a justified final selection. Marketplace eligibility
  does not establish diagnostic quality.
- Norlys must establish permitted model fields and processing boundaries,
  plus artefact retention/access. Resource location alone is insufficient.
- The concrete authorised action adapters, approving roles, dry-run and
  rollback methods, and direct-change versus infrastructure-code process
  need to be specified. Existing production exclusions still apply.

Use these notes together with Chapter 5's case, parameter and reviewer
notes. Do not remove them by inventing approvals or experiment outcomes.
Verify actual source field mappings, connector coverage, storage and
identity configuration in Chapter 7. If implementation changes this design,
follow the alignment procedure above and preserve the assessed version.

### Follow-up work from State of the Art

These tasks concern the PoC and its evaluation. They are open decisions,
not missing literature-review text or evidence of completed work. Their
motivation remains in Chapter 3. Complete the details in the chapters
listed below and refer back to the relevant literature synthesis.

| Origin in Chapter 3 | What the later chapters need to explain | Destination |
| --- | --- | --- |
| 3.3 Security Telemetry and Feature Selection | Chapter 6.3 defines the initial security fields and traceable summaries. Confirm which are available along the selected path and check source-specific mappings and calculations. | Record the implemented fields and gaps in Chapter 7, Implementation, and assess their contribution under the Chapter 5 protocol. |
| 3.4.3 Evidence for Agent Collaboration | Chapters 5--6 specify the matched comparison and coordinator/two-specialist candidate with shared evidence, model and total limits. Final numeric limits require the development pilot. | Complete the Chapter 5 parameter note and verify the Chapter 6 role and budget contracts in Chapter 7. |
| 3.6.1 Diagnostic Correctness and Evidence Grounding | Chapter 5 separates reserved references from diagnostic inputs and defines correctness and evidence scoring. Verify that the fault harness, tools and stored inputs enforce this separation. | Chapter 7, Implementation, and the Chapter 5 case/reviewer notes. |

Remove an item from this list only when the corresponding account has been
written and checked, or an explicit scope decision makes it unnecessary.
Keep the exact four thesis research questions and the single SLR review
question unchanged when completing these tasks.

### Candidate baseline from the supervisor discussion, 4 November 2026

**Status: proposal retained for discussion with Christian.** Søren suggested
an engineer-informed decision tree or rule-based troubleshooting procedure
as a reference for evaluating the agents. No final baseline or additional
human-participant study has been agreed.

The procedure would define which observations trigger which checks, the
evidence required for a conclusion and when to stop or report insufficient
evidence. The firewall was an illustrative check, not an agreed starting
point. A reasonable procedure reviewed with Søren could provide a repeatable
reference without claiming to represent every engineer's individual approach.

A candidate implementation is ordinary conditional code using the same
telemetry connectors as the agents, with explicit rules choosing the next
query and interpreting results. This would be an additional rule-based
baseline, not a trained ML model or a replacement for the multi-agent PoC.

Two comparisons would answer different questions:

- Rule-based procedure versus an agent: does agent-directed investigation add
  diagnostic value beyond the defined procedure?
- Single investigator versus collaborating agents: does collaboration add
  value under comparable conditions?

Use shared cases, evidence access and scoring. For the agent variants, retain
the same model version, tools and total resource limits. Define and review
the rules before the final evaluation cases are used, including healthy and
incomplete-evidence outcomes. Assess correctness, evidence, time, resource use
and any required human intervention, rather than rewarding agreement with a
particular query order.

An automated procedure does not measure actual human performance. Claims
about time saved for engineers would require corresponding human observations.
The proposed baseline can be useful without making that claim. Chapter 5 now
sets out this candidate comparison for review. Discuss feasibility with
Christian before treating it as the final experimental protocol. Explain
the chosen design in Chapter 6 and any implementation in Chapter 7.

### Model comparison and selection

Recorded 2 November 2026. Model selection needs an explicit comparison and
justification. An initial model used to establish connectivity is not evidence
that it is the best model for operational diagnosis.

| Chapter | Account to write |
| --- | --- |
| 4. Problem Analysis and Requirements | State the capabilities and constraints the model must satisfy, including tool calling, structured diagnostic output, evidence use and the agreed hosting and data-processing boundaries. |
| 5. Research Methodology and Evaluation Design | Define the candidate-selection procedure and any pilot tests. Specify common tasks, evidence, scoring and resource limits before running a comparison. Keep pilot cases separate from the final evaluation cases. |
| 6. System Design | Compare the shortlisted models against those criteria, explain trade-offs and justify the choice. Distinguish documented capabilities from observations in the pilot. |
| 7. Implementation | Record the model and version actually deployed, deployment name and type, region, hosting option, authentication, SDK/API integration and relevant settings. Describe deviations from the design explicitly. |
| 8. Evaluation and Results | Report the formal experimental results. If models are compared experimentally here, use the procedure defined in Chapter 5. Do not present vendor benchmarks as results from this PoC. |

Use Chapter 3 to motivate the diagnostic and evaluation criteria. The model
comparison should consider deployment availability, tool calling and structured
output, diagnostic correctness, evidence support, latency, token use, cost and
model-version availability through the evaluation period. The shortlist, pilot
cases, scoring and thresholds remain to be specified.

For the proposed single-investigator versus collaborating-agent comparison,
hold the selected model and version, tools, available evidence, scenarios and
total resource limits constant. Model choice and agent organisation are
different variables. No final architecture or model winner has been established.

**Current setup direction.** Claude deployment was blocked by the tenant's
Private Marketplace policy. Mads subsequently selected the lightweight GPT
deployment `gpt-6-luna` in the project's Foundry resource.
He confirmed a successful playground call and a successful connection from
the local C# application. Keep the resource-specific endpoint in the project's
protected configuration rather than in this public writing guide.
These are user-confirmed connectivity results, not evidence of telemetry
diagnosis or a completed model comparison. On 5 November, Mads supplied a
Copilot inspection reporting model version `2026-09-22` and deployment type
`GlobalStandard`. These settings have not been independently
checked in Azure during the thesis edit. Record the deployed configuration
and integration settings in Chapter 7. Mads makes application-code changes
himself.

**Hosting distinction to resolve.** Keep the Foundry resource and deployment
under the designated development landing zone, with Sweden Central as the preferred resource
location. Resource ownership and resource location do not establish where
inference is processed. Sweden-only inference has not been established as a
Norlys requirement. Confirm the permitted processing boundary and the actual
deployment's processing terms before sending operational telemetry. A
successful connection does not settle that data-handling question.

Historical source notes for the earlier Claude candidate, consulted
2 November 2026:

- [Anthropic: Claude Haiku 5.5](https://www.anthropic.com/claude-haiku-5-5):
  identifies the new lightweight model, released 7 October 2026.
- [Anthropic: Claude in Microsoft Foundry](https://platform.claude.com/docs/en/build-with-claude/claude-in-microsoft-foundry):
  lists Haiku 5.5, its deployment name and Azure/Anthropic hosting options.
- [Microsoft: Deploy and use Claude models in Microsoft Foundry](https://learn.microsoft.com/en-us/azure/foundry/foundry-models/how-to/use-foundry-models-claude):
  documents deployment scope, Marketplace prerequisites and authentication.

## Project decisions and limits

Use the agreed problem statement and research questions unless Mads
explicitly changes them. The current problem statement retains
"non-production" and the exact four RQs remain unchanged. On 5 November,
Mads explicitly requested clarification of the environment boundary.
Non-production describes the test application and authorised experimental
resources, not the entire transport path. Chapters 1, 2 and 4 now distinguish
this development environment from the shared production tunnel connector
and firewalls. This is a documented boundary clarification, not permission
for production fault injection or remediation. Any rewording of the approved
problem statement itself remains a separate decision. The data is real
operational telemetry, filtered to the test investigation, not mock data.

Do not present tools, experiments, comparison baselines or detailed
evaluation methods as agreed decisions unless they have been agreed.
AIOpsLab is potential related work, not an adopted evaluation framework.
Citing ReAct or AutoGen does not commit the implementation to either.
Do not assume that a complete trace or every desired telemetry field will
be available.

Describe unimplemented work as planned or proposed. Avoid claims that the
system is safe, accurate or effective before evaluation. Keep Main
Contributions and Outline of the Thesis as placeholders until there is
enough evidence and the structure is stable.

### Environment boundary and follow-up, 5 November 2026

Mads supplied a newer Copilot inspection of the environment. It was not
independently verified against Azure or Cloudflare during this edit.
The following consequences guide the report without reproducing an internal
network inventory in this public repository:

- Distinguish a configured Cloudflare Tunnel route from a demonstrated
  end-to-end request and complete correlation. Record the experimental
  client's authorised access and successful endpoint behaviour as evidence.
- Source coverage must apply to the selected test hostname. The presence of
  Cloudflare telemetry for another zone does not establish that coverage.
  Confirm the required request and security-event data and policy access.
- Tunnel-side connection records do not uniquely identify HTTP requests.
  Recording the Cloudflare request identifier in application telemetry is a
  correlation requirement to implement and verify, not a completed result.
  Preserve the background chapter's qualification about identifier uniqueness.
- Development resources are distinct from shared production connectivity.
  Development tags do not authorise arbitrary changes. Proposed WAF, firewall,
  network-security or tunnel changes are not approved fault targets. Keep
  production writes excluded and record actual fault coverage against AC-7.
- Model ownership, resource location and inference processing location are
  different constraints. Sweden Central remains a preferred resource location,
  not an established Sweden-only inference requirement. Confirm permitted
  fields, masking, processing locations and record retention against Norlys
  policy before using operational telemetry.
- Existing portal and infrastructure workflows are integration inputs, not
  completed PoC functionality. Establish authorised actions, operator roles,
  execution permissions, the change process and recovery and rollback checks.
- Chapter 5 must define evidence retention sufficient for reproducible cases,
  independently introduced faults and evaluation budgets. Chapters 6 and 7
  must distinguish proposed runtime and storage choices from their implementation.
  The rule-based baseline remains a proposal for discussion with Christian.

The public report can explain these boundaries without internal hostnames,
private addresses, shared-resource identifiers or a detailed permission
inventory. Keep detailed operational evidence in the appropriate Norlys
records. The dedicated operator interface replaces Cybertron integration as
recorded above. Retain its workflow and human-approved remediation requirements.
Do not claim successful cross-source correlation or verified remediation
from a model connection test.

## Layout convention

Keep A4 paper and the existing oneside setting. The proposed body layout
uses equal 28.5 mm side margins, with 25 mm at top and bottom including the
header/footer area. The side margins approximate the friend's PDF. That PDF
uses US Letter, so page breaks and text width will not be identical.
The title page retains its separate geometry settings.

Example of a bold paragraph lead-in:

~~~latex
\noindent\textbf{Logs.} A log records events emitted by a system component.
~~~


## Agreed revision requirements

- Preserve the four thesis RQs and the single approved SLR review question.
- Write final-quality prose. Do not use semicolons or the word “corpus”.
- Compare conventional ML and LLM methods against the same diagnostic needs.
  Motivate the LLM focus from task fit, without treating general superiority as established.
- Introduce a paper before referring to its authors' findings. Define metrics before scores.
- Security scope concerns misconfigured controls blocking legitimate requests.
  Attack detection is outside the PoC evaluation scope.
- Use the existing yellow thesisTODO boxes for project choices awaiting agreement
  when they prevent completion of the text at that location. Track tasks for
  later chapters in this guide.
  Keep genuine research limitations in ordinary academic prose.
- Explain technical terms, study-specific labels and evaluation measures
  where the reader needs them. The report has no separate glossary appendix.
- After all chapters are written, review titles, repeated content and the narrative
  connecting the problem, four RQs, literature, design, evaluation and conclusions.
