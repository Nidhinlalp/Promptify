<p align="center">
  <img src="https://img.shields.io/badge/Gemini-Gem-4285F4?style=for-the-badge&logo=google&logoColor=white" alt="Gemini Gem" />
  <img src="https://img.shields.io/badge/Prompt_Engineering-Elite-FF6F00?style=for-the-badge" alt="Prompt Engineering" />
</p>

<h1 align="center">⚡ Promptify</h1>

<p align="center">
  <strong>One-click prompt beautifier — paste messy, get professional.</strong><br/>
  A Gemini Gem that transforms unstructured prompts into elite, copy-ready AI instructions.
</p>


---

## What It Does

Promptify takes any rough, half-finished, or unstructured prompt and transforms it into a **single, polished, professional AI instruction** — complete with an expert persona, structured problem statement, actionable steps, and targeted constraints.

**You paste this:**
> fix the login bug in my react app it keeps crashing

**You get back:**
> You are a Senior React Engineer with 8+ years building production web applications. You specialize in authentication flows, component lifecycle debugging, and diagnosing runtime crashes in complex single-page applications...
>
> **Current Behavior:** The login flow crashes during...
>
> **The Issue:** ...
>
> **Expected Result:** ...
>
> 1. Analyze the authentication component...
> 2. Identify the root cause...
>
> — Do not introduce new dependencies...

No commentary. No filler. Just the prompt — ready to paste.

---

## Features

- **Zero-friction transformation** — paste in, copy out. One message, one result.
- **Automatic persona assignment** — Promptify selects the most domain-specific expert identity for every task.
- **7-component prompt architecture** — every output follows the professional structure: Persona → Context → Problem Statement → Steps → Constraints → Format → Examples.
- **RAG-powered intelligence** — backed by a 700+ line Knowledge Base distilled from Anthropic's prompt engineering research and production AI design patterns.
- **No meta-commentary** — the output IS the prompt. No "Here is your improved prompt" wrappers.
- **Domain-agnostic** — works for code, copy, data analysis, DevOps, design, security, and more.

---

## The 7 Components of an Elite Prompt

Every prompt Promptify generates can include up to seven components, chosen deliberately based on the task:

| # | Component | Purpose |
|---|---|---|
| 1 | **Persona** | Activates domain-specific knowledge and sets response depth |
| 2 | **Context** | Grounds the model in the exact technical or domain environment |
| 3 | **Problem Statement** | Structures the ask into Current State → Issue → Expected Result |
| 4 | **Task Instructions** | Ordered, imperative steps from diagnosis to implementation |
| 5 | **Constraints** | Surgical anti-patterns specific to the task's likely failure modes |
| 6 | **Output Format** | Explicit structure, length, and formatting requirements |
| 7 | **Examples** | Few-shot patterns that teach format and quality simultaneously |

---

## Setup Guide — Build It Yourself

### Prerequisites

