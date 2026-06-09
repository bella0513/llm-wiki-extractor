# Extraction Framework

The goal of extraction is not to create a Markdown page. The goal is to identify reusable knowledge objects and connect them to the existing knowledge network.

## Decision Flow

```text
raw material
-> What work task does it serve?
-> What steps, actions, and decisions appear?
-> What reusable knowledge object exists?
-> ICPT classification
-> Existing page or new page?
-> Network updates
-> Lint
```

## ICPT

| Type | Main Question | Default Treatment |
| --- | --- | --- |
| Information | What happened? | Keep raw unless stable and reusable. |
| Concept | What is it? | Extract when boundaries are clear. |
| Principle | Why does it work? | Extract when it supports judgment. |
| Tool | How do we do it? | Extract first when reusable. |

## Tool Knowledge Types

Tool knowledge is usually the highest-value extraction target because it helps people or AI agents act.

| Type | Signals | Examples |
| --- | --- | --- |
| Standard | factors, scoring, criteria, boundaries | evaluation rubric, classification rule |
| Sensing | checklists, data fields, diagnostic clues | interview checklist, research frame |
| Plan | stages, steps, timeline, resources | project playbook, rollout plan |
| Countermeasure | scenario and response | risk playbook, exception handling |

## Wiki Action Choices

Choose one of these actions:

- **Keep raw only**: one-time facts, todos, meeting process, project progress.
- **Update existing concept**: existing page can absorb a new rule, example, source, or clarification.
- **Create new concept**: a stable reusable object exists and no existing page can hold it.
- **Update MOC**: topic structure, source list, or exploration questions changed.
- **Update person page**: the person has durable value to the knowledge system.
- **Route to outputs**: the material is a deliverable, report, speech, course, policy, or business draft.

## Closure Criteria

Extraction is complete only when the agent checks the surrounding network:

- page has required metadata and useful sections;
- MOC and INDEX are considered;
- related concepts use real links;
- sources are recorded;
- status or queue is updated if the knowledge base uses one;
- lint or manual health checks are done.

If the agent can only create a single Markdown page but cannot maintain the network, it should not perform bulk extraction.
