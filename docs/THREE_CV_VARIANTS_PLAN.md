---
title: Three Targeted CV Variants Plan
createdAt: "2026-09-23"
updatedAt: "2026-09-23"
status: complete
---

# Three Targeted CV Variants Plan

## Objective

Create three evidence-based CV source variants in `resume-builder` for distinct role families, while preserving `source/canon-resume/` intact:

1. **Frontend Engineer — React/TypeScript**
2. **Product Engineer — UX and workflows**
3. **Frontend Technical Lead — hands-on technical leadership**

These are separate content projections, not changes to the builder's existing `ats` and `grouped` output profiles. Each source variant can be rendered with either output profile.

## Implementation result

Created and rendered:

- `source/cv-frontend-react-typescript/`
- `source/cv-product-engineer-ux/`
- `source/cv-frontend-technical-lead/`

All three variants render as two-page ATS-profile DOCX files using the existing builder. `source/canon-resume/` remains byte-for-byte unchanged from the captured pre-implementation checksums. The React variant states that recent product work is SwiftUI; the Product Engineer variant leads with Alfred and workflow examples; the Technical Lead variant emphasizes hands-on technical direction and does not claim people-management duties. CDP Status Checker and the unresolved UNBOX name history were not projected as established claims.

## Boundaries and authority

- Treat `source/canon-resume/` as immutable during this work. Do not edit, rename, reformat, or relocate its files.
- Create each variant as an independent section-based source directory under `source/`, initially copied from the canonical CV and then selectively edited for the target role.
- Do not introduce separate global profiles, schemas, templates, or new builder behavior unless implementation reveals a concrete need.
- Use the accepted Career knowledge and source reviews in CognitiveOS as evidence references. Do not copy unreviewed claims into a variant as established facts.
- Keep candidate claims, self-reported outcomes, and unresolved facts clearly qualified or omit them.
- Do not lengthen variants to preserve every role. Use relevance and current CV conventions to decide whether older entries are compressed or omitted.
- Variant source creation has been executed under this plan. Further edits remain subject to review against evidence and target-role needs.

## Target positioning

| Variant | Primary hiring question | Lead evidence | Main gap to state honestly |
|---|---|---|---|
| `frontend-react-typescript` | Can this candidate deliver and maintain production frontend applications with React and TypeScript? | Signal React/TypeScript delivery and Gamesys/Bally's commercial frontend, components, APIs, tests, and production workflows. | Recent hands-on work is SwiftUI. Alfred demonstrates current UI engineering but does not establish recent React/TypeScript proficiency. Do not imply otherwise. |
| `product-engineer-ux` | Can this candidate understand user workflows and deliver useful product experiences end to end? | Alfred flows and native app implementation; Signal's self-service template workflow; Gamesys authoring/preview tools; HSBC portal and test-authoring case study. | No documented Alfred user validation, adoption, or market outcomes. CDP Status Checker UX/Figma/implementation ownership remains user-reported pending artifacts. |
| `frontend-technical-lead` | Can this candidate provide hands-on technical direction and improve frontend delivery across a team or platform? | Formal Bally's Frontend Tech Lead role; architecture, standards, technical-debt mapping, onboarding, mentoring, developer tooling, and roadmap/delivery input. | Evidence supports technical leadership, not yet formal people management such as hiring, performance reviews, or line-management accountability. |

## Content rules by variant

### Frontend Engineer — React/TypeScript

- Put React/TypeScript employment evidence before Alfred; emphasize production frontend delivery, component maintenance, API integration, data-rich UI, testing, and code quality.
- Use Alfred to show current engineering activity and transferable UI skills, labelled Swift/SwiftUI.
- Keep technical-lead material concise and tied to frontend quality and delivery.
- Compress UNBOX and older GPAC/HSBC material to relevant frontend/product evidence; do not imply that historical Flash/ActionScript or older web-stack experience is current.
- Consider a short learning/current-practice entry only if the user supplies verifiable recent React/TypeScript work; do not invent a skills-refresh project.

### Product Engineer — UX and workflows

- Lead with product framing, user flows, workflow outcomes, and cross-functional delivery rather than architecture breadth alone.
- Give Alfred the clearest recent UX/UI-from-scratch treatment, while retaining the documented no-validation/no-adoption boundary.
- Select Signal, Gamesys, and HSBC examples that show what users, administrators, designers, or content teams could do more effectively.
- Describe design judgment and collaboration without claiming a UX Designer or visual-design-specialist role.
- Treat CDP Status Checker design scope, UNBOX's sustained UX duration, and any unsourced personal ownership as pending corroboration.

