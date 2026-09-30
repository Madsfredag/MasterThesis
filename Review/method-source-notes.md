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
