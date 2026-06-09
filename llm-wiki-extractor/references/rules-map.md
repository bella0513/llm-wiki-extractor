# Rules Map

This file explains when an agent should read deeper local rules. It does not define a universal directory structure.

Use the target knowledge base's own files whenever possible. The names below are examples of common rule categories, not required paths.

## Project Entry Rules

Read the project's `AGENTS.md`, README, schema, or operating guide when:

- entering a new knowledge base;
- deciding editable scope;
- checking whether raw materials are read-only;
- learning page types and link conventions;
- determining whether bulk edits are allowed.

## Collaboration Rules

Read collaboration rules when:

- the task may need a new thread, branch, worktree, or operation log;
- the task involves automation, sync, crawling, RSS, GitHub Actions, or external ingestion;
- the user asks for long-running work;
- the agent must decide whether to plan first or implement.

## Knowledge Operations Rules

Read knowledge operations rules when:

- changing directory structure;
- changing wiki page templates;
- moving content between raw, wiki, outputs, attachments, and system areas;
- defining MOC, INDEX, person, concept, or source fields;
- preparing output artifacts from wiki knowledge.

## Extraction Rules

Read extraction rules when:

- deciding whether raw content should enter the wiki;
- applying ICPT;
- choosing between keep raw, update concept, create concept, update MOC, update person, or route to outputs;
- checking extraction closure across page, network, link, status, and lint layers.

## External Agent Task Rules

Read external-agent rules when:

- another AI tool, script, or agent will perform extraction;
- the task needs clear input/output contracts;
- file permissions and safety boundaries must be explicit;
- the user wants a task brief that another agent can execute.

## Sample Calibration

Read sample or pilot records when:

- classification is ambiguous;
- the agent needs examples of past extraction decisions;
- the user wants a small sample before bulk processing.

## Error Log

Read the error log when:

- a similar mistake may have happened before;
- a new mistake needs to be recorded;
- the agent is about to repeat a failed route.

## Lint Rules

Read lint rules or scripts when checking:

- broken links;
- orphan pages;
- missing template sections;
- raw dumps;
- duplicate pages;
- likely misclassification;
- non-wiki assets inside wiki areas.

## Automation Rules

Read automation or tooling rules when:

- the user asks for sync, crawler, RSS, GitHub Actions, scheduled ingestion, monitoring, or external knowledge-base integration;
- source stability, account restrictions, cost, privacy, permissions, or maintenance risk could decide the route.
