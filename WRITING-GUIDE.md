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
Keep the approved review question unchanged and evaluate conventional ML
as a possible component or baseline when its data and task requirements fit.

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

### Follow-up work from State of the Art

These tasks concern the PoC and its evaluation. They are open decisions,
not missing literature-review text or evidence of completed work. Their
motivation remains in Chapter 3. Complete the details in the chapters
listed below and refer back to the relevant literature synthesis.

| Origin in Chapter 3 | What the later chapters need to explain | Destination |
| --- | --- | --- |
| 3.3 Security Telemetry and Feature Selection | Confirm which fields are available along the selected path: time, source and destination, request target, status, policy action and rule identifier. Explain which fields the diagnostic tasks require and whether event counts or other aggregates should be exposed as agent-tool outputs. Justify the choice using availability and diagnostic relevance. | Chapter 4, Problem Analysis and Requirements, and Chapter 6, System Design. Record the implemented fields and any gaps in Chapter 7, Implementation. |
| 3.4.3 Evidence for Agent Collaboration | Specify the single-investigator baseline and collaborating variant to be compared. Define the shared model, evidence interface, scenarios and resource limits so that the comparison can distinguish agent organisation from changes in available information or budget. These variants remain candidates until the evaluation design is agreed. | Chapter 5, Research Methodology and Evaluation Design. Describe the chosen agent roles and interfaces in Chapter 6, System Design. |
| 3.6.1 Diagnostic Correctness and Evidence Grounding | Explain how fault labels and other answer-revealing test metadata are kept separate from agent-visible telemetry. Check this separation in the implemented fault scenarios. | Chapter 5, Research Methodology and Evaluation Design, and Chapter 7, Implementation. |

Remove an item from this list only when the corresponding account has been
written and checked, or an explicit scope decision makes it unnecessary.
Keep the exact four thesis research questions and the single SLR review
question unchanged when completing these tasks.

## Project decisions and limits

Use the agreed problem statement and research questions unless Mads
explicitly changes them. The current problem statement retains
"non-production". The planned data is real operational telemetry, not mock
data. Do not silently reinterpret either statement.

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
- Appendix B explains technical terms and evaluation measures.
- After all chapters are written, review titles, repeated content and the narrative
  connecting the problem, four RQs, literature, design, evaluation and conclusions.
