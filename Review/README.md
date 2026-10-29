# Literature review records

The current review question is: How do LLM-based agents use operational
telemetry to diagnose faults in cloud and microservice systems, and what
evidence supports the correctness and reliability of their diagnoses?

Chapter 3 presents the thematic synthesis and evaluation criteria. Appendix A
contains the complete review method, selection outcome, appraisal approach
and retained-report catalogue. The conventional ML comparison precedes the
LLM-focused synthesis and is not counted as an additional database search.

| Record | Purpose |
| --- | --- |
| [searches.csv](searches.csv) | Five executed searches, including exact expressions, dates, fields, filters and capture limits. |
| [screening.csv](screening.csv) | 945 recorded occurrences, with stable IDs, decisions, reasons, links, companion relations and retrieval status. |
| `SLR-screening-completed.xlsx` | Master assessment workbook supplied with the review: full screening metadata, 68 study extractions, key results and retrieval history. |

## Selection outcome

IEEE (550) and ACM (269) supplied 819 occurrences; 26 duplicates left 793
candidates. The Scholar supplement captured 150 occurrences, of which 46
were duplicates, leaving 104 new candidates. Two known benchmark reports
were added separately. Thus 899 candidates entered selection: 702 were
excluded at title/abstract stage and 197 reports were sought.

Retrieval closed on 29 October 2026 with 97 reports not retrieved. Of 100
full texts assessed, 68 were retained, 29 excluded and three linked as
companions. The full-text exclusions are E1: 3, E2: 3, E3: 18 and E4: 5.
These counts are not numbers of independent experiments or author-read papers.

## Interpretation and maintenance

Screening and extraction used AI assistance. The author's decision and reason
fields remain blank until the author performs that verification. A recorded
assessment is not independent double screening. The sources for the flagged
new results were checked where obtainable; GS2-14's existing borderline E4
assessment was retained from the supplied workbook, without claiming another
independent full-text check.

SuperDRI remains included because it has an implemented diagnostic method
and completed process evaluation, although it does not establish diagnostic
correctness. DBAgent's success metric jointly assesses cause and remedy,
and its aggregate includes consultation. GS2-42 pools fault and healthy cases
in its headline success rate; Table 5 spans 0–100% healthy false positives
across configurations. Agent-MIRUPD reuses published baseline scores rather
than rerunning those baselines, so those scores are not independent evidence.

The 97 unretrieved reports remain identifiable. Access obstacles are not
relevance exclusions or proof of universal unavailability. Retrieval is
closed for this review; no new search or wholesale rescreening is implied.
Corrections should identify the affected record and evidence.

These consolidated tables replace the superseded working tables. Earlier
versions remain in Git history; there is no need to maintain parallel active
search histories or a separate download checklist. Exact source passages and
full retrieval attempts remain in the workbook rather than being duplicated
throughout the thesis.