### Frontend Technical Lead

- Foreground the formal Frontend Tech Lead title and bounded 11/2022–11/2023 period.
- Select a small number of concrete examples covering technical direction, frontend standards, architecture/technical-debt analysis, onboarding, mentoring, and delivery systems.
- Retain hands-on implementation evidence to avoid implying a move into management-only work.
- Distinguish technical leadership from people management; omit hiring, performance management, or direct-report claims unless separately evidenced.
- Reduce older role detail while retaining progression and only the strongest context needed to establish breadth.

## Shared evidence and claim controls

- Keep dates, formal titles, and accepted role identities aligned with CognitiveOS accepted Career records and the existing canonical CV.
- Prefer the accepted Gamesys/Bally's and Signal contribution wording for shared ownership and measured outcomes; do not convert repository statistics into impact metrics.
- The HSBC 2006 portfolio supports a portal redesign, layout/programming, a question-bank authoring workflow, and interactive e-learning. The source reports a numerical speed change and delivery duration, but CognitiveOS review says the numerical measure is unverified and the dates are unavailable; omit those metrics/timing unless corroborated.
- UNBOX's company-name sequence and sustained UX emphasis, GPAC's approximate six-year agency total and creative-team collaborators, and CDP Status Checker design ownership require confirmation/artifacts before stronger external claims.
- Do not infer hiring outcomes, age bias, overqualification, or role mismatch as facts. Variants are an application experiment, not a conclusion about why prior applications were rejected.

## Proposed source layout

```text
source/
  canon-resume/                       # preserve intact
  cv-frontend-react-typescript/
    meta.md
    sections/
      summary.md
      core-skills.md
      professional-experience.md
      education.md
  cv-product-engineer-ux/
    ... same section contract ...
  cv-frontend-technical-lead/
    ... same section contract ...
```

The new directories should follow the existing required section contract. Keep `selected-project.md` out unless a variant has a specific, high-value project that merits a dedicated section and the parser already supports it.

## Phases

1. **Evidence lock and claim matrix:** Map each proposed bullet to canonical CV content, accepted Career knowledge, source review, or explicitly user-reported input. Mark each as ready, needs confirmation, or omit.
2. **Variant outlines:** Decide each version's summary, skills emphasis, role ordering/detail, length target, and treatment of older roles before drafting full prose.
3. **Create source copies:** Copy the canonical source structure to the three new directories. Do not touch `canon-resume`.
4. **Draft variants:** Tailor summary, skills, and experience independently under the shared evidence and claim controls. Preserve consistent dates, titles, and ownership boundaries.
5. **Review cross-variant consistency:** Check facts across all three, remove unsupported duplication or contradictory claims, and verify each version answers its target hiring question.
6. **Render and inspect:** Generate ATS and grouped output as useful, inspect layout and length, and check the generated documents against their Markdown sources.
7. **Validation and handoff:** Run the project-required tests, lint, format, compile, and whitespace checks after implementation. Report files changed and any evidence claims still held back.

## Acceptance criteria

- `source/canon-resume/` is byte-for-byte unchanged from the pre-implementation baseline.
- Three complete, independently renderable section-based source directories exist with target-specific metadata and content.
- Each variant has a distinct, accurate positioning and no unsupported skill, title, metric, ownership, or people-management claim.
- The React/TypeScript variant makes the SwiftUI-versus-React recency distinction clear.
- The Product Engineer variant presents UX and workflow evidence without claiming specialist UX credentials or undocumented product validation.
- The Technical Lead variant demonstrates hands-on technical leadership without implying formal people management.
- All variants are concise relative to the target; older history is included only where it adds relevant evidence.
- Required repository validation passes and generated outputs are visually reviewed.

## Remaining decisions for application tailoring

- Confirm whether the CVs should share one visual style and output format or whether each needs different layout treatment.
- Confirm a target length (recommended starting point: two pages each, with a justified exception only if a version cannot preserve important evidence within that limit).
- Confirm whether to include a compressed UNBOX entry in all three variants or omit it selectively in the React-focused application CV.
- Resolve or explicitly defer the UNBOX name history and CDP Status Checker evidence before projecting those claims.
