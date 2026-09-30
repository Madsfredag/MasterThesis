# Literature review records

Protocol version: 0.3, revised on 30 September 2026.

The full review belongs in `Appendices/A-Systematic-Literature-Review.tex`.
Chapter 3 summarises its coverage, compares the findings and explains
their implications. This directory holds the operational search and study
records supporting that appendix.

IEEE Xplore and OpenAlex are the two main search sources. Mads requested
a replacement for ACM Digital Library on 30 September 2026. The assistant
selected OpenAlex after checking its documented search capabilities and
successfully retrieving records through its public Works API without signing in.
No formal corpus has been exported, screened or assessed. Pilot queries
and database-access checks are recorded separately. Empty selection and
extraction arrays mean **not yet recorded**, not zero eligible studies.

## Next steps

1. Pilot and validate all four search families in IEEE Xplore and OpenAlex.
   Record the exact fields, date limits and platform syntax. The access
   pilot does not validate the four final queries.
2. Check retrieval of known relevant papers and estimate the screening
   workload. OpenAlex's default search includes available full text as well
   as titles and abstracts. Record any changes made after the pilot.
3. Export all results for each final query. Deduplicate, screen and assess
   them under the recorded criteria.
4. Populate the appendix with actual records and detailed findings, then
   write the evidence-based synthesis in Chapter 3.

On 30 September, the first IEEE structured-query trial displayed no
results with an unvalidated nested field expression. A simpler native
search returned 94 results, but had no publication-date filter and no
retained export. Neither query is a completed formal search. ACM remained
on a bot-verification page, so no query or result count was obtained there.
That planned search has now been replaced, rather than counted as a
completed search with no results. The OpenAlex access pilot retained five
metadata records in `pilot-openalex-20260930.json`. This is an incomplete
sample from an exploratory query, not a shortlist of included studies.

OpenAlex can index records from different publishers and repositories.
It does not reproduce an ACM Digital Library search, and an indexed record
does not establish peer review or guarantee access to the full paper.
Check publication status and link preprint and published reports of the
same study. Preserve source memberships when deduplicating overlap with IEEE.

The initial publication window is 1 January 2020 to the date of the final
search. Record each actual search date. Rerun earlier source searches at
the end of data collection so updates are captured. State any remaining
differences in coverage. Do not claim that every source was searched on
the same date unless that happened.

## Proposed search families

These are conceptual Boolean queries, **not executed database commands**.
Adapt quotation, fields and term limits to the actual interface. Preserve
the exact executed form in `search-log.json`. Search titles, abstracts and
keywords where supported. Record different fields explicitly. A platform
limit may require splitting a query into several equivalent subqueries.
Retain all their exports and deduplicate their union.

For OpenAlex, use the documented Works API Boolean `search` parameter and
publication-date filters. It searches titles, abstracts and available full
text. Retain the exact request parameters and raw metadata response. Use
cursor pagination for complete exports, checking that all pages were
retained. Do not treat the API's relevance order as a selection criterion.
See the official documentation linked in `method-source-notes.md`.

### S1: Correlation and root-cause analysis

```text
(cloud OR microservice OR microservices OR "distributed system"
 OR "distributed systems")
AND (telemetry OR log OR logs OR trace OR traces OR metric OR metrics)
AND (correlation OR "trace reconstruction" OR "request tracing"
 OR "root cause" OR "fault localisation" OR "fault localization")
```

### S2: Security telemetry and features

```text
(firewall OR WAF OR "network security" OR "application security"
 OR "intrusion detection" OR SIEM)
AND (telemetry OR log OR logs OR event OR events OR "network flow")
AND ("feature selection" OR "feature extraction" OR "feature engineering"
 OR "derived features" OR diagnosis OR investigation OR correlation)
```

### S3: LLM agents for operational diagnosis

```text
("large language model" OR LLM OR "LLM agent" OR "multi-agent")
AND (cloud OR microservice OR microservices OR AIOps
 OR "distributed system" OR "distributed systems")
AND (diagnosis OR diagnostic OR troubleshooting OR "root cause"
 OR "incident management")
```

### S4: Remediation and human oversight

```text
(cloud OR microservice OR microservices OR AIOps OR "network management"
 OR "distributed system" OR "distributed systems")
AND (remediation OR "self-healing" OR "automated repair"
 OR "incident response" OR "fault recovery")
AND (agent OR automation OR autonomous OR "human oversight"
 OR "human-in-the-loop" OR approval OR rollback OR "dry run")
```

