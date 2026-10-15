# Literature review records

The thesis text is in `Chapters/03-State-of-the-Art.tex` and
`Appendices/A-Systematic-Literature-Review.tex`. Detailed paper summaries and
quality assessments are included directly in the appendix.

This folder contains two supporting tables. They can be opened in Excel or
another CSV reader. They are research records, not additional thesis chapters.

| File | Contents |
| --- | --- |
| [searches.csv](searches.csv) | Eight searches: source, search date, exact expressions, fields, filters and result counts. |
| [screening.csv](screening.csv) | 954 deduplicated records: titles, authors, source links, available abstracts, search memberships and selection decisions. |

## Current selection

The searches returned 1,131 occurrences. Removing 177 exact DOI/title repeats
left 954 records. These comprise 305 provisional exclusions, eight records
assessed for the current synthesis and 641 records awaiting final assessment.
Five supplementary studies described in Appendix A bring the synthesis to
thirteen studies. The final inclusion set is not yet established.

The initial screening and assessments used AI assistance and remain unverified.
`Verified by`, `Verification date` and `Final decision` are blank until those
steps are completed. An assessed record is not automatically a final inclusion.
The exclusion codes are defined in Appendix A. Missing abstracts and dates
mean the search export did not supply them; they are not exclusion reasons.
IEEE S4 retained titles and document IDs, so those records need enrichment.

## Maintaining the records

Use the existing record ID when reviewing a paper. Check its publication
version, title/abstract and relevant full text, then record the decision and
reason. Keep provisional and verified decisions distinct. Assess the remaining
candidates and complete the reference-list search before finalising the counts.
Add new searches as rows and keep their actual search dates.

The earlier individual exports, retrieval logs and extraction files are
preserved in [repository history](https://github.com/Madsfredag/MasterThesis/tree/a664a543cba1fc5ea6f2fd15bc64f87a7b2bbb57/Review).
The two consolidated tables replace those scattered files in the working tree.
