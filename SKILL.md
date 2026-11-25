---
name: pyq-intelligence-system
description: Source-grounded workflow for extracting, organizing, classifying, comparing, and reporting previous-year examination questions (PYQs). Use when a user supplies exam papers, question banks, or syllabi and asks for question registers, syllabus mapping, repeat analysis, topic trends, study priorities, or related reports.
---

# PYQ Intelligence System

Use this workflow to analyse previous-year questions across subjects, boards, universities, programmes, and examination systems. Ground every result in the supplied documents or cited official sources. Preserve uncertainty instead of filling gaps by guesswork.

## Operating rules

- **Plan before bulk work.** First inventory the available papers and syllabus documents, identify the requested outputs, describe the processing steps, and present a concise execution plan. Wait for the user's explicit approval before bulk extraction, classification, or analysis. Answer a narrow question or inspect a small sample when that does not amount to bulk processing.
- **Keep a source trail.** For each extracted question, retain the source filename and page number (or another stable location). For syllabus mappings, record the syllabus/source title, version or date where available, and the relevant unit/topic. Cite official sources when consulting the web.
- **Do not invent data.** Never infer missing wording, marks, years, paper identity, page numbers, syllabus details, or source citations as facts. Use `unknown`, `not stated`, or `needs review` and explain uncertainty.
- **Preserve the paper's wording.** Store original question text separately from any normalized text used for comparison. Keep marks, subparts, internal choices, and question numbering distinct where the source makes them clear.
- **Show scope and denominators.** State which papers, years, syllabus version, and question records are included. Distinguish paper frequency from question frequency and marks frequency. Historical frequency is descriptive and does not guarantee future appearance.
- **Respect source material.** Use supplied files for question content. Do not reproduce more copyrighted material than needed for the user's requested analysis; prefer concise excerpts, identifiers, and summaries in reports.

## Workflow

### 1. Inventory and plan

List each supplied file with its apparent type, paper/subject/year if identifiable, page count if available, and any access or readability issue. Identify missing inputs that materially affect the requested work, such as an applicable syllabus or unclear exam-year labels. Then propose:

1. the paper set and syllabus version to use;
2. extraction and review steps, including OCR or manual checks for scans;
3. the requested register, comparisons, metrics, and deliverable formats;
4. any assumptions or unresolved questions.

Wait for explicit approval before processing the corpus at scale. If the user has already approved a clearly scoped plan, proceed without asking again. If the user changes the scope, summarize the material change and obtain approval for the revised bulk plan.

### 2. Extract and structure

Create one record per question or meaningful sub-question, retaining parent/part relationships. Capture available fields such as:

- stable question ID;
- source file, page, paper/session, year, subject, and question number;
- original wording and optional normalized wording;
- marks, including marks for parts when shown;
- syllabus unit/topic and mapping evidence;
- extraction method and confidence;
- uncertainty or review notes.

Use `unknown` for absent values. Do not treat OCR output as verified when the source is difficult to read. Mark uncertain text and ask for a clearer source only when it prevents reliable completion.

### 3. Map to the syllabus

Use the syllabus supplied for the relevant examination period as the primary mapping source. If the user asks for current or official syllabus verification, or the supplied syllabus is incomplete, consult official institutional/board sources and cite them. Record syllabus version and source date. If documents conflict, show the conflict and pause the affected mapping until the user resolves it; continue independent work when possible.

Map questions to the narrowest defensible unit/topic. A question may map to multiple topics when its parts test distinct areas. Explain ambiguous mappings instead of forcing a single classification.

### 4. Classify recurrence

Compare questions within the stated corpus and assign one of these labels:

- **Exact repeat:** wording is identical or substantially the same, allowing for immaterial formatting differences.
- **Conceptual repeat:** wording differs, but the core concept or task is materially the same.
- **Related:** topic or skill overlaps, but the question is not the same task.
- **Unique:** no meaningful match was found in the compared corpus.

For every repeat or related match, identify the paired question IDs and explain the basis briefly. Do not call questions exact repeats solely because they share keywords or a syllabus topic. State when OCR quality or incomplete papers limits the comparison.

### 5. Calculate and interpret metrics

Use clearly defined counts:

- **Paper frequency:** distinct papers containing at least one question mapped to a topic.
- **Question frequency:** question records mapped to a topic; state how subparts are counted.
- **Marks frequency:** sum of known marks mapped to a topic; state how shared or unknown marks are handled.

Show numerator and denominator, such as `4 of 8 papers`, and identify excluded or incomplete papers. Avoid double counting. If a question maps to multiple topics, explain the counting rule and do not imply topic totals must equal the corpus total.

Study priorities may consider syllabus importance, recurrence, marks, recency, and coverage, but label them as recommendations based on the supplied evidence—not predictions or guarantees.

### 6. Produce and validate deliverables

Use the format requested by the user. Common outputs include a question register and a concise report in Markdown, CSV, Excel, or PDF when those formats are available. Include the corpus scope, definitions, source references, missing-data notes, and methodology needed to interpret the results.

Before delivery, check that:

- each question can be traced to its source location;
- original wording is preserved and uncertain OCR is flagged;
- paper metadata and marks agree with the source where legible;
- repeat labels have evidence and linked records;
- syllabus mappings identify their source/version;
- metrics use consistent counting rules and show denominators;
- conclusions do not exceed what the corpus supports.

Report validation issues plainly. Do not claim a check was performed if it was not possible.

## Response style

Use clear tables for registers and comparisons when helpful. Keep extracted wording faithful, explain labels and metrics once, and separate documented facts from interpretation. When inputs are missing or ambiguous, state the effect on the result and continue with unaffected work where practical.
