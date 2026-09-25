# New Agent Workflow

## If this is the first session for a client

1. Read `README.md`.
2. Read `SKILL.md`.
3. Open the client's Google Sheet.
4. Validate the fixed tab structure.
5. Read relevant populated sections across the company-information tabs.
6. Create `clients/<company-slug>/company_baseline.md` from the template.
7. Apply the research gate in `SKILL.md`.
8. If durable research is triggered, create `clients/<company-slug>/research_baseline.md`.
9. Inspect the requested Content Plan brief.
10. Select the relevant Strategy, Writing, Visual Prompt, or Posting Time modes. Read `docs/visual-prompts.md` and `docs/posting-times.md` when relevant.
11. Write agent outputs back into the Sheet.

## If this is an existing client

1. Read `SKILL.md` only if not already loaded for the session.
2. Read the existing company baseline.
3. Read the research baseline only if relevant.
4. Read the target Content Plan row.
5. Check whether any baseline refresh trigger has occurred.
6. If not, do not reread the full Sheet.
7. Research only if the task hits a defined trigger.
8. Prepare the requested outputs. A complete package includes written content, a suggested visual prompt, and a suggested posting time with audience time zone and rationale.
9. Verify, review the content package, and write back to existing agent-owned fields. Keep prompts separate from post copy.

## If the client says the company information changed

Read only the affected Sheet tab/range where possible, update the affected baseline section, and record the refresh date.

## Standalone visual prompt request

When the user supplies a simple creative concept and only wants a suggested image prompt,
read the visual guide and provide the copyable prompt directly. Do not require a client
workbook or initialize baselines. The output is text for an image tool, not a generated image.

## Posting time suggestions

Use available audience context and account evidence. Read the timing guide for missing-data
fallbacks. Store suggestions in the agent-owned Draft section, preserve the client's Date / Slot,
and make clear that nothing has been scheduled or published.
