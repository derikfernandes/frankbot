# Building Frankbot

Frankbot is a **skill-spec project**: the product must be built from specifications, tests and Agent Skills, not from loose prompts.

Use this repository as the source of truth when working in an AI IDE such as Cursor, Google AI Studio, Codex, Windsurf or any other coding agent.

The first implementation target is a frontend that helps the user operate the Frankbot workflow: choose a task, select or infer the right skill, provide documents or context, generate technical outputs, review quality and record learnings for future skills.

## Quick start

Give your coding agent this prompt:

```text
Build the Frankbot frontend.

You must work using the SSVC methodology: Skill-Spec Vibe Coding.

Rules:

1. Do not start by coding.
2. First read the project documentation.
3. Use the specs as the source of truth.
4. Use the skills as execution procedures.
5. Implement the smallest useful vertical slice first.
6. Every screen and feature must map to a spec, a user flow and an acceptance criterion.
7. Every final answer or generated artifact must include a skill-learning review.
8. If the existing skills are not enough, propose or create a new skill.
9. If an existing skill is insufficient, propose or apply an update to that skill.
10. Do not implement features outside the documented scope.

Read these files first:

- README.md
- specs/00_PROJECT_OVERVIEW.md
- specs/01_DOMAIN_MODEL.md
- specs/02_USER_FLOWS.md
- specs/04_OUTPUT_CONTRACTS.md
- specs/05_ACTION_ROUTING_MAP.md
- specs/07_ACCEPTANCE.md
- specs/08_OUT_OF_SCOPE.md
- specs/09_DECISIONS.md
- specs/TASKS.md
- specs/tests.yaml
- docs/padroes_notas_tecnicas.md
- docs/catalogo_skills.md

Then read the relevant skills:

- skills/leitura-processual/skill.md
- skills/analise-tecnica-controladoria/skill.md
- skills/redacao-relatorio-tecnico/skill.md
- skills/linguagem-institucional/skill.md
- skills/recomendacoes-e-encaminhamentos/skill.md
- skills/qa-controladoria/skill.md
- skills/skill-creator/skill.md
- skills/skill-reviewer/skill.md

Implement the first frontend version with these minimum screens:

1. Home / Project Overview
   - Explain what Frankbot does.
   - Explain that it works through specs and skills.
   - Show the main workflow.

2. New Analysis
   - Allow the user to describe the case.
   - Allow the user to choose the desired output type:
     - technical note;
     - technical report;
     - executive summary;
     - information request;
     - recommendations;
     - text review.
   - Allow the user to paste text or indicate uploaded documents.

3. Skill Router
   - Show the recommended main skill.
   - Show auxiliary skills.
   - Explain why each skill was selected.
   - If no skill fits, suggest using skill-creator.

4. Draft Output
   - Show the generated structure before final text.
   - Use the contracts from specs/04_OUTPUT_CONTRACTS.md.
   - For technical notes, follow docs/padroes_notas_tecnicas.md.

5. QA Review
   - Apply the checklist from skills/qa-controladoria/skill.md.
   - Classify the output as:
     - approved;
     - approved with notes;
     - needs revision.

6. Skill Learning
   - Always ask:
     - Was the skill sufficient?
     - Is a new skill needed?
     - Should an existing skill be updated?
     - Is a checklist, template, example or script needed?

Use a clean, institutional and modern interface.

Do not connect to external systems in the first version.
Use local mock data or static state if needed.
Do not create authentication in the first version.
Do not create backend integrations unless explicitly requested later.

After implementation, provide:

1. files created or changed;
2. specs used;
3. skills used;
4. tests or manual checks performed;
5. out-of-scope items avoided;
6. skill-learning review.
```

## What the coding agent should do

1. **Read the specs** — Understand the project objective, domain model, user flows, output contracts, acceptance criteria and decisions.
2. **Read the skill catalog** — Identify which skill is relevant to each feature.
3. **Read the selected skills** — Use the skill instructions to guide the implementation.
4. **Design the first vertical slice** — Build the smallest useful frontend flow.
5. **Implement incrementally** — One feature, one screen or one flow at a time.
6. **Verify against acceptance criteria** — Compare implementation with specs and tests.
7. **Record skill learning** — Every task must end by checking whether skills need to be created or improved.

## Files

