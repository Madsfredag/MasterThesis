# Study extraction form

Template only. No study has been assessed using this form.

## Identity and relevance

- Study ID and all linked report IDs/versions.
- Existing bibliography key, or proposed new key after verification.
- Title, authors, year, venue, DOI/URL and publication status.
- Relevant LQs and why the setting meets the eligibility criteria.
- Primary reviewer, dates, AI assistance and human verification status.

## Approach and data

- Problem, system boundary, deployment setting and fault types.
- Operational, synthetic or controlled data, traffic scale and duration.
- Logs, metrics, traces, security events and configuration evidence used.
- Correlation identifiers, time windows, topology and missing-data handling.
- Security fields, derived feature definitions and evidence of relevance.
- Model/version, prompts, tools, agent roles, state and coordination.
- Diagnosis granularity, confidence, abstention and links to source evidence.
- Training or fine-tuning requirements and access assumptions.

## Remediation

Record action types, identity/permission boundaries, allowlists, approval,
dry-run checks, execution, audit, recovery verification and rollback.
For every capability, distinguish `proposed`, `implemented`, `evaluated`,
`explicitly_absent` and `not_reported`. Add the source location and the
evaluation evidence. Implementation alone does not establish safety.

## Evaluation

- Dataset and scenario counts, ground truth and test separation.
- Baselines and differences in input information or resources.
- Each metric's original definition, value, denominator and uncertainty.
- Repeated trials and variation across models, faults or runs.
- Evidence-quality assessment procedure, including human assessment.
- Remediation success, harms, failed attempts and rollback outcomes.
- Investigation time, model/tool cost and measurement conditions.
- Author-stated limitations and separately labelled reviewer inferences.

Every factual extraction needs report ID, page/section/table and a short
paraphrase. Use `not_reported` instead of guessing. Keep different experiments
within a study separate. Do not add findings based on the abstract alone.

## Quality appraisal

For Q1--Q6 in section 3.1, record `supported`, `partly_supported`,
`not_supported`, `not_reported` or `not_applicable`, the reason and source
location. Use `not_supported` for an identifiable methodological weakness
and `not_reported` when the paper does not provide enough information.
Q4 is not applicable when no comparative improvement is claimed.
For Q5, consider randomness, repeated runs, test leakage, representativeness
and relevant confounders. Do not automatically require every item for every
study design. Do not sum the judgements or invent a pass threshold.

Explain how each material concern limits the particular conclusion being
drawn. Record the extraction recheck and resolved discrepancies separately.
