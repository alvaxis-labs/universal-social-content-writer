# Universal Social Content Writer

A reusable content planning, writing, and creative direction skill for **X/Twitter and Facebook**. It produces written content, copy-paste AI image prompt suggestions, and suggested posting times.

The client completes one starting brief and shares approved references. The agent organizes the detailed Google Sheet workspace and maintains compact working context and reusable research.

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
Prompts default to thoughtful everyday design: clear hierarchy, moderate detail, natural
depth, and purposeful accents. The aim is a finished, approachable human-made feel without
excessive gloss or deliberate amateur styling. Canva/Photoshop are illustrative references;
subjects, colors, and materials adapt to each brief. 3D remains available when explicitly requested
or part of approved brand guidance. See [the visual prompt guide](docs/visual-prompts.md) for the format and an example.
[Posting time guidance](docs/posting-times.md) distinguishes account evidence from suggested
test windows. These are recommendations, not scheduled posts.

Example requests:

- “Turn Content Plan row 12 into a Facebook post with a visual concept and a copy-paste AI image prompt.”
- “Suggest a pink character graphic with thoughtful composition, moderate detail, natural depth, and no excessive gloss.”
- “Outline a five-panel educational post with panel copy and image prompt suggestions.”
- “Review this caption and visual prompt together, then improve them.”
- “Suggest posting hours for this Facebook post for our audience in Vietnam. Label times to test if we have no analytics.”

Simple standalone prompt requests do not need a client Sheet. Brand content uses the setup
below. The scope remains X/Twitter and Facebook; video production and automatic publishing
are outside this pack's current workflow.

## Client brand adherence

Before writing a client image prompt, the agent asks for the approved brand kit if it has not already been supplied, then reads it,
records its exact visual rules, and identifies the official assets. Each prompt contains
the applicable colors, typography, logo treatment, imagery rules and exact text, alongside
concrete composition instructions. Website observations do not become approved brand rules.

The agent checks the prompt against the kit. When you return a generated image, it checks
the result and writes targeted corrections. See [the brand-kit workflow](docs/brand-kit-workflow.md).
The balanced visual style above applies only within the client's brand rules.

## First-time setup

1. Give the agent this repository or skill pack and your content request.
2. Make a copy of the current Google Sheet template below.
3. Fill only the starting brief in **01 Brand**: nine core answers and three optional answers. “Not sure—please help” is acceptable.
4. Share one approved brand-kit/asset-folder link, or select “No brand kit yet”. No need to transcribe fonts or colors.
5. Give the operator access to your copy and linked files, and send the copied Sheet link back. Use `BOOTSTRAP_PROMPT.md` when starting a fresh agent session.
6. The agent reads your sources, fills designated agent sections and asks a short grouped follow-up only for essential gaps. Empty optional tabs do not block work.
7. The agent prepares the requested package. Review copy, image prompts and suggested posting times in **07 Content Plan**; detailed columns expand when needed.

The agent proposes a visual direction for approval when no kit exists. Clear, already approved information does not need a second confirmation round.

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

Use this live Google Sheet as the canonical onboarding template. The bundled `Universal_Content_Writer_Template.xlsx` is the legacy detailed layout and does not include the simplified starting page.

The client should make a copy for their company and keep the fixed tab names and headers. The owner must grant the intended client viewing access if the master is restricted; sharing a URL does not grant access.

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
