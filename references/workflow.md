# Workflow

## 1. Establish Source Boundary

Classify the source before summarizing:

| Tier | Available material | Output label | What to do |
| --- | --- | --- | --- |
| A | Full legal text: PDF, EPUB, copied chapters, article/book web text, or full notes | Source-grounded version | Extract chapter structure, core claims, evidence, examples, tensions, and action implications. Cite or reference the user-provided source where useful. |
| B | Substantial partial source: sample PDF, long excerpt, Kindle highlights, lecture notes, chapter summaries | Partial-source version | Ground claims in the provided material, clearly mark gaps, and supplement only with public official sources if needed. |
| C | Title/author/link only | Public-information framework version | Browse official publisher/author pages and stable public sources. Summarize the known public framework. Explicitly say this is not a full-text summary. |

Never use unauthorized “free PDF” mirrors or piracy sites. If only a sample PDF is available, say it is incomplete and ask for the full legal source if the user wants chapter-level fidelity.

## 2. Gather Source Material

- For Tier C or if facts may have changed, browse official pages first: author site, publisher page, library/ebook listing, table of contents previews, reputable interviews, and reviews.
- For uploaded files or local files, use the relevant file skill (`pdf`, `documents`, `spreadsheets`, etc.) and extract enough structure before writing.
- For links, inspect the page contents rather than relying only on the title.

Keep source notes internal unless the user asks for detailed citations; include source boundary in the final document.

## 3. Choose Viewpoints

Pick 5-8 viewpoints. Each viewpoint should be a claim the reader can remember, not just a topic label.

Good viewpoint examples:

- “The goal is healthspan, not just lifespan.”
- “Medicine 3.0 shifts care from late treatment to early risk management.”
- “Exercise functions like a core longevity drug.”

Weak viewpoint examples:

- “Exercise”
- “Chapter 3”
- “Nutrition section”

If full source is available, include nuance: counterarguments, evidence quality, where the author speculates, and what the book under-emphasizes.

## 4. Design One Board Per Viewpoint

Use the installed `beautiful-feishu-whiteboard` skill when available. Prefer a restrained reading style such as `Reading Room`, `Editorial Forest`, `Papier Bleu`, or another style that fits the book.

Board rules:

- One board = one idea.
- Put only content on the board; no tool names, source labels, prompts, or process notes.
- Keep boards simple enough to remain editable and readable.
- Use native shapes and whiteboard validation/rendering rules from `beautiful-feishu-whiteboard`.
- Render and visually inspect each board before writing it to Feishu.

Suggested board patterns:

| Viewpoint type | Board pattern |
| --- | --- |
| Shift in mindset | Before/after comparison |
| Method or framework | Center model with 3-5 supporting blocks |
| Risk landscape | 2x2 or clustered risk cards |
| Intervention stack | Layered pyramid or columns |
| Timeline | Horizontal stages |
| How to apply | Loop or checklist flow |

## 5. Create The Feishu Document

Use `lark-doc` for the document and whiteboard block creation. Default to the user identity only when normal personal ownership is desired.

If the user wants the document authored by a bot, app, or CLI identity:

1. Create the document with `--as bot`.
2. Confirm the CLI grants the current user `full_access`, or otherwise tell the user what permission is missing.
3. Write whiteboards using the same identity where possible.
4. Verify the user can fetch/open the document with `--as user`.

Document structure:

```xml
<title>《书名》核心观点与注释图</title>
<callout>Source boundary note and one-sentence conclusion</callout>
<h1>观点一：...</h1>
<whiteboard type="blank"></whiteboard>
<p>Annotation...</p>
...
<h1>怎么开始用这本书</h1>
<ol>...</ol>
```

## 6. Quality Bar

Before delivering:

- Verify every whiteboard rendered locally.
- Check there are no text overflow errors.
- Confirm the Feishu document can be fetched by the intended viewer.
- Provide the Feishu link and briefly state the source boundary.
- If there is no full source, say what would improve fidelity: full PDF/EPUB, chapter photos, Kindle highlights, notes, or a legal full-text link.
