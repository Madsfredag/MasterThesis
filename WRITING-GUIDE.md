# Thesis writing guide

Working conventions, updated 14 October 2026.

## Current report and editing workflow

The report is maintained in https://github.com/Madsfredag/MasterThesis.
Before editing, read the latest relevant chapter, Bibliography.bib and this
guide from the repository. Check the branch and commit to avoid mixing an
old draft with current work.

When editing in Overleaf, push changes through Integrations > GitHub before
requesting a review. Overleaf saves alone do not update GitHub. If changes
are made through GitHub, pull them into Overleaf before continuing there.
The assistant checks the repository during requested work; it does not
continuously monitor either service.

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

Decision of 30 September 2026: put the full review documentation in
Appendix A, `Appendices/A-Systematic-Literature-Review.tex`. It contains
the protocol and will contain search and selection records, quality
assessments, detailed study findings and review limitations. Remove the
old section 3.1 on the method. Chapter 3, State of the Art, presents a
concise account of the review coverage, the thematic comparison and
evidence-supported implications for the PoC. Include relevant negative
and conflicting findings. It must remain understandable without the
appendix. This supersedes the earlier decision to keep the detailed
method in Chapter 3.

IEEE Xplore and OpenAlex are the current main search sources. Mads asked
for another site after ACM access problems. The assistant selected
OpenAlex and verified an API search and metadata export on 30 September
2026. This replaces the earlier ACM source choice.
Scopus and an independent arXiv search have been removed from the plan.
One round of reference-list checking remains supplementary. An author
copy can provide full text without being counted as a database search.
Record the fields used in each source. OpenAlex's default search includes
available full text in addition to titles and abstracts. Check publication
status and link preprints to published reports. Do not describe OpenAlex
as equivalent to ACM coverage or claim comprehensive coverage of AI research.

Protocol version 0.4 and the actual reporting status are in Appendix A.
On 14 October, four focused searches were exported from both sources.
The 1,131 search occurrences produced 954 records after exact DOI/title
matching. Screening is unfinished. The current synthesis contains thirteen
full-text assessments, not a final SLR inclusion set. The 305 initial
exclusions are provisional and require verification. Do not describe
unattempted retrieval as unavailable or unfinished screening as completed.
The machine-readable status and metadata are in `Review/2026-10-14/`.
Broader September search exports were recovered from an interrupted attempt
and remain separate from the October corpus.

The author reported on 14 October that health, ping and controlled-failure
endpoints run in the Container App, with application requests and logs visible
in Application Insights. This does not establish a complete Cloudflare-to-Azure
request path or access to every intended source. Clarify and inspect that
telemetry alongside the literature work. Record actual iterations with dates.
Do not backdate searches or claim human verification that has not happened.

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

- 3.1 Telemetry Correlation and Root-Cause Analysis
- 3.2 Security Telemetry and Feature Selection
- 3.3 LLM Agents for Operational Diagnosis
- 3.4 Automated Remediation and Human Oversight
- 3.5 Comparison and Research Gap

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

