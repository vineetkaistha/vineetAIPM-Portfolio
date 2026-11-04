# AI Product Management Portfolio — Working Context

## Purpose of this document

Use this file as the source of truth when planning, writing, or building an AI
Product Management (AI PM) portfolio from this repository. It explains what
exists today, what the portfolio should demonstrate, and which details still
need to come from the portfolio owner.

This is a working brief, not a claim that the portfolio website or AI products
have already been built.

## Portfolio goal

Create a credible, easy-to-navigate portfolio that helps a hiring manager,
product leader, or collaborator assess the owner's ability to identify valuable
problems and lead AI-enabled products from discovery through delivery and
measurement.

The portfolio should demonstrate product judgment, not just familiarity with
AI terminology or the ability to produce polished mockups. It should show how
the owner:

- Connects customer needs to business outcomes.
- Decides whether AI is appropriate, and identifies a simpler non-AI baseline.
- Turns uncertainty into testable requirements and experiments.
- Partners with engineering, design, data, legal, security, and operations.
- Evaluates quality, safety, reliability, latency, and cost.
- Defines launch criteria, human oversight, monitoring, and iteration.
- Communicates trade-offs and learns from measured outcomes.

## Current repository: verified facts

This repository is currently a small, dependency-free browser game project. It
is not yet an AI product or a portfolio website.

### Memory Game

- `memory-game.html` is a responsive card-matching game implemented with
  standard HTML, CSS, and browser JavaScript in one file.
- It supports 4x4 and 6x6 grids, a timer, moves, ratings, a completion dialog,
  keyboard interaction, and saved best scores.
- It includes light and dark themes. Theme preference and game scores use
  separate local-storage keys.
- `PRD_dark_theme.md` documents the dark-theme requirements and acceptance
  criteria.

### Snake

- `snake-game.html` is a standalone Snake game implemented with standard HTML,
  CSS, and browser JavaScript in one file.
- It supports keyboard and touch controls, pause/resume/restart, scoring,
  best-score persistence, increasing speed, and responsive presentation.
- `PRD_snake.md` documents its intended requirements and acceptance criteria.

### Repository documentation

- `README.md` explains how to open and play the games.
- `read.me` is the AI PM portfolio setup guide.
- This file (`context.md`) is the working context for future portfolio work.

### Evidence boundary

The game source and PRDs can demonstrate small-scale product definition,
acceptance criteria, accessibility considerations, interaction design, and
implementation constraints. They do not, on their own, establish:

- That either game uses AI or machine learning.
- Professional AI PM experience, team leadership, or production ownership.
- User research, user counts, business impact, conversion, retention, or other
  outcome metrics.
- The identity, industry experience, or career history of the portfolio owner.

Do not present unsupported claims as facts. Treat these games as prototype or
product-execution examples unless the owner supplies additional evidence.

## Intended audience

Primary audience:

- Hiring managers and product leaders evaluating AI Product Manager candidates.
- Cross-functional partners assessing how the owner reasons about AI product
  opportunities and delivery risks.

They need to understand quickly:

1. What kinds of problems the owner can solve.
2. How the owner makes product decisions under uncertainty.
3. What the owner personally contributed.
4. What evidence supports the stated results.
5. How the owner balances user value, business value, and responsible AI.

## Positioning and personal information

Do not invent personal details. Obtain these from the owner before publishing:

- Preferred name, professional title, and location/time zone if desired.
- Target role level, industries, and geography.
- Career summary, employment history, and education or credentials.
- Products shipped, team scope, responsibilities, and dates.
- Public contact details, links, and preferred call to action.
- Approved portfolio projects, artifacts, and outcome metrics.
- Confidentiality boundaries and permission to discuss past work.

Until confirmed, use clearly marked placeholders such as `[Preferred name]`,
`[Target role]`, or `[Verified outcome]`, and keep them out of public-facing
claims.

## Recommended portfolio structure

The eventual portfolio can be a small static site or a carefully structured
GitHub repository. Keep the first version focused:

1. **Home** — concise positioning, intended role, strongest proof points, and
   links to two or three selected case studies.
2. **Case studies** — detailed problem framing, decisions, execution, results,
   and learning.
3. **Product approach** — a short explanation of the owner's discovery,
   experimentation, delivery, and measurement practices.
4. **About** — verified professional background and working style.
5. **Contact** — owner-approved contact channel and professional links.

Potential repository organization once there is enough material:

```text
portfolio/
  README.md
  context.md
  index.html                 # If a static site is built
  case-studies/
    [project-slug].md
  artifacts/
    diagrams/
    prototypes/
  assets/
```

