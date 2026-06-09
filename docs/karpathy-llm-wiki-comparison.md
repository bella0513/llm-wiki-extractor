# Karpathy LLM Wiki Comparison

This project is inspired by Andrej Karpathy's [LLM Wiki pattern](https://gist.github.com/karpathy/442a6bf555914893e9891c11519de94f).

The original insight is that a useful AI-readable knowledge base should not rely only on repeated retrieval from raw materials. Raw materials can be compiled into a persistent wiki that agents can read and maintain over time.

This project focuses on what happens before writing: extraction decisions.

## The Missing Operations Layer

A persistent wiki compounds only if the agent writes the right things into it.

Without extraction rules, an AI-maintained wiki often becomes noisy:

- every raw input becomes a page;
- summaries replace reusable knowledge;
- meeting notes are copied into concept pages;
- duplicate pages appear;
- links point nowhere;
- the wiki becomes larger but not more useful.

`llm-wiki-extractor` adds a decision layer for preventing those failures.

## Comparison

| Dimension | Karpathy-style LLM Wiki | llm-wiki-extractor |
| --- | --- | --- |
| Main contribution | Persistent AI-readable wiki pattern | Knowledge extraction decision framework |
| Core flow | raw -> wiki -> schema | raw -> task -> ICPT -> wiki action -> lint |
| Main risk | Repeated retrieval from raw every time | AI-generated wiki clutter |
| Primary object | Wiki pages and schema | Reusable knowledge objects |
| Writing strategy | Compile raw materials into wiki | Decide whether, where, and how to write |
| Best fit | Building the knowledge base idea | Operating and maintaining it safely |

## Positioning Statement

Not another wiki template. A decision framework for extracting reusable knowledge from raw materials.

## Credit

Credit goes to Andrej Karpathy for the [LLM Wiki pattern](https://gist.github.com/karpathy/442a6bf555914893e9891c11519de94f). This project is an operations-layer extension focused on extraction, classification, and anti-clutter rules for agent-maintained Markdown wikis.
