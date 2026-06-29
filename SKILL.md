---
name: book-to-feishu-visual-notes
description: Turn a book the user has not finished reading into a Feishu/Lark document with core viewpoints, concise annotations, and one editable visual whiteboard per viewpoint. Use when the user asks to summarize a book, make reading notes, create book takeaways, convert an unread or partly read book into a Feishu document, or repeat the “multiple core viewpoints + annotated Feishu whiteboards” reading workflow. Supports books identified by title/author/link, and higher-fidelity work when the user provides a legal full source such as PDF, EPUB, text export, Kindle highlights, web link, notes, or excerpts.
---

# Book To Feishu Visual Notes

Create a Feishu document that helps the user quickly grasp a book without pretending to have read more than the available source supports.

## Required Workflow

Before working, read `references/workflow.md`.

Follow its source-boundary rules:

- If the user only gives a title, author, or bookstore link, produce a **public-information framework version** and say that the output is based on official descriptions, public summaries/reviews, and stable public knowledge rather than the full text.
- If the user provides a legal full source or substantial excerpts, produce a **source-grounded version** with chapter-level or passage-level fidelity.
- Never imply that the full book was read unless the full book content was actually available in the conversation, workspace, or a user-provided/legal source.
- Prefer multiple focused whiteboards, one per core viewpoint, instead of compressing all ideas into one large map.
- Use Feishu/Lark document creation and editable whiteboard workflows. When the user wants bot/app attribution, create the document with bot identity and ensure the user has access.

## Output Shape

Default document:

1. Source boundary note
2. 5-8 core viewpoints
3. One editable Feishu whiteboard under each viewpoint
4. Short annotations after each board
5. “How to use this book” action section
6. Medical/legal/financial caution when relevant

Keep whiteboards explanatory, not decorative. Each board should carry one idea clearly.
