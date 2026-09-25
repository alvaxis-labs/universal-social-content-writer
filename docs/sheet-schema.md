# Google Sheet Schema

The client maintains one Google Sheet with these fixed tabs:

1. `01 Brand`
2. `02 Audience`
3. `03 Voice & Style`
4. `04 Product Offering`
5. `05 Content Strategy`
6. `06 Competitors & References`
7. `07 Content Plan`
8. `08 Knowledge & Claims`

Do not rename tabs or headers.

## Ownership model

### Client-owned
The client owns and maintains:

- brand/company information
- audiences
- voice/TOV preferences
- product facts and product status
- approved strategy
- competitor/reference seeds
- content briefs
- approved claims
- constraints/compliance notes
- approval decisions

The agent should not silently overwrite these fields.

### Agent-owned
The agent may maintain:

- research decisions
- research notes
- source links
- competitor observations
- terminology findings
- writer angle/rationale
- drafts
- self-review
- verification notes
- draft status
- final copy when approved/requested
- last-updated fields

## Tab purpose

### 01 Brand
Core company identity, category, positioning, differentiators, business goals, marketing goals, markets, priorities, and constraints.

### 02 Audience
Audience segments, knowledge level, motivations, pain points, objections, attention triggers, and desired action.

### 03 Voice & Style
Brand personality, tone, writing style, language preferences, banned language, platform notes, and positive/negative content references.

### 04 Product Offering
Products, services, features, offers, status, mechanics, benefits, differentiators, target audiences, links, and limitations.

### 05 Content Strategy
Approved content pillars, purpose, audience, messages, topics, formats, platform fit, frequency/share, CTAs, evidence requirements, and do-not-do rules.

### 06 Competitors & References
Client-selected competitors and creative references plus agent research on positioning, TOV, recurring themes, strong formats, recent examples, and sources.

### 07 Content Plan
The operational client-to-writer board. Client supplies the brief; the agent records research decision, sources, improved angle, draft, self-review, status, and final copy.

### 08 Knowledge & Claims
Reusable terminology, product/company facts, statistics, marketing claims, compliance rules, approved wording, permissions, sources, and verification status.

## Baseline relationship

The Sheet is authoritative. Baselines are compressed caches.

Refresh `company_baseline.md` only when material recurring context changes, such as positioning, audience, TOV, products, strategy, claims, terminology, constraints, or reference set.

A new Content Plan row alone does not require a baseline rebuild.

## Visual prompts and complete content packages

Use the existing columns. No workbook migration or new tab is required.

| Existing Content Plan field | Content package use |
| --- | --- |
| Writer Angle / Rationale | Angle, format choice, visual concept, and why it supports the objective |
| Draft | Labeled post copy, on-image copy, suggested AI image prompt(s), panel outline, suggested posting time with time zone and rationale, and assembly notes as relevant |
| Research Notes / Sources | Verified claims, source links, and relevant reference asset links |
| Writer Self-Review | Copy/prompt consistency, verification limits, and missing asset dependencies |
| Draft Status | Actual writing/review stage; a suggested prompt does not mean a visual exists |
| Final / Published Copy | Approved/requested final post copy; keep image-tool instructions in Draft |

Read the target row before editing. Preserve unrelated content and existing drafts unless
revision or replacement is requested. If there is no dedicated prompt section, append a
clearly labeled section to the agent-owned Draft cell. On revision, update only the relevant
section. Avoid replacing formulas or writing entire rows when a specific cell is sufficient.

Do not overwrite `Date / Slot`, `Client Approval`, client briefs, or required assets. A suggested time belongs in a labeled `Suggested posting time` section of Draft; it does not replace the client schedule. Do not put a prompt
in `Publish / Post URL` or mark a suggestion as an approved image. If Sheet access is
unavailable, return the same labeled package for manual pasting and report that limitation.

Approved visual preferences can be read from relevant existing Voice & Style entries and
asset references. Keep inferred directions labeled as suggestions in agent notes. Refresh
only the affected company baseline section when approved visual guidance changes.