Do not move or rename the existing game files just to match this proposed
structure. Decide separately whether the games belong in a portfolio repository
or should remain in their current project repository.

## Case-study standard

Each published case study should distinguish the owner's direct work from team
work and cover the following:

1. **Snapshot** — product, domain, dates, status, audience, and the owner's role.
2. **Problem** — user, unmet need, context, and why it mattered.
3. **Evidence** — research, data, support signals, or assumptions; state the
   source and limitations.
4. **Opportunity and strategy** — target outcome, alternatives, and why this
   direction was chosen.
5. **AI suitability** — why AI is useful, what a non-AI baseline would do, and
   where deterministic rules are preferable.
6. **Requirements and experience** — workflows, success criteria, edge cases,
   accessibility, and failure handling.
7. **Solution and system boundaries** — model or service role, data inputs,
   retrieval/tools if applicable, UI, human review, and dependencies. Include
   only details the owner is authorized to share.
8. **Evaluation** — offline and online measures, representative test cases,
   quality thresholds, safety checks, and known limitations.
9. **Delivery and collaboration** — decisions, sequencing, stakeholders,
   risks, launch plan, and the owner's personal contribution.
10. **Outcomes** — baseline, target, measured result, time period, and source.
    If no product was launched, label results as prototype or experiment
    findings, not production impact.
11. **Reflection** — what changed, what did not work, and what the owner would
    do next.

For AI features, choose measures that fit the product. Possible categories
include task success, groundedness or answer correctness, harmful-output rate,
human escalation or override rate, latency, cost per successful task, adoption,
and user trust. Do not list a metric as achieved unless it was actually
measured and can be explained.

## Responsible AI expectations

For any AI case study, document relevant risks and mitigations, including:

- Data privacy, consent, retention, access, and sensitive information.
- Incorrect, ungrounded, biased, or harmful outputs.
- Prompt injection or unsafe tool/data access where applicable.
- User disclosure, uncertainty communication, and appeal or correction paths.
- Human review and escalation for consequential or ambiguous cases.
- Evaluation coverage, monitoring, incident response, and rollback criteria.
- Accessibility, language coverage, and differences across user groups.

Risk treatment should be proportional to the product and domain. Avoid claiming
that a system is “safe,” “bias-free,” or “hallucination-free.”

## Content and presentation principles

- Prefer clear, direct language over buzzwords.
- Make the problem and decision visible before describing the technology.
- Use diagrams, screenshots, and prototypes only when they clarify real work.
- Explain trade-offs, rejected options, and limitations.
- Label hypothetical, educational, prototype, and production work accurately.
- Redact customer, employer, and personal data unless disclosure is authorized.
- Make pages readable on mobile and accessible by keyboard and screen reader.
- Keep claims concise and make evidence easy to inspect.

## Suggested initial project mix

The current games can demonstrate product execution, but an AI PM portfolio
will be stronger with evidence that directly addresses AI product decisions.
Possible future work, clearly labeled as self-directed if it is not professional
experience:

- A retrieval-based knowledge assistant with citations, abstention, and
  evaluation for answer quality.
- A support-agent copilot with human approval, escalation, and measurable
  resolution-time and quality goals.
- An AI workflow discovery brief comparing automation, augmentation, and a
  non-AI alternative.

Choose projects based on the owner's target roles and real domain knowledge.
Avoid building a demo solely to claim AI experience; include a realistic user
problem, a quality evaluation plan, and explicit risk handling.

## Instructions for future AI collaborators

- Treat this document as context, not as permission to invent missing facts.
- Ask for owner-provided career details and evidence when a claim depends on
  them.
- Keep the game projects separate from AI case studies unless an actual AI
  component is added and documented.
- When writing a case study, identify whether work is professional,
  self-directed, hypothetical, prototype, or production.
- Preserve confidentiality; do not copy credentials, customer data, or
  proprietary details into public artifacts.
- Keep claims and metrics traceable to owner-approved evidence.
- Before publishing, check links, mobile layout, accessibility, and spelling.

## Open inputs for the portfolio owner

- What roles, seniority levels, and industries are you targeting?
- Which professional projects can you discuss publicly?
- What was your role and what decisions did you personally own?
- What verified outcomes or artifacts can you share?
- Do you have AI product work, experiments, or relevant learning to include?
- Should this portfolio be a website, a GitHub-first portfolio, or both?
- Should the existing game projects be included, linked, or kept separate?
- What tone, visual style, and contact method do you prefer?
