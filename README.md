# PYQ Intelligence System

The PYQ Intelligence System is a source-grounded workflow for organizing and analysing previous-year examination questions (PYQs). It helps turn exam papers and syllabi into a traceable question register, compare recurring questions, summarize topic coverage, and prepare evidence-based study priorities.

The workflow is designed for use across subjects, schools, boards, universities, and examination systems. It is an instruction package; it does not automatically extract or analyse documents by itself. Available file-reading, OCR, web, and export features depend on the assistant or platform being used.

## What it supports

- Inventorying exam papers and syllabus documents before analysis.
- Extracting questions while preserving original wording and source locations.
- Recording paper metadata, marks, question parts, syllabus mappings, and uncertainty.
- Classifying matches as exact repeats, conceptual repeats, related questions, or unique questions.
- Reporting paper frequency, question frequency, and known-mark totals with clear denominators.
- Producing requested reports or registers in formats supported by the working platform.
- Checking results against source documents and flagging gaps or uncertain details.

Historical frequency describes the supplied corpus; it does not guarantee what will appear on a future exam.

## Getting started

1. Use an assistant or workspace that can read the exam papers and syllabus you want to analyse.
2. Provide [`SKILL.md`](SKILL.md) as the workflow instructions or reference document.
3. Upload the relevant PYQ papers and the syllabus version that applies to those papers.
4. Ask for the analysis and the output format you need.
5. Review the proposed inventory and plan. Bulk processing should begin only after you approve that plan.
6. Review the delivered register and report, including source references and any flagged uncertainties.

Example request:

> Follow the PYQ Intelligence System workflow. I’m providing examination papers and the applicable syllabus. First inventory the files and propose an analysis plan. Wait for my approval before processing the full set.

## Classification definitions

| Label | Meaning |
|---|---|
| Exact repeat | Wording is identical or substantially the same, aside from immaterial formatting differences. |
| Conceptual repeat | Wording differs, but the core concept or task is materially the same. |
| Related | The topic or skill overlaps, but the question is a different task. |
| Unique | No meaningful match was found in the compared set. |

## Metric definitions

- **Paper frequency:** number of distinct papers containing at least one question mapped to a topic.
- **Question frequency:** number of question records mapped to a topic; reports should explain how subparts are counted.
- **Marks frequency:** sum of known marks mapped to a topic, with shared or unknown marks handled transparently.

Reports should state the corpus scope and show denominators, such as `4 of 8 papers`. Topics may overlap, so topic totals need not add up to the corpus total.

## Repository contents

- [`SKILL.md`](SKILL.md) — core workflow instructions.
- [`QUICK-START.md`](QUICK-START.md) — short setup and example prompt.
- [`CONTRIBUTING.md`](CONTRIBUTING.md) — contribution guidance.
- [`LICENSE`](LICENSE) — project license.

## Contributing

See [`CONTRIBUTING.md`](CONTRIBUTING.md). Keep analysis traceable to source files, preserve the original wording, and clearly distinguish evidence from interpretation.
