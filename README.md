# Book to Feishu Visual Notes

An agent skill for turning a book into a Feishu/Lark document with:

- clear source-boundary handling,
- 5-8 memorable core viewpoints,
- one editable visual whiteboard per viewpoint,
- concise reading annotations and action notes.

The skill is designed for books the user has not finished reading yet. It does **not** pretend to read the full book when only public information is available.

## Source Boundary

The skill explicitly separates three cases:

- **Full legal source available**: PDF, EPUB, copied chapters, full notes, or a legal full-text link. The output can be source-grounded and chapter-aware.
- **Partial source available**: sample PDF, excerpts, Kindle highlights, lecture notes, or chapter summaries. The output should mark gaps and avoid overclaiming.
- **Title/link only**: the output is a public-information framework version based on official pages, public summaries, and stable public knowledge.

It should not use unauthorized book PDFs or piracy mirrors.

## Requirements

Recommended runtime capabilities:

- Codex or another agent that supports `SKILL.md` skills.
- `lark-cli` configured for Feishu/Lark document creation.
- A Feishu/Lark account and appropriate document/whiteboard permissions.
- Optional but recommended: [`beautiful-feishu-whiteboard`](https://github.com/zarazhangrui/beautiful-feishu-whiteboard) for polished editable whiteboard styling.
- File-reading skills or tools for PDF, EPUB, DOCX, or other source formats when full content is provided.

## Install

Install this repository as a Codex skill from the repository root:

```bash
python3 install-skill-from-github.py \
  --repo oliviawen92-stack/book-to-feishu-visual-notes \
  --path . \
  --name book-to-feishu-visual-notes
```

If your agent supports direct GitHub skill installation, use the repository URL and select the repository root as the skill path.

## Example Prompt

```text
Use $book-to-feishu-visual-notes to turn this book into a Feishu document with core viewpoints and visual annotation boards: Outlive by Peter Attia.
```

For better fidelity, provide a legal PDF/EPUB, long excerpt, Kindle highlights, or your own notes.