- A Google account with access to [Gemini](https://gemini.google.com)
- Access to [Gem Manager](https://gemini.google.com/gems/view)

### Step 1: Create the Gem

1. Go to [Gemini Gem Manager](https://gemini.google.com/gems/view)
2. Click **"New Gem"**
3. Fill in the fields exactly as specified below.

---

### Step 2: Set the Name

Paste this into the **Name** field:

```
Promptify
```

---

### Step 3: Set the Description

Paste this into the **Description** field:

```
Promptify is your one-click prompt beautifier. Paste in any messy, unstructured, or half-baked prompt and get back a single, clean, copy-ready instruction — with an expert persona, clear problem statement, and actionable steps. No fluff, no meta-commentary. Just the prompt, ready to go.
```

---

### Step 4: Set the Instructions

Paste the following **exactly** into the **Instructions** field. This is the Gem's system prompt — it defines Promptify's identity, transformation rules, and output format.

<details>
<summary><b>Click to expand full Instructions</b></summary>

```
You are Promptify, an elite Prompt Architect. Your sole purpose is to transform a user's messy, unstructured, or incomplete prompt into a single, polished, professional AI instruction that is ready for immediate use.



## Core Rules — Read These First



- **Output ONLY the pretty prompt.** Never add commentary like "Here is your enhanced prompt" or "I have transformed your request." The entire response IS the prompt.

- **No wrapper titles.** Do not add headers like "✨ PromptForge Output" or "The Pretty Prompt". Start directly with the persona line.

- **No emojis.** Use plain bold Markdown labels (e.g., **Current Behavior:**) for section markers.

- **One cohesive block.** The output should read as a single, unified prompt — not a formatted report with cards and sections. Use paragraphs and inline bold labels, not rigid section boxes.

- **Act, don't ask.** Never ask follow-up questions. Infer context, fill gaps, and make smart choices. The user came to you for a one-click result.

- **Preserve intent.** Enhance the delivery, never change the destination.



---



## How to Build the Pretty Prompt



Process every input through these stages, then collapse the output into one clean prompt block:



### 1. Persona Line (First sentence)

Open with an expert persona tailored to the task.

Format: `You are a [Title] specializing in [Specific Domain]. You have deep experience in [Relevant Skill Area].`



Do NOT add a label like "Persona:" before it. It is simply the first sentence.



### 2. Context (Inline, no label needed)

Weave the technical or domain context naturally into the setup. For code tasks, mention the file, framework, and component. For non-technical tasks, mention the industry, audience, and medium.



### 3. Problem Statement (Bold inline labels)

State the problem clearly using these inline bold labels on their own lines:



**Current Behavior:** What is happening now.



**The Issue:** The specific gap, bug, or conflict.



**Expected Result:** What correct behavior looks like.



For feature requests, use: **Current State:**, **Objective:**, **Success Criteria:**



### 4. Investigation / Implementation Steps (Numbered list)

Provide a numbered list of specific, actionable steps. Be concrete and reference the actual tech stack, function names, or patterns inferred from the input.



### 5. Constraints (Inline dashes, end of prompt)

Close with a compact dash-separated list of constraints or guidelines. No section header — just the list as a final paragraph.



---



## Output Format



- Pure Markdown only

- No triple-dashes or horizontal rules

- No titles or meta-headers

- Bold labels for problem sections

- Numbered list for steps

- Dash list for constraints

- The full output must be copyable as a single, self-contained prompt
```

</details>

---

### Step 5: Upload the Knowledge Base

This is the critical step that elevates Promptify from a simple reformatter to an **intelligent prompt architect**.

1. Download the [`Knowledge.md`](./Knowledge.md) file from this repository.
2. In the Gem configuration, find the **"Knowledge"** section.
3. Click **"Upload"** and select the `Knowledge.md` file.

#### What the Knowledge Base Does

The `Knowledge.md` file is Promptify's **source of truth** — a 700+ line professional field guide that acts as the RAG (Retrieval-Augmented Generation) layer. When the Gem processes a user's prompt, it references this knowledge to:

| Capability | How It Uses the Knowledge Base |
|---|---|
| **Persona selection** | Draws from 10+ domain-specific persona templates (Flutter, React, DevOps, Security, Copywriting, etc.) |
| **Context engineering** | Follows Anthropic's format patterns for structured context blocks |
| **Problem structuring** | Applies the 3-part problem statement formula (Current Behavior → Issue → Expected Result) |
| **Task instruction writing** | Uses imperative verb patterns and conditional logic from the field guide |
| **Constraint generation** | References task-specific anti-pattern libraries for code, output, and tone |
| **Quality grading** | Internally scores prompts against a 7-dimension rubric (Persona, Context, Clarity, Instructions, Format, Constraints, Hallucination Guards) |
| **Advanced techniques** | Applies Chain-of-Thought, Negative Space, Confidence Calibration, and Self-Review patterns when appropriate |

Without the Knowledge Base, the Gem uses only its Instructions. With it, the Gem has access to **professional-grade prompt engineering patterns** distilled from Anthropic research, Claude Opus specialists, and production AI system design.

---

### Step 6: Save and Test

1. Click **"Save"**
2. Open the Gem and paste in any rough prompt
3. Verify the output follows the structure: **Persona → Context → Problem → Steps → Constraints**

---

## How It Works

```
┌─────────────────────────────────────────────────────────┐
│                    User's Raw Input                     │
│  "fix the bug in my flutter app where the map crashes"  │
└──────────────────────────┬──────────────────────────────┘
                           │
                           ▼
┌─────────────────────────────────────────────────────────┐
│                   Promptify Engine                       │
│                                                         │
│  1. Extract core task                                   │
│  2. Identify domain (Flutter/Dart)                      │
│  3. Assign specific persona (Senior Flutter Engineer)   │
│  4. Build context block (framework, architecture, file) │
│  5. Structure 3-part problem statement                  │
│  6. Write ordered task instructions                     │
│  7. Add targeted constraints                            │
│  8. Collapse into single unified prompt block           │
│                                                         │
│  ┌───────────────────────────────────────────────────┐  │
│  │        Knowledge.md (RAG Layer)                   │  │
│  │  • Persona templates  • Constraint libraries      │  │
│  │  • Format patterns    • Quality rubrics            │  │
│  │  • Advanced techniques (CoT, Negative Space...)   │  │
│  └───────────────────────────────────────────────────┘  │
└──────────────────────────┬──────────────────────────────┘
                           │
                           ▼
┌─────────────────────────────────────────────────────────┐
│                 Elite Prompt Output                      │
│                                                         │
│  You are a Senior Flutter/Dart Engineer with 8+ years   │
│  of experience building production-grade mobile apps... │
│                                                         │
│  **Current Behavior:** The map widget crashes when...   │
│  **The Issue:** ...                                     │
│  **Expected Result:** ...                               │
│                                                         │
│  1. Analyze the MapController lifecycle...              │
│  2. Identify disposal timing conflicts...               │
│                                                         │
│  — Do not refactor the entire navigation stack...       │
└─────────────────────────────────────────────────────────┘
```

---

## Repository Structure

```
promptify/
├── README.md            # This file — setup guide and documentation
├── Description.md       # Gem description (paste into Description field)
├── Instructions.md      # Gem system prompt (paste into Instructions field)
└── Knowledge.md         # RAG knowledge base (upload to Knowledge section)
```

---

## Quick Reference — What Goes Where

| Gem Field | Source File | Action |
|---|---|---|
| **Name** | — | Type `Promptify` |
| **Description** | `Description.md` | Copy & paste contents |
| **Instructions** | `Instructions.md` | Copy & paste contents |
| **Knowledge** | `Knowledge.md` | Upload the file directly |

---

## The Transformation Rules

When Promptify receives a messy prompt, it applies these rules in order:

1. **Extract the core task** — isolate a single sentence describing the user's goal
2. **Identify the domain** — Flutter, React, Python, copywriting, data analysis, DevOps, etc.
3. **Assign the most specific persona** — never generic when specific fits
4. **Build the context block** — language, framework, file, architecture (or industry, audience, medium)
5. **Structure the problem in three parts** — Current Behavior / Issue / Expected Result (or Current State / Objective / Success Criteria)
6. **Write ordered task instructions** — numbered imperatives, one action per line
7. **Add targeted constraints** — only the most likely failure modes, never more than 5–6
8. **Output as a single, unified block** — no wrapper, no commentary, no explanation

---

## Contributing

Contributions are welcome. If you have improvements to the Knowledge Base, transformation rules, or documentation:

1. Fork this repository
2. Create a feature branch (`git checkout -b improve-knowledge-base`)
3. Commit your changes (`git commit -m 'Add persona templates for ML engineers'`)
4. Push to the branch (`git push origin improve-knowledge-base`)
5. Open a Pull Request

---