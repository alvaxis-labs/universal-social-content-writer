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
5. If this is a new client or no current company baseline exists, read the relevant populated company sections of the Sheet and create a concise company_baseline.md using templates/company_baseline.template.md.
6. Create or refresh research_baseline.md only when SKILL.md's research triggers require durable research. Use templates/research_baseline.template.md.
7. Do not copy the entire Sheet into the baselines. Compress recurring context only.
8. Do not overwrite client-owned fields. Write only to agent-designated research, draft, source, status, verification, and working-note fields.
9. For normal recurring tasks, use the company baseline + relevant Content Plan row instead of rereading the full workbook.
10. Select the modes needed for my task: Strategy, Writing, Visual Prompt, or Posting Time. For a complete content package, provide written content, a suggested copy-paste AI image prompt, and suggested posting hours with the audience time zone and evidence or test assumptions. Read docs/visual-prompts.md and docs/posting-times.md when relevant. Produce prompt suggestions, not generated images. Store them in labeled sections of existing agent-owned fields; do not add or rename Sheet columns or overwrite the client-owned Date / Slot. Do not schedule or publish posts.
11. Before client visual prompts, apply docs/brand-kit-workflow.md. Find and inspect the approved kit and assets, store its sourced specifications in the baseline, embed the fixed rules in each prompt, and check adherence before handoff. Use the kit over generic aesthetic defaults. Inspect generated images when supplied and issue targeted correction prompts.
12. Ask me only when missing information materially affects accuracy, positioning, compliance, or quality and cannot be researched.

After initialization, inspect the current Content Plan and proceed with the task I give you. If no task is specified, tell me the client workspace is initialized and what is ready for use.
```
