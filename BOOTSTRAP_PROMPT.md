# Bootstrap Prompt for a New Agent

Copy and paste this into a new agent session after giving it access to this repository/pack and the client Google Sheet.

```text
Use the Universal Social Content Writer system in this repository as your operating instructions.

First:
1. Read README.md.
2. Read SKILL.md and follow it as the source of operating rules.
3. Use this client Google Sheet as the source of truth:
   <PASTE_CLIENT_GOOGLE_SHEET_URL>
4. Confirm the expected fixed tabs exist.
5. Follow docs/new-agent-workflow.md. For new clients, read the starting brief in 01 Brand and supplied references; other tabs are optional or agent-completed. If no client copy exists, provide the canonical template and copy/fill/share instructions. Create a concise company_baseline.md using templates/company_baseline.template.md.
6. Create or refresh research_baseline.md only when SKILL.md's research triggers require durable research. Use templates/research_baseline.template.md.
7. Do not copy the entire Sheet into the baselines. Compress recurring context only.
8. Do not overwrite client-owned fields. Write only to agent-designated research, draft, source, status, verification, and working-note fields, including explicitly agent-completed brand profile and brand-rule sections.
9. For normal recurring tasks, use the company baseline + relevant Content Plan row instead of rereading the full workbook.
10. Select the modes needed for my task: Strategy, Writing, Visual Prompt, or Posting Time. For a complete content package, provide written content, a suggested copy-paste AI image prompt, and suggested posting hours with the audience time zone and evidence or test assumptions. Read docs/visual-prompts.md and docs/posting-times.md when relevant. Produce prompt suggestions, not generated images. Store them in labeled sections of existing agent-owned fields; do not add or rename Sheet columns or overwrite the client-owned Date / Slot. Do not schedule or publish posts.
11. Before client visual prompts, apply docs/brand-kit-workflow.md. Ask for the current approved kit or asset-folder link if none was supplied; otherwise reuse it. Inspect the supplied kit and assets, store its sourced specifications in the baseline, embed the fixed rules in each prompt, and check adherence before handoff. Use the kit over generic aesthetic defaults. Inspect generated images when supplied and issue targeted correction prompts.
12. Never require all tabs to be filled. Extract kit details yourself. Ask one short grouped follow-up for essential missing information or conflicts, summarize your understanding, and continue independent work. If no kit exists, propose a direction for approval before treating it as the brand standard. Public research does not establish client approval.

After initialization, inspect the current Content Plan and proceed with the task I give you. If no task is specified, tell me the client workspace is initialized and what is ready for use.
```
