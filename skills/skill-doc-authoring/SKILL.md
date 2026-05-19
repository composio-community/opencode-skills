---
name: skill-doc-authoring
description: Write a well-formed agent SKILL.md from a workflow, SOP, or repeated procedure. Use when the user wants to "create a skill", "turn this process into a skill", "document this workflow as a skill", or asks why a skill isn't triggering.
---

# Skill Doc Authoring

Produce a single valid `SKILL.md` that an agent will actually trigger and follow. The two failure modes this prevents: skills that never fire (weak description) and skills that fire but don't help (vague body).

## File contract

- Directory name and `name:` MUST match, lowercase, hyphens only, ≤ 64 chars.
- Filename MUST be exactly `SKILL.md` (case-sensitive).
- Frontmatter has exactly two keys: `name`, `description`. `description` ≤ 1024 chars.

```
skills/<skill-name>/SKILL.md
```

## The description is the trigger

The agent decides whether to load the skill from the `description` alone. Write it in third person, lead with what it does, then **"Use when …"** with concrete user phrasings and situations. Include the trigger words a user would actually type.

- Weak: `Workflow for handling data.`
- Strong: `Validate and clean CSV exports before import. Use when the user uploads a CSV, mentions "dirty data", or asks to "prep this for the database".`

State when **not** to use it if a sibling skill is close — overlapping triggers cause the wrong skill to fire.

## Body structure

Write for an agent with no project context. Concise, imperative, decision-oriented.

```
# Title
One-line purpose.
## When to use            # + when not to
## Procedure / The loop   # numbered, concrete, with commands
## Quality bar            # how to know it's done right
## Anti-patterns          # the tempting wrong moves
```

Rules:
- Imperative voice ("Run X", "Verify Y"), not "the agent should consider".
- Every step is verifiable or has a concrete command/example.
- Cut "Notes", "Overview" padding, and restatements. If a line doesn't change what the agent does, delete it.
- Put long reference material (schemas, tables, scripts) in sibling files and link them; keep `SKILL.md` skimmable (aim < ~200 lines).

## Procedure

1. Extract the real procedure from the user (the SOP, the steps they actually take, the decisions and their criteria).
2. Identify triggers: what does someone say/do right before this skill is needed?
3. Draft the description (trigger test: would it fire on those phrasings? would it *not* fire on unrelated ones?).
4. Write the body to the structure above.
5. Validate: filename, name/dir match, frontmatter keys, description length.
6. Dry-run mentally: give the skill to a context-free agent on 2–3 sample requests — does it know exactly what to do?

## Anti-patterns

- Generic skeleton (Overview → "This skill enables…" → bulleted nouns → Notes) that fits any topic and helps with none.
- Description that describes the domain but never says *when* to fire.
- Restating general best practice the model already knows instead of the user's specific procedure.
- One giant `SKILL.md` where a script + a short doc would serve better.
