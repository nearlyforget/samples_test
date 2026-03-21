# UCP Sample Applications (samples_test) Style Guide

<!--*
freshness: { owner: 'chadliu' reviewed: '2026-03-21' }
*-->

This guide defines the standards for the UCP sample implementations (A2A, REST, etc.), focusing on clarity, educational value, and brand neutrality.

## Core Principles

### 1. Brand Neutrality (MANDATORY)
Samples are the first thing developers see. They MUST be strictly brand-neutral.
*   **DO NOT** use brand names (e.g., Target, Shopify) in product names, shop names, or URLs.
*   **DO** use generic terms: `Flower Shop`, `Gadget Store`, `The Merchant`.
*   **Placeholder Data:** Use `example.com` for all domains.

### 2. Educational Value
*   **Comments:** Use comments to explain **why** a certain UCP step is taken, not just what the code does. Refer to specific UCP specification sections where applicable.
*   **Simplicity:** Favor readable, straightforward code over complex optimizations. The goal is for a developer to be able to copy-paste and adapt the logic.

### 3. Consistency Across Tech Stacks
*   **Cross-Language:** Ensure the Python, Node.js, and TypeScript samples implement the same logic and commerce flows so developers can compare implementations easily.

## Technical Standards

### Multi-Language Style
*   **Python:** Follow **2-space indentation** (as per `pyproject.toml` in `business_agent`). Use Pydantic for models.
*   **JavaScript/TypeScript:** Follow **2-space indentation** (as per `.prettierrc`). Use clean, modern React/Vite patterns for frontend samples.
*   **Markdown:** Use clear, step-by-step instructions in all `README.md` and `DEVELOPER_GUIDE.md` files.

### Repository Specifics
*   **A2A (Agent-to-Agent):** Ensure ADK (Agent Development Kit) patterns are followed correctly.
*   **REST:** Ensure standard UCP REST API headers and error structures are used.

## Semantic Review Focus
Gemini should prioritize:
1.  **Brand Leaks:** Rigorously check for any accidental brand mentions in UI text or sample data.
2.  **Clarity:** Is the code easy for a newcomer to understand? Are the comments helpful?
3.  **Spec Alignment:** Do the sample payloads match the current UCP specification?
