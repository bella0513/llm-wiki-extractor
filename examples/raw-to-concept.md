# Example: Raw To Concept

## User Prompt

```text
[$llm-wiki-extractor] Extract reusable knowledge from this meeting note. First decide whether it should enter the wiki. Do not edit files yet.
```

## Raw Material

```text
We reviewed the onboarding project. New hires struggled because mentors answered questions differently. The team agreed to create a checklist for mentors: role expectations, first-week tasks, escalation rules, and common mistakes. HR will draft it next week.
```

## Extraction Decision

This raw note should not be copied into the wiki as a meeting record.

It contains reusable Tool knowledge:

- ICPT: Tool
- Tool type: Standard + Sensing
- Reusable object: mentor onboarding checklist

## Recommended Wiki Action

Update an existing onboarding, mentoring, or training concept page if one exists.

Create a new concept page only if no existing page can hold the checklist.

## Candidate Concept Shape

```markdown
---
title: Mentor Onboarding Checklist
type: concept
knowledge_form: Tool
tool_type: Sensing
source_path: path/to/raw-note
updated: YYYY-MM-DD
---

# Mentor Onboarding Checklist

## Definition
> A checklist that helps mentors give consistent guidance to new hires during onboarding.

## Use Task
- Standardize mentor support for new hires.

## Key Points
- Role expectations
- First-week tasks
- Escalation rules
- Common mistakes

## Related Concepts
- Existing onboarding or mentoring pages only if they exist.
```

## Lint Checks

- Does the related onboarding page already exist?
- Are all links real?
- Did we avoid copying the meeting note?
- Did we record the source?
