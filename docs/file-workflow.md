# Downloadable workbook workflow

This is the default route. No Google account, Drive connection or public sharing is required. Use an available spreadsheet-authoring capability to create actual `.xlsx` files; follow its native export and verification guidance. A chat table is not an Excel attachment.

## Intake first

When a new client has not supplied enough context, attach `assets/Client_Intake_Template.xlsx`. The single `Client Brief` tab contains nine core answers and three optional answers. Tell the client to fill the yellow cells, save and upload it with their current approved brand kit and assets. Do not require the old eight-tab workbook. Accept another supplied workbook or an adequate conversational brief instead of making the client start again.

Read supplied assets before asking questions. Inaccessible links should lead to a request for the specific file upload, not an account connection. Never claim that file upload avoids sharing the file's contents with the AI.

## Content package

Create `<Client>_Content_<Period>_v01.xlsx`. Use the actual campaign period; if unknown, use an undated descriptive name and label dates as proposed. Start with these three output tabs. Preserve a supplied Client Brief or useful existing client tabs when updating their workbook, placing output tabs first. Do not add empty research or admin tabs.

| Tab | Columns |
| --- | --- |
| Content Calendar | Post ID, Platform, Topic, Suggested date, Suggested time, Time zone, Timing basis / reason, Client-approved date / time, Status |
| Post Content | Post ID, Full post copy, CTA, Sources / factual checks, Client feedback, Client approval, Final approved copy |
| Image Prompts | Post ID, Visual / panel ID, Complete AI image prompt, Exact on-image text, Required assets, Brand source / version, Review notes |

- Create one calendar row per platform-specific post and one matching Post Content row. Assign stable IDs such as `POST-001`. Never derive IDs from current row positions or renumber after sorting.
- Image Prompts may have several rows for a carousel. Keep the parent Post ID and distinct panel IDs. Repeat applicable brand rules and exact text in every independently copyable prompt. If a post intentionally has no image, say so in one linked row rather than inventing a visual.
- Keep complete captions and prompts as selectable cell text, never screenshots or clipped summaries. Each prompt requests the whole finished image. Required assets identify actual uploaded filenames, with links only when the client supplied accessible ones. Local machine paths are not user-accessible asset links.
- Store each piece of editable content once. Exact on-image text is the reference text, and its intentional repetition inside the complete prompt must match. Put sources next to the supported copy and brand references next to the prompt.
- Posting times are suggestions, not scheduled actions. Preserve the client's approved schedule separately. Label timing evidence or test assumptions; never invent analytics.
- Preserve client approval decisions. Default new work to Pending. Changed approved copy or prompts must be marked for re-review, with the previous decision retained as history in feedback/review notes. Never mark posts published merely because the workbook was delivered.
- For a narrow text-only or single-prompt request, answer directly unless a file is requested. For calendars and complete packages, file delivery is the default.

## Make it usable

Freeze table headers and Post ID columns where useful. Use filters, readable fonts, wrapped text and practical widths. Keep the calendar compact; long captions and prompts belong on their own tabs. Size rows to expose content without shrinking text. For text beyond Excel's cell or row-height limits, split at meaningful boundaries into numbered continuation rows with the same Post ID and explicit copy order; do not silently truncate content. Use plain values for copy and prompts so leading `=` characters cannot become formulas. Do not add macros, external data connections or credentials.

Use native date/time values and explicit formats when dates and times are known. Do not replace missing dates with invented ones. Add approval/status dropdowns when supported; keep the set small and relevant.

## Revisions and return

Use the latest workbook uploaded by the client as the starting point. Ask which file is current only when versions conflict. Preserve input files and save a new version such as `_v02.xlsx`. Retain stable Post IDs, client feedback, approval history and unaffected content. Baselines are caches, not authority over the uploaded file. No automatic synchronization is implied: ask the client to upload their current version for the next revision.

Before delivery, open/inspect the saved workbook and check all tabs, full text, Post ID matches, panel IDs, source/asset references, dates/time zones, approval state and layout. Resolve orphan or duplicate post records and accidental truncation. Verify that the download points to the actual saved file.

Return a short chat handoff, for example: “Your 5-post plan is ready, with captions, complete image prompts and suggested posting times. Download [workbook]. POST-003 still needs your offer-price confirmation.” Attach/link the file through the host's supported download mechanism. Do not claim the file is delivered when only a filename or inaccessible path was printed.

If file generation is unavailable, explain that specific limitation and offer three labeled copyable tables with matching Post IDs. Do not silently switch to connected Google Sheets or require a paid service.
