# Example: Automation Assessment

## User Prompt

```text
[$llm-wiki-extractor] I want to automatically sync web articles into my knowledge base. First assess goals, mature tools, risks, and maintenance cost. Do not write code yet.
```

## Assessment Flow

### 1. Clarify Goal

The agent should ask or infer which goal matters most:

- save full text;
- remind user to read;
- summarize;
- extract reusable knowledge;
- reduce manual filing;
- feed an AI Q&A system.

### 2. Compare Routes

Possible routes:

- browser clipper;
- RSS reader;
- read-it-later app;
- no-code automation;
- paid knowledge tool;
- custom script.

### 3. Check Risks

- Source website stability.
- Login and paywall issues.
- Account or anti-scraping risk.
- Privacy and copyright.
- Maintenance burden.
- Whether summaries will be mistaken for extracted knowledge.

### 4. Recommendation

For most personal knowledge bases, start with manual or semi-automatic clipping plus extraction review.

Do not auto-ingest every article into wiki. Keep clipped articles raw until the extractor finds reusable knowledge objects.

## Good Output

```text
Recommendation: do not build a crawler first. Start with a read-it-later or clipper workflow, then run extraction on selected articles. The main bottleneck is not capture; it is deciding what should become reusable knowledge.
```