| File | Purpose |
|---|---|
| README.md | Project summary and core rules |
| INSTALL.md | Instructions for AI IDE implementation |
| specs/00_PROJECT_OVERVIEW.md | Project objective and problem definition |
| specs/01_DOMAIN_MODEL.md | Core concepts and entities |
| specs/02_USER_FLOWS.md | Main user flows |
| specs/03_KNOWLEDGE_MODEL.md | Knowledge layers used by Frankbot |
| specs/04_OUTPUT_CONTRACTS.md | Required output structures |
| specs/05_ACTION_ROUTING_MAP.md | Action-to-skill routing map |
| specs/06_INTEGRATIONS.md | Integration rules and future integrations |
| specs/07_ACCEPTANCE.md | Acceptance criteria |
| specs/08_OUT_OF_SCOPE.md | What must not be implemented yet |
| specs/09_DECISIONS.md | Architectural and product decisions |
| specs/TASKS.md | Execution roadmap |
| specs/tests.yaml | Language-agnostic behavior checks |
| docs/padroes_notas_tecnicas.md | Patterns extracted from model technical notes |
| docs/catalogo_skills.md | Skill catalog |
| skills/*/skill.md | Execution procedures for each skill |

## First frontend scope

The first frontend should not try to be the full Frankbot platform.

It should be a guided interface for using the methodology.

Minimum scope:

```text
Home
→ New Analysis
→ Skill Router
→ Draft Structure
→ QA Review
→ Skill Learning
```

The frontend should make the methodology visible. The user should always understand:

- what is being produced;
- which skill is being used;
- which spec is being followed;
- what acceptance criteria apply;
- whether a new skill is needed;
- whether an existing skill must be improved.

## Suggested UX behavior

### Home

Show the central concept:

```text
Frankbot codifies the work method of a highly skilled Controladoria analyst.
```

Show the workflow:

```text
Case → Skill Selection → Technical Analysis → Draft → QA → Skill Learning
```

### New Analysis

Collect:

- title;
- case description;
- output type;
- target audience;
- available sources;
- sensitivity level;
- optional pasted text.

### Skill Router

Map output type to skills:

| Output type | Main skill | Auxiliary skills |
|---|---|---|
| technical note | redacao-relatorio-tecnico | analise-tecnica-controladoria, linguagem-institucional, qa-controladoria |
| technical report | redacao-relatorio-tecnico | leitura-processual, analise-tecnica-controladoria, qa-controladoria |
| executive summary | linguagem-institucional | redacao-relatorio-tecnico, qa-controladoria |
| information request | recomendacoes-e-encaminhamentos | linguagem-institucional, qa-controladoria |
| recommendations | recomendacoes-e-encaminhamentos | analise-tecnica-controladoria, qa-controladoria |
| text review | linguagem-institucional | qa-controladoria |

If no route fits, use:

```text
skill-creator
```

### Draft Structure

Show an outline before generating full text.

For technical notes, prefer:

```text
1. Introducao
2. Metodologia
3. Analise
4. Solucoes sugeridas
5. Recomendacoes
6. Limitacoes da analise
```

For reports, use the contract in `specs/04_OUTPUT_CONTRACTS.md`.

### QA Review

Use the following checks:

- Does it answer the objective?
- Does it separate fact from inference?
- Does it avoid unsupported conclusions?
- Does it identify gaps?
- Does it include actionable recommendations?
- Does it respect out-of-scope rules?
- Does it include skill-learning review?

### Skill Learning

Every flow must end with:

```text
Skill used:
- [name]

Was the skill sufficient?
- Yes/No

What was missing?
- [description]

New skill needed?
- Yes/No

Recommended update:
- none / update existing skill / create checklist / create template / create example / create script / create new skill
```

## Implementation rules

### Do

- Build from specs.
- Keep screens simple.
- Use clear labels.
- Make skill routing explicit.
- Show acceptance criteria in the interface.
- Keep out-of-scope items blocked or marked as future.
- Prefer static mocked flows in the first version.
- Register assumptions in the UI or code comments.

### Do not

- Do not add login/authentication yet.
- Do not connect to municipal systems yet.
- Do not create a database unless requested later.
- Do not generate PDF/DOCX in the first version unless requested later.
- Do not hide skill selection from the user.
- Do not skip QA.
- Do not skip skill-learning review.
- Do not implement features not described in specs.

## Suggested first task for the AI IDE

Use this as the first implementation task:

```text
Implement the first vertical slice of the Frankbot frontend.

Stack decision:
- If the project has no stack yet, use a simple React + TypeScript + Vite frontend.
- Use local state only.
- No backend.
- No authentication.
- No external integrations.

Build these screens:

1. Home
2. New Analysis
3. Skill Router
4. Draft Structure
5. QA Review
6. Skill Learning

Read and follow:

- INSTALL.md
- README.md
- specs/00_PROJECT_OVERVIEW.md
- specs/02_USER_FLOWS.md
- specs/04_OUTPUT_CONTRACTS.md
- specs/05_ACTION_ROUTING_MAP.md
- specs/07_ACCEPTANCE.md
- specs/08_OUT_OF_SCOPE.md
- specs/09_DECISIONS.md
- docs/padroes_notas_tecnicas.md
- docs/catalogo_skills.md

Do not implement anything outside this scope.

At the end, report:

1. files changed;
2. specs followed;
3. skills used;
4. checks performed;
5. risks;
6. skill-learning review.
```

## Verification

After the frontend is implemented, verify manually:

- The app shows what Frankbot is.
- The app lets the user start a new analysis.
- The app recommends a main skill and auxiliary skills.
- The app shows a draft structure based on the selected output type.
- The app includes a QA checklist.
- The app includes a skill-learning step.
- The app does not include login, backend, database or external integrations.
- The app respects the out-of-scope file.

If tests are added, they should check at least:

- output type maps to the correct main skill;
- technical note uses the correct outline;
- QA checklist is displayed;
- skill-learning fields are required;
- out-of-scope features are not present.

## Why this works

Traditional vibe coding starts with a broad prompt and lets the agent improvise.

Frankbot must work differently.

The value of the project is not only the frontend code. The value is the documented work method: specs, skills, tests, templates and continuous skill improvement.

The frontend is only an interface over this method.

The code can change. The specs and skills are the source of truth.
