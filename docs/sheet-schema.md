# Google Sheets Intake and Optional Write-Back Schema

The Google template is the default intake. Its eight tabs are not mandatory client homework. Finished content defaults to a downloadable Excel package; see [file-workflow.md](file-workflow.md). The write-back instructions below apply only when the user explicitly requests connected Google Sheets output.

Default intake template: https://docs.google.com/spreadsheets/d/1MYlCFQZYjfnFfNlWqQ9idDWg1jBpaDZCr6AjkfzzbgQ/edit

The client and agent use one client-owned Google Sheet with these fixed tabs:

1. `01 Brand`
2. `02 Audience`
3. `03 Voice & Style`
4. `04 Product Offering`
5. `05 Content Strategy`
6. `06 Competitors & References`
7. `07 Content Plan`
8. `08 Knowledge & Claims`

Do not rename tabs or headers.

## Starting page and progressive detail

The current master uses `01 Brand` as the only required client onboarding page. It asks for nine core answers and three optional answers, including one kit/folder link. Locate fields by their labels after reading the live Sheet; do not depend on row numbers. A client may also supply the equivalent information in conversation.

Detailed tabs remain available. The brand profile below the starting brief and the brand-rule extraction section in `03 Voice & Style` are explicitly marked **AGENT COMPLETES** and collapsed initially. Populate these from supplied sources, recording provenance and separating proposals from approved facts. Do not require clients to repeat information already in their kit.

`07 Content Plan` initially displays seven review columns. Other columns are grouped/collapsed, not removed. Read their actual headers and address existing cells without changing the client's view unnecessarily. `Draft` contains copy, image prompts and posting-time suggestions; `Client Approval` remains client-owned.

Older copies and the bundled legacy XLSX may have the original layout. Detect their actual labels and ownership before writing. Do not overwrite their client-owned fields just because a newer master assigns similar information to an agent section; use existing Agent Notes or obtain authorization for a migration.

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

- sourced details in explicitly agent-completed brand profile and brand-rule sections
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
