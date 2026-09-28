# Universal Social Content Writer

A reusable content planning, writing, and creative direction skill for **X/Twitter and Facebook**. It produces written content, copy-paste AI image prompt suggestions, and suggested posting times.

The system is designed so the client maintains one Google Sheet, while the agent maintains compact working context and reusable research.

## Architecture

- **`SKILL.md`**: universal operating instructions for the agent. Never store client-specific information here.
- **Client Google Sheet**: source of truth for brand, audience, voice, products, strategy, competitors, content plan, terminology, claims, and approvals.
- **`company_baseline.md`**: agent-generated compressed company context for recurring work.
- **`research_baseline.md`**: optional agent-generated durable market/category research.

The Google Sheet always wins if it conflicts with a baseline.

## Supported channels

- X/Twitter
- Facebook

## One skill, multiple modes

The modes share the same brand context and approved strategy:

| Mode | What you get |
| --- | --- |
| Strategy | Research, ideas, angles, pillars, campaigns, and content plans |
| Writing | Posts, threads, hooks, CTAs, and platform adaptations |
| Visual Prompt | Visual concepts, suggested AI image prompts, on-image copy, and multi-image outlines |
| Posting Time | Suggested hours, audience time zone, rationale, and evidence or test assumptions |

Ask for a complete content package to get three outputs: written content, a suggested visual prompt, and a suggested posting time. Or request just one output. Editorial review applies to the whole package.
Visual Prompt Mode produces suggestions you can copy into an image tool. It does not create
images itself. Each prompt asks the image AI to create the whole finished graphic, including
its text and layout; no separate Canva or Photoshop assembly is required by default.
Prompts default to a simple, slightly amateur human-made appearance: ordinary fonts,
basic shapes, few elements, and mild unevenness. Text stays readable. Canva/Photoshop
are examples of familiar tools, not a required style or a demand for professional polish. 3D remains available when explicitly requested
or part of approved brand guidance. See [the visual prompt guide](docs/visual-prompts.md) for the format and an example.
[Posting time guidance](docs/posting-times.md) distinguishes account evidence from suggested
test windows. These are recommendations, not scheduled posts.

Example requests:

- “Turn Content Plan row 12 into a Facebook post with a visual concept and a copy-paste AI image prompt.”
- “Suggest a pink character graphic that looks made by a beginner: simple flat doodle, ordinary font, few elements, and no glossy 3D.”
- “Outline a five-panel educational post with panel copy and image prompt suggestions.”
- “Review this caption and visual prompt together, then improve them.”
- “Suggest posting hours for this Facebook post for our audience in Vietnam. Label times to test if we have no analytics.”

Simple standalone prompt requests do not need a client Sheet. Brand content uses the setup
below. The scope remains X/Twitter and Facebook; video production and automatic publishing
are outside this pack's current workflow.

## First-time setup

1. Give the agent this repository (or upload this pack).
2. Give the agent the client's Google Sheet URL.
3. Paste the prompt in `BOOTSTRAP_PROMPT.md`.
4. The agent reads `SKILL.md` and the client Sheet.
5. The agent creates a client workspace and generates `company_baseline.md`.
6. The agent creates `research_baseline.md` only if durable external research is triggered.
7. The agent selects the relevant modes, prepares the requested content package, and writes results back to the existing agent-owned Sheet fields.

## Normal recurring work

For normal tasks, the agent should **not reread the full workbook**.

It should use:

1. `SKILL.md`
2. the client's `company_baseline.md`
3. `research_baseline.md` when relevant
4. the relevant row(s) from `07 Content Plan`
5. only the specific Sheet section needed for verification or refresh

## Client Sheet

Current template:

https://docs.google.com/spreadsheets/d/1MYlCFQZYjfnFfNlWqQ9idDWg1jBpaDZCr6AjkfzzbgQ/edit

The client should make a copy for their company and keep the fixed tab names and headers.

See `docs/sheet-schema.md` for the expected structure and ownership rules.

## Client workspace

Recommended structure per client:

```text
clients/
  company-slug/
    company_baseline.md
    research_baseline.md
```

Do **not** commit real client baseline files to a public repository unless the client explicitly permits it. The default `.gitignore` excludes client-generated files.

## Core rule

**Follow the strategy. Challenge the execution.**

The agent should respect approved positioning, audience, facts, and strategy while improving weak angles, hooks, framing, structure, format, and CTA.
