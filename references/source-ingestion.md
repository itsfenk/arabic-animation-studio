# Source ingestion and evidence workspace

## Supported inputs

Accept files and references the current environment can actually read: PDF, DOCX, TXT, Markdown, CSV, spreadsheets, HTML pages, URLs, image scans, transcripts, and user notes. A file extension does not guarantee readable text. For scanned documents, inspect page images when needed; do not claim OCR or transcription succeeded unless verified.

## Intake procedure

1. Inventory every source before extracting claims.
2. Record its exact title, author/organization, edition, publisher, date, URL or original file name, access date, language, format, and any access limitations.
3. For books/PDFs, capture page labels as printed and PDF page index when they differ. For video/audio, record timestamp ranges. For web sources, record stable canonical URL and publication/update date where available.
4. Extract only relevant material. Keep exact quotations short and faithful; paraphrase in your own words otherwise.
5. Note missing pages, broken links, inaccessible sections, low-quality scans, unclear authorship, and secondary citations.
6. Assign stable IDs: `SRC-001`, `SRC-002`, etc. Claims get `CLM-001`, `CLM-002`, etc.
7. Store notes in `templates/source-register.csv` and `templates/claim-ledger.csv` or a project-specific equivalent.

## User-provided sources

Ask whether supplied sources are mandatory, preferred, or simply starting points only when that distinction changes the research plan. Never assume the user's source is correct. Evaluate it respectfully and explain conflicts. Do not replace a source silently; retain it in the register and explain why a specific claim was accepted, qualified, or excluded.

## Evidence mapping

Every factual line in the script, title card, diagram, map, graphic, caption, and video description should point to one or more claim IDs. A source record alone is insufficient: the particular passage/data must support the particular claim.

Use source notes in this form:

`[SRC-004, printed p. 83 / PDF p. 91, section “...”] supports [CLM-012] for the specific point that ...`

For time-based media:

`[SRC-006, 00:12:43–00:13:18]`

## Evidence hygiene

- Distinguish primary, secondary, tertiary, and user-generated sources.
- Prefer original documents/data/official records for what they directly establish; use reputable scholarship to interpret them.
- A search snippet, generated summary, social post, or unattributed quotation is a discovery lead, not final evidence.
- Do not cite a source you did not open or inspect.
- Do not invent page numbers, titles, authors, publication dates, hadith numbers, URLs, or quotations.
- Preserve conflicting evidence rather than averaging it into false certainty.
- Track translation choices. A translated source may not preserve the exact wording or technical nuance of the original.
- Copyrighted sources may be summarized and cited; do not copy large passages, chapters, lyrics, or full transcripts into scripts.

## Research dossier output

The dossier should include: scope, research questions, source inventory, key findings, claim ledger, disagreements, unsupported/open questions, excluded claims and reasons, and a concise source bibliography. State the date research was conducted when current sources are involved.
