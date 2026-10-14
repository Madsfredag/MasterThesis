# Protocol preparation source notes

Date: 29 September 2026. These are methodological lookups, not technical-study
searches for the systematic review. They do not contribute to selection counts.

## Actual method lookups

Web-search queries executed on this date:

- `Kitchenham Charters 2007 guidelines systematic literature reviews software engineering pdf`
- `PRISMA-S Rethlefsen 2021 literature searches systematic reviews full text`

## Sources read

1. Kitchenham and Charters, *Guidelines for Performing Systematic Literature
   Reviews in Software Engineering*, version 2.3 (2007).
   https://www.cin.ufpe.br/~in1037/leitura/kitchenham2007guidelines.pdf
   Section 5.4 supports defining questions and procedures in advance.
   Sections 6.1--6.3 discuss pilot queries, search records, screening and
   appraisal. The source is methodological guidance, not evidence about
   cloud agents. Its age is an explicit exception to the recent-paper
   preference. Bibliographic identity was also checked against
   https://ebse.webspace.durham.ac.uk/ebse-bibliography/guidelines-for-performing-systematic-literature-reviews-in-software-engineering/.

2. Rethlefsen et al., *PRISMA-S*, JMLA 109(2), 174--200 (2021).
   https://jmla.pitt.edu/ojs/jmla/article/download/962/1281?inline=1
   Table 1 supports recording sources, queries, limits, dates, counts and
   deduplication. The paper explicitly distinguishes reporting guidance from
   guidance for conducting or evaluating a review. No full compliance claim
   is made. The PMC route showed a browser check, so the JMLA full text was used.

The proposed source set, search families, eligibility rules, calibration
sizes and quality questions are decisions proposed for this thesis.
They are not claimed to be mandatory rules from either publication.

## Project material read

- `operations-with-agents.md`: implementation scope, AC-1--AC-7 and DoD.
- `centralized-observability-story 1.md`: wider organisational context.
- Christian Damsgaard Jensen's report guide: logical progression, separation
  of design, implementation and evaluation, and detailed records in appendices.
- Example thesis: contents and Related Work chapter inspected for thematic
  comparison and separation from methodology/results. No text, topic-specific
  sources or conclusions copied.

The latest GitHub Introduction and Background remain the authority for
approved wording. The non-production problem statement and real operational
telemetry are preserved. The full specification also contains implementation
requirements, such as Azure AI Foundry, which are not replaced by the review.
Uploaded source documents have not been republished to GitHub.

## Follow-up on 30 September 2026

Reopened Kitchenham and Charters and PRISMA-S using the same URLs above
when moving the protocol to Appendix A. These remain methodological
sources, not included technical studies. The source-selection and appendix
placement changes are recorded in `protocol-amendments.json`.
Native database-access observations are in `access-log.json`. IEEE pilot
query attempts are in `search-log.json`. They do not establish review
findings or a formally selected corpus.

## OpenAlex replacement check on 30 September 2026

Mads requested another site after ACM bot verification prevented searching.
OpenAlex was selected after reading its official documentation and testing
the public Works API. The retained response is an access pilot, not review
evidence or a completed search. It contains an ACM-published cloud diagnosis
paper, which demonstrates discovery of that record but not complete ACM
coverage. The broad pilot also returns unrelated papers.

Official documentation read on this date:

- https://help.openalex.org/api/searching/
  Supports uppercase Boolean operators, quoted phrases and the default
  title, abstract and available-full-text search fields. Default relevance
  ranking is not an eligibility criterion. The live page states that it
  was updated on 19 September 2026.
- https://help.openalex.org/api/authentication/
  States that basic API queries can be made without a key. Access and
  usage limits can change. The check succeeded without an account.
- https://help.openalex.org/api/paging/
  Documents cursor pagination and the supported page size of up to 100.
  Complete exports must retain all pages. Only five records were retained
  in this access pilot.

Search parameters, result count and limitations are recorded under
`P-OA-20260930-01` in `search-log.json`. Raw metadata is retained in
`pilot-openalex-20260930.json`. No abstracts or full papers are republished.
Protocol amendment 0.3 records the source change before formal screening.


## Execution and reporting on 14 October 2026

The field-specific OpenAlex search and paging documentation was checked
again. Four focused title/context queries were paginated to completion in
OpenAlex and executed in IEEE Xplore. Search metadata, exact expressions and
interim counts are in `2026-10-14/`.

The field refinement improves precision but misses known relevant studies.
It is recorded as a protocol amendment and recall limitation, not a claim
that title searches exhaust the field. Thirteen full-text assessments now
support Chapter 3. The remaining selection and reference-list work is
explicitly incomplete. No backdated review decisions are asserted.
