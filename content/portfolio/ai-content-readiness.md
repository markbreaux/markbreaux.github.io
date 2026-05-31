---
title: "AI Content Readiness"
date: 2026-05-01
description: "How I positioned NI's documentation organization ahead of the AI curve — through automated content enrichment, schema.org structured data injection, normalized content exports, and a custom AI prompt library."
draft: false
tags: ["AI/LLM", "Content Architecture", "DITA", "Schema.org", "Automation"]
---

Before AI-driven content consumption became a mainstream organizational concern, I was already designing for it — building infrastructure to ensure NI's documentation would perform well in LLM interfaces, AI-powered search, and internal AI platforms. This case study covers four interconnected initiatives that collectively established the organization's AI content readiness foundation.

---

## The Challenge

As AI-driven interfaces — chatbots, LLMs, AI-assisted search — became a real documentation delivery channel, a critical question emerged: *was the content structured in a way that would actually perform well in those contexts?*

The honest answer was no. Short descriptions, the content most likely to surface as featured snippets in AI-generated responses, were missing or inconsistent across thousands of topics. HTML output lacked machine-readable signals that help search engines and AI systems understand content context. There was no normalized export of documentation for AI teams who needed to ingest it. And the writer community had no shared tooling to work effectively alongside AI.

---

## The Approach

I addressed this through four parallel efforts:

**Automated short-description enrichment.** Short descriptions are the highest-value content in an AI interface — they're what appears in summaries, search snippets, and chatbot responses. I built a custom Positron action to automate DITA short-description population at scale, then coordinated a team-wide effort to apply it across documentation aligned to a major software roadmap.

**Schema.org structured data injection.** I developed a DITA Open Toolkit plugin that injects schema.org structured data tags into HTML5 output. This signals content type, context, and relationships to both search engines and AI systems — improving how documentation is understood and surfaced at ingestion time.

**Normalized content exports for AI consumption.** I designed DITA and Markdown content repositories as automated CCMS exports, enabling AI teams within the organization to directly ingest documentation into internal AI platforms. The architecture eliminated manual handoff and made the documentation library a first-class content source for downstream AI initiatives.

**AI prompt library.** Working with the writer community, I built a shared AI prompt library — a curated set of prompts designed for documentation use cases and tested against real authoring scenarios. This gave 30–50 technical writers a scalable, practical foundation for AI-assisted authoring from day one.

---

## The Outcome

- Improved featured-snippet performance in AI-driven chat interfaces and internal AI tools.
- Established a reusable, scalable infrastructure for documentation to be consumed by LLMs and AI platforms.
- Enabled on-demand ingestion of the full documentation library by internal AI teams.
- Gave the writer community practical, tested AI tooling to work with immediately.
- Positioned the documentation organization as a forward-thinking partner to product and technology teams exploring AI-driven delivery.

---

## Why It Matters

AI content readiness isn't a single project — it's an architectural posture. This work demonstrates how I approach emerging technology: not by reacting to requirements as they arrive, but by identifying what the content infrastructure needs to look like *before* the business asks for it.
