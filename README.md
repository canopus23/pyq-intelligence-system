# PYQ Intelligence System (PYQ-IS)

**A reusable, source-grounded workflow for extracting, classifying, analysing and comparing Previous-Year Questions (PYQs).** Designed to work across subjects, universities, boards, programmes and examination systems.

> The system plans first and waits for explicit approval before bulk processing.

## What it does

- Extract questions from PDFs, documents, scans and other provided papers; retain source file/page references and extraction confidence.
- Structure questions into a normalized register with paper metadata, marks, units, topics and original wording.
- Map questions to syllabus topics using both provided syllabi and official sources; note source dates and conflicts.
- Identify **exact repeats**, **conceptual repeats**, **related questions**, and **unique questions**.
- Calculate transparent topic frequency, question frequency and known-mark totals; show denominators.
- Analyse trends and prepare approved study priorities without presenting historical frequency as a guarantee.
- Generate deliverables in Markdown, CSV, Excel and PDF as requested.
- Validate outputs against source files and flag missing or uncertain details.

## Quick start

1. Start a ChatGPT Project named **PYQ Intelligence System** (or use any compatible assistant/workspace).
2. Add [`PROJECT-INSTRUCTIONS.txt`](PROJECT-INSTRUCTIONS.txt) to the project instructions.
3. Upload [`SKILL.md`](SKILL.md) and [`PYQ-IS-Reference-Manual.md`](PYQ-IS-Reference-Manual.md) as reference files.
4. Upload your PYQ papers and syllabus/course outline.
5. Ask for the analysis you need. The workflow should return a task inventory and execution plan, then **wait for your approval**.
6. Review the approved work and validate the resulting reports against the sources.

This is a portable instruction and template package—not an automatically installed native AI skill. Tool availability, file limits and capabilities vary by platform and account.

## Package contents

| File / folder | Purpose |
|---|---|
| `SKILL.md` | Core reusable workflow instructions |
| `PROJECT-INSTRUCTIONS.txt` | Instructions for a persistent assistant workspace |
| `PYQ-IS-Reference-Manual.md` | Combined reference manual |
| `QUICK-START.md` | Short setup guide |
| `modules/` | Document processing, question analysis, reporting and validation procedures |
| `schemas/` | Normalized question data schema |
| `templates/` | Report template and question-register CSV |
| `examples/` | Example task and proposed plan |
| `tests/` | Acceptance checklist |
| `PYQ-IS-Quick-Start.pdf` | Printable quick-start guide |
| `PYQ-IS-Question-Register.xlsx` | Starter spreadsheet register |

## Classification model

1. **Exact repeat** — wording substantially matches an earlier question.
2. **Conceptual repeat** — tests the same core concept with different wording or framing.
3. **Related** — overlaps in topic or skills, but is not the same question.
4. **Unique** — no meaningful match found in the supplied corpus.

## Metrics

- **Paper frequency:** number of distinct papers in which a topic appears.
- **Question frequency:** number of question records associated with a topic.
- **Marks frequency:** sum of known marks associated with a topic.

Always show the denominator and corpus scope. Do not confuse question counts with paper counts, and do not imply that frequency guarantees future appearance.

## Quality principles

- Never invent question wording, marks, paper years, page numbers, syllabus mappings or official sources.
- Preserve original wording; put normalized wording in a separate field.
- Cite the source file and page for extracted questions; cite official sources for syllabus mappings.
- Mark missing data and uncertainty explicitly.
- Keep syllabus versions and source dates visible.
- Review OCR and classification uncertainty rather than silently guessing.

## License

Released under the [MIT License](LICENSE).

## Contributing

See [`CONTRIBUTING.md`](CONTRIBUTING.md) and the acceptance checklist in `tests/acceptance-tests.md`.
