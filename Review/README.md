# Literature review records

Updated 14 October 2026. Protocol 0.4. **Search exports are complete for the
focused queries. Study selection is not complete.**

The main synthesis is in `Chapters/03-State-of-the-Art.tex`. Appendix A holds
the review method and thirteen study assessments. These are the current
assessed evidence set, not a final set selected from the complete search corpus.

## What has actually been done

- Four searches in OpenAlex and four in IEEE Xplore on 14 October.
- 1,131 search occurrences: 933 OpenAlex and 198 IEEE.
- 954 records after exact DOI/title matching, with memberships retained.
- 305 provisional exclusions: 253 E4, 50 E3 and two E7.
- Eight formal records and five supplementary studies assessed for synthesis.
- 641 other formal records have no final assessment. Provisional exclusions
  also need verification. No human verification has been performed.

The bulk retrieval process was interrupted by a network-policy rejection.
Its failures do not establish that papers are unavailable through AU access.
Some full texts were available as previously retained author copies or through
web rendering. A PDF download is not an eligibility decision.

## Files

| File | Purpose |
| --- | --- |
| `search-log.json` | Historical pilots and executed October searches. |
| `protocol-amendments.json` | Actual dated changes and their limitations. |
| `selection-log.json` | Every deduplicated formal record, provisional decisions and pending statuses. |
| `study-extraction.json` | Thirteen assessments with source locators, quality judgements and reviewer implications. |
| `2026-10-14/status.json` | Reconciled interim counts, not a completed PRISMA flow. |
| `2026-10-14/records.json` | Bibliographic record identities, source memberships and exact-match duplicates. |
| `2026-10-14/exports/` | All hit metadata retained from the eight focused searches. |
| `2026-10-14/query-expressions.json` | Exact Boolean term blocks. |
| `2026-10-14/openalex-search-log.json` | API fields, request URLs, pagination and original-page hashes. |
| `2026-10-14/ieee-search-log.json` | Field-prefixed expressions, filters, counts and export limitations. |
| `2026-10-14/retrieval-attempts.json` | Actual bulk attempts, including errors and unassessed HTML. |
| `2026-10-14/assessed-report-versions.json` | Versions and hashes for the reports used in the synthesis. |
| `2026-10-14/original-export-manifest.json` | Original export hashes. Repository exports contain bibliographic metadata, not republished full papers. |
| `2026-10-14/prior-attempt-status-2026-09-30.json` | Recovered checkpoint from the unfinished broader September attempt. |

IEEE S4's citation download did not yield a retained file. All 45 visible
result titles and document IDs were retained instead. Abstract and publication
metadata enrichment remains pending. This is not an ACM search or an
independent arXiv search.

## Completing the review

1. Recheck the provisional exclusions and resolve pending title/abstract decisions.
2. Retrieve and assess the eligible full texts. Keep inaccessible and unattempted
   reports separate. Link preprints and publications with changed titles.
3. Complete the planned one-round reference-list check. The present supplementary
   set comes from Background and earlier exploration, not completed snowballing.
4. Verify all extraction claims and locators. Record who performed each check.
5. Reconcile the final selection flow and update the synthesis, including any
   contradictory results. Reconsider title-focused recall because several
   relevant seed studies were missed.

The scope remains the approved non-production Cloudflare-to-Azure PoC.
The search-field refinement and assistant assessments are documented decisions,
not separately approved supervisor methods or human-reviewed results.
