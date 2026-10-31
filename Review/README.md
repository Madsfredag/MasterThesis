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
| [retrieval-log.csv](retrieval-log.csv) | Raw retrieval attempts for the records whose full text was sought on 29 and 30 October 2026, kept separate so that screening.csv stays readable. |
| `SLR-screening-completed.xlsx` | Assessment workbook: full screening metadata, 76 study extractions, appraisal ratings, key results and retrieval history. |

## Selection outcome

IEEE (550) and ACM (269) supplied 819 occurrences; 26 duplicates left 793
candidates. The Scholar supplement captured 150 occurrences, of which 46
were duplicates, leaving 104 new candidates. Two known benchmark reports
were added separately. Thus 899 candidates entered selection: 702 were
excluded at title/abstract stage and 197 reports were sought.

Retrieval passes on 29 and 30 October 2026 obtained 13 more full texts
each, after 87 reports had been assessed. Of 197 reports sought, 84 remain
not retrieved (62 database and 22 Scholar records) and 113 are assessed:
76 retained, 34 excluded and three companions. Full-text exclusions are E1: 4, E2: 3,
E3: 22 and E4: 5.
These counts refer to reports rather than independent experiments.

## Interpretation and maintenance

I checked all 113 full-text decisions and 176 title/abstract decisions.
My decisions and reasons are recorded in the corresponding fields.
There was no second independent reviewer. The sources for the flagged
results were checked where obtainable. GS2-14's borderline E4 decision
rests on the existing full-text assessment in the workbook.

SuperDRI remains included because it has an implemented diagnostic method
and completed process evaluation, although it does not establish diagnostic
correctness. DBAgent's success metric jointly assesses cause and remedy,
and its aggregate includes consultation. GS2-42 pools fault and healthy cases
in its headline success rate; Table 5 spans 0–100% healthy false positives
across configurations. Agent-MIRUPD reuses published baseline scores rather
than rerunning those baselines, so those scores are not independent evidence.

The 84 unretrieved reports remain identifiable. Access obstacles are not
relevance exclusions or proof of universal unavailability. The renewed pass used the existing candidate set. No new database search
or wholesale rescreening was performed.
Corrections should identify the affected record and evidence.

These consolidated tables replace the superseded working tables. Earlier
versions remain in Git history; there is no need to maintain parallel active
search histories or a separate download checklist. Exact source passages and
full retrieval attempts remain in the workbook rather than being duplicated
throughout the thesis.
