# Example: Query Existing Pages

## User Prompt

```text
[$llm-wiki-extractor] Check whether my wiki already has a page about customer segmentation. Read INDEX and MOC pages first. Do not scan the whole vault unless needed.
```

## Agent Behavior

1. Read the business or marketing INDEX page.
2. Read relevant MOC pages.
3. Search only if indexes do not answer the question.
4. Report candidate existing pages before suggesting a new page.

## Good Answer Shape

```text
I found two related pages:

- Customer Segmentation Method: likely the main concept page.
- Sales Qualification Criteria: related, but narrower.

Recommendation: update Customer Segmentation Method instead of creating a new page. The new material appears to add a scoring criterion, not a separate concept.
```

## What To Avoid

```text
I created a new page called Customer Segmentation.
```

This is wrong if an existing page already covers the topic.