Do not require safety terms in every S4 result. A study without an approval
mechanism can still be an informative comparator. Do not require a specific
cloud vendor. The main search is all four families in both selected databases. Scopus
and an independent arXiv search are not part of version 0.3. Author copies
may be retrieved from repositories, including arXiv, without treating
that retrieval as a separate systematic search.

## Pilot and workload

Inspect up to five records per family and one available full text per family
to test eligibility and extraction. Log the selection of pilot records.
Possible query checks from the existing bibliography include Sage,
TraceWeaver, SIERRA, RCACopilot and AIOpsLab. They are unassessed candidates,
not an included set. Record any known relevant paper a query fails to find
and examine whether the cause is vocabulary, fields or source coverage.

Use the pilot to estimate workload. If it is unmanageable, revise the scope
or queries before formal screening and document the change. Do not take
only the first page of results or stop at a desired number of included papers.
One round of reference-list checking is bounded to eligible main-search
studies and relevant Background seeds. Record each seed, reference list,
date and candidate. New candidates do not trigger further rounds without a
documented amendment. A separate forward-citation search is not included
in version 0.3. This limits coverage and must be reported.

## Eligibility decisions

Include English-language primary research within the date window that
addresses an LQ and reports an empirical evaluation in the defined domain.
Record peer-reviewed and preprint evidence separately. Keep surveys,
standards, methodology papers and product documentation as contextual or
discovery sources. They are not independent primary-study results.

For full-text exclusions, use the first applicable reason in this order:

- E1: Outside the publication period.
- E2: Full report is not in English.
- E3: Not a primary empirical study.
- E4: Domain is outside cloud/distributed application operations and their
  supporting network or security controls.
- E5: Does not address an LQ. For security benchmarks, explain why the
  telemetry/feature analysis does not inform the diagnostic question.
- E6: No relevant empirical evaluation of the described approach.

Link duplicate records and related reports before screening rather than
counting them as full-text exclusions. Mark unavailable texts `not_retrieved`
with retrieval attempts. Eligibility uncertainty remains `uncertain` until
resolved. Apply the same rules regardless of positive or negative results.

## Record files

`access-log.json` records interface-access checks without claiming that a
query was executed. `search-log.json` contains one object per actual query
attempt, including failed or unvalidated pilots. Required fields:
`search_id`, `phase` (pilot/formal/update/snowball), `protocol_version`,
`executed_at`, `executor`, `database`, `platform`, `query_family`,
`exact_query`, `fields`, `filters`, `date_from`, `date_to`, `reported_hits`,
`exported_records`, `export_file`, `status`, `coverage_limitations` and `notes`.
Citation searches also record `seed_id` and `direction`. Use null for an
unknown count with an explanation. Zero means a verified zero.

`selection-log.json` contains one object per retrieved record. Fields:
`record_id`, `source_search_ids`, `title`, `authors`, `year`, `doi`, `url`,
`report_id`, `study_id`, `duplicate_of`, `related_reports`, `publication_status`,
`title_abstract_decision`, `full_text_status`, `full_text_decision`,
`exclusion_code`, `reason`, `source_location`, `reviewer`, `decision_date`,
`ai_assistance` and `recheck`. The recheck records the sampling seed,
original and repeat decisions, differences and their resolution.

`study-extraction.json` contains one object per included study, following
`study-form.md`. Keep raw metric definitions and denominators. Do not replace
them with an invented common accuracy score. Each result links to its
report/version, page or section, and author-verified evidence.

`protocol-amendments.json` records changes after version 0.1. Fields:
`date`, `from_version`, `to_version`, `change`, `reason`, `agreed_by`,
`affected_searches_or_decisions` and `required_rework`. Do not populate
`agreed_by` without an actual decision.

Retain raw exports in an appropriate persistent location and record their
paths. Keep redistribution restrictions in mind before committing abstracts
or PDFs to a public repository. The audit trail can use metadata and source
locations without republishing full papers. Reconcile counts from these
records when writing the completed method. No flow counts exist yet.

## Interpretation

Use a comparison table with study, setting, telemetry, correlation, agent
organisation, diagnostic evidence, safety controls, evaluation and limits.
Distinguish proposed, implemented, evaluated, explicitly absent and not
reported capabilities. Separate preprints and inspect whether conclusions
depend on studies with substantial quality concerns. Link multiple reports
of one experiment to avoid counting the same evidence twice.

Research gaps must follow the extracted evidence. Limited traffic, missing
identifiers and restricted write permissions are relevance questions, not
pre-established gaps. A different vendor combination alone is not novelty.
