# llm-wiki-extractor

A knowledge extraction skill for Karpathy-style LLM Wikis.

Karpathy's [LLM Wiki pattern](https://gist.github.com/karpathy/442a6bf555914893e9891c11519de94f) shows how raw materials can be compiled into a persistent wiki. This project focuses on the hard part: extraction.

It helps AI agents decide what should become reusable knowledge, what should stay raw, and how to keep an LLM Wiki from becoming an AI-generated junk drawer.

中文一句话：这是一个面向 LLM Wiki 的知识萃取 skill，帮助 AI 判断 raw 中哪些内容值得进入 wiki、应该进入哪里，以及如何避免空壳页、重复页和 raw 全文搬运。

## Why This Exists

Many AI-assisted knowledge bases fail in the same way:

- one raw note becomes one empty wiki page;
- meeting notes get copied into concept pages;
- links point to pages that do not exist;
- the AI creates duplicate concepts instead of updating existing ones;
- the wiki grows, but reusable knowledge does not.

This skill adds an extraction decision layer before writing.

## Inspired By Karpathy's LLM Wiki

This project is inspired by Andrej Karpathy's [LLM Wiki pattern](https://gist.github.com/karpathy/442a6bf555914893e9891c11519de94f).

Karpathy showed why LLM Wikis compound: raw information can be compiled into a persistent, agent-readable knowledge base.

This project adds a practical governance layer:

| Topic | Karpathy-style LLM Wiki | llm-wiki-extractor |
| --- | --- | --- |
| Core question | How can raw materials become a persistent wiki? | What exactly should be extracted from raw materials? |
| Main focus | Persistent knowledge compilation | Reusable knowledge extraction |
| Risk addressed | Repeated retrieval from scratch | AI-generated wiki clutter |
| Writing policy | Let agents maintain the wiki | Decide before writing, then maintain the network |
| Best use | Building an LLM-readable wiki | Keeping that wiki clean and useful |

## Core Ideas

- **Extraction-first**: do not turn every raw input into a wiki page.
- **ICPT framework**: classify knowledge as Information, Concept, Principle, or Tool.
- **Tool knowledge priority**: prioritize standards, sensing/checklists, plans, and countermeasures.
- **Network-aware writing**: check existing concepts before creating new pages, then update MOC, INDEX, person pages, sources, and links.
- **Anti-junk rules**: prevent raw full-text dumps, empty concept pages, duplicate pages, broken links, and vague AI summaries.

## What This Is Not

- Not a complete wiki app.
- Not a RAG system.
- Not an Obsidian plugin.
- Not a bulk import tool.
- Not a replacement for your own knowledge base rules.

It is a decision framework and Codex-style skill for agents that work on Markdown knowledge bases.

## Repository Structure

```text
llm-wiki-extractor/
├── README.md
├── LICENSE
├── llm-wiki-extractor/
│   ├── SKILL.md
│   └── references/
│       └── rules-map.md
├── examples/
│   ├── raw-to-concept.md
│   ├── query-existing-pages.md
│   └── automation-assessment.md
└── docs/
    ├── karpathy-llm-wiki-comparison.md
    └── extraction-framework.md
```

## Quick Start

Copy the `llm-wiki-extractor/` skill folder into your Codex skills directory:

```text
C:\Users\YOUR_NAME\.codex\skills\llm-wiki-extractor
```

Then start a new conversation and call it explicitly:

```text
[$llm-wiki-extractor] Help me decide whether this raw note should be extracted into my wiki. Read only the necessary files and do not edit anything yet.
```

Before allowing edits, adapt the skill to your own knowledge base:

- raw directory;
- wiki directory;
- output directory;
- system/rules directory;
- page types;
- MOC/INDEX conventions;
- link format;
- lint process.

## Example Prompts

```text
[$llm-wiki-extractor] Extract reusable knowledge from this raw note. First decide whether it contains Information, Concept, Principle, or Tool knowledge. Do not write files until you explain the extraction decision.
```

```text
[$llm-wiki-extractor] Check whether my wiki already has a page for this topic. Read INDEX and MOC pages first. Avoid full-vault search unless needed.
```

```text
[$llm-wiki-extractor] I want to automatically sync web articles into my knowledge base. First assess goals, mature tools, risks, and maintenance cost. Do not write code yet.
```

## Commercial Use Case

This open-source skill is a lightweight demo of a broader service pattern: turning messy organizational materials into reusable knowledge assets.

It can support teams that have:

- meeting notes that never become useful standards;
- project retrospectives that are not reused;
- expert knowledge trapped in interviews or training materials;
- AI Q&A systems with poor knowledge sources;
- training teams that need reusable cases, SOPs, and evaluation materials.

The paid work is not the skill file. The paid work is applying this extraction method to real organizational materials and building a maintainable knowledge asset system.

## Suggested Topics

```text
llm-wiki
knowledge-extraction
ai-agent
codex
obsidian
markdown
knowledge-management
personal-knowledge-base
wiki
prompt-engineering
```

## License

MIT
