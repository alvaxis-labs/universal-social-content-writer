# Universal Social Content Writer

A reusable content planning, writing, and creative direction skill for **X/Twitter and Facebook**. It produces written content, copy-paste AI image prompt suggestions, and suggested posting times.

The client downloads a short intake workbook, fills it in, and uploads it with approved brand references. The agent returns a completed Excel workbook. No Google Drive connection is required.

## Architecture

- **`SKILL.md`**: universal operating instructions for the agent. Never store client-specific information here.
- **Latest client workbook and uploaded assets**: source of truth for the brief, approved brand rules, facts and feedback. Google Sheets is optional.
- **`company_baseline.md`**: agent-generated compressed company context for recurring work.
- **`research_baseline.md`**: optional agent-generated durable market/category research.

The latest supplied workbook and explicit client corrections take precedence over cached baselines.

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

1. Give the agent this skill pack and say what content you need. You do not need a Sheet URL.
2. The agent first gives you [Client Intake Template.xlsx](assets/Client_Intake_Template.xlsx), unless you already supplied enough context.
3. Fill the yellow answers, save the workbook and upload it with your brand kit/assets. Optional answers may stay blank; “Not sure—please help” is valid.
4. The agent reads your materials and asks only about essential missing details. If no kit exists, it proposes a direction for approval.
5. Receive a downloadable `.xlsx`: **Content Calendar**, **Post Content**, and **Image Prompts**, connected by **Post ID**. Captions and image prompts have their own cells.
6. To revise, upload your latest workbook with feedback. The agent returns a new version preserving unchanged work and your decisions.

Use [BOOTSTRAP_PROMPT.md](BOOTSTRAP_PROMPT.md) for a fresh session. See [the file workflow](docs/file-workflow.md) for output fields and delivery rules. Uploading files shares those files with the AI; it does not grant access to your Drive.

## Optional Google Sheets route

Choose this explicitly if you want the agent to work in a connected Sheet. The [Google template](https://docs.google.com/spreadsheets/d/1MYlCFQZYjfnFfNlWqQ9idDWg1jBpaDZCr6AjkfzzbgQ/edit) and [existing schema](docs/sheet-schema.md) remain supported. Account access and write permissions are separate from skill installation.

`Universal_Content_Writer_Template.xlsx` is the legacy eight-tab template. Use `assets/Client_Intake_Template.xlsx` for new file-based onboarding. Do not require clients to fill all legacy tabs.

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
