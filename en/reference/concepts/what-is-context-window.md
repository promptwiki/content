---
title: "Context Window: How much AI can hold in its head at once"
purpose: reference
level: beginner
persona:
  - general
  - power-user
  - developer
status: stable
lang: en
translationKey: "what-is-context-window"
tags:
  - concept
  - context-window
  - token
created: "2026-02-18"
updated: "2026-02-18"
contributors:
  - Raunplaymore
---

The **context window** is the maximum amount of text an AI model can process in a single conversation — everything it can "see" at once.

Think of it as working memory. Whatever fits inside it, the AI knows about. Whatever falls outside, it doesn't.

## What's a token?

Context windows are measured in **tokens**, not words. Tokens are roughly word-sized chunks, but not exactly.

| Text | Approximate tokens |
|---|---|
| 1 English word | ~0.75 tokens |
| 1 Korean character | ~1–2 tokens |
| 1 page of English text | ~500 tokens |
| 1 page of Korean text | ~800–1,000 tokens |

**Reference sizes (early 2026, varies by model)**

| Model | Context Window |
|---|---|
| GPT-4o | 128,000 tokens (~96,000 words) |
| Claude 3.5 Sonnet | 200,000 tokens (~150,000 words) |
| Gemini 1.5 Pro | 1,000,000+ tokens |

## What's inside the context window?

```
┌─────────────────────────────────┐
│         Context Window          │
│                                 │
│  ┌──────────────────────────┐   │
│  │ System prompt            │   │
│  │ (AI's role / rules)      │   │
│  └──────────────────────────┘   │
│  ┌──────────────────────────┐   │
│  │ Conversation history     │   │
│  │ (your messages + AI's)   │   │
│  └──────────────────────────┘   │
│  ┌──────────────────────────┐   │
│  │ Your current message     │   │
│  └──────────────────────────┘   │
└─────────────────────────────────┘
```

The AI only "knows" what's inside the window. Anything beyond the limit is inaccessible — it's not that the AI forgot, it literally can't see it.

## What this means in practice

**Long conversations cause early instructions to get lost**
When the context window fills up, older content gets pushed out first. That's why instructions you gave at the start of a long conversation sometimes get ignored later.

Fix: Repeat important instructions mid-conversation if things start going off track.

**Huge documents have limits**
You can't paste a 500-page book into a single chat. Anything beyond the model's limit gets cut off or rejected.

Fix: Break large documents into sections and process each separately. Or summarize first, then work with the summary.

**New conversation = clean slate**
"Like I said before..." doesn't work across separate conversations. Starting a new chat means starting from zero.

Fix: Keep a text file with your frequently-used context (who you are, your project background, your preferences) and paste it at the start of new conversations.

## Common misconceptions

**"AI remembers me"**
Only within the current conversation — and only if the app doesn't clear history. Start a new chat, and the AI has never met you.

**"Bigger context window is always better"**
Larger windows let you process more at once, but very long contexts can cause the model to miss things buried in the middle. Keeping things focused is often more effective than dumping everything in.
