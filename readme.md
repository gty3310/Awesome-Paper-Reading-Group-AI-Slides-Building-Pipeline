# Slide Creation Workflow with Deep Research + ChatGPT + Gamma + NotebookLM

## Goal
Create strong study group or class slides quickly by combining:
- **ChatGPT / Claude Deep Research** for topic research
- **ChatGPT voice mode** for thinking through structure
- **Gamma.app** for fast text-based decks
- **NotebookLM** for understanding papers and generating explanation-heavy decks
- **Manual edits** for images, code, repos, diagrams, and final polish

---

## Core Decision Rule

### If the topic is simple and mostly text-based
Use:
- Deep research
- ChatGPT for outline
- **Gamma.app** for fast slide generation

### If the topic is complex and needs strong explanation
Use:
- Deep research
- ChatGPT for outline
- **NotebookLM** for learning, explanation, and source-grounded deck generation
- Manual additions for visuals, code, and practical examples

---

## Workflow

```mermaid
flowchart TD
    A[Pick topic] --> B[Do deep research in ChatGPT / Claude]
    B --> C[Learn the topic + talk through outline in ChatGPT voice mode]
    C --> D[Compress outline]
    D --> E{Topic does not require illustration, or slides has clickable urls or images you want to insert}
    E -- No --> G[Upload support reading materials to notebooklm.google]
    E -- Yes --> F[Generate deck in Gamma.app]
    G --> H[Generate explanations and deck structure]
    F --> I[Manual polish]
    H --> I[Manual polish]
    I --> J[Final quality check]
```

---

## Full Workflow

### 1. Start with deep research on the topic
Use:
- **ChatGPT Deep Research**
- **Claude Deep Research**

Goal:
- understand the topic
- collect the most important ideas
- identify strong supporting sources
- figure out what still needs clarification

---

### 2. Learn and think through it with ChatGPT voice mode
Open ChatGPT voice mode and talk through:
- the topic
- who the audience is
- what each section should roughly cover
- what is confusing
- what facts still need more research

Ask ChatGPT to turn that into:
- a **slide-by-slide outline**
- a rough teaching flow
- a suggested session structure

---

### 3. Compress the outline
If the outline is too long, ask ChatGPT to shorten it by about **30–40%**.

Goal:
- get to **one clean text version** of the whole deck before generating slides
- reduce repetition
- keep only the strongest teaching flow

---

### 4. Choose the slide generation path

#### Path A — Fast path for simpler topics
Use this when:
- the topic is easy to explain
- the slides are mostly text-based
- visuals are not the main challenge

Workflow:
- take the compressed outline
- take the research notes
- put them into **Gamma.app**
- generate the first full deck quickly

#### Path B — Structured path for harder topics
Use this when:
- the concept is hard to explain
- diagrams or infographics are needed
- source grounding matters more
- the session is paper-heavy or technically dense

Workflow:
- identify the **top subtopics**
- identify the **top sources / papers**
- upload the papers or source material into **NotebookLM**
- use NotebookLM to understand and explain the material
- use NotebookLM plus your compressed outline to help generate the main deck structure

---

## NotebookLM Use Case

### 5. Use NotebookLM to learn faster
Upload the paper or source material into NotebookLM.

Use it to:
- understand the paper quickly
- generate explanations for subtopics
- test whether the teaching flow makes sense
- compare how different concepts connect
- identify what needs simpler explanation for the audience

This is especially useful for:
- paper reading groups
- technical study groups
- research-heavy sessions
- topics that need layered explanation

---

### 6. Generate the main deck
Use AI to generate most of the deck structure and teaching flow using:
- the topic
- the source material
- the compressed outline
- the system prompt below

Goal:
- let AI produce the **main 80%**
- keep your effort for the highest-value 20%

---

### 7. Manually add the final 20%
Add these yourself:
- custom images
- diagrams AI misses
- GitHub repos
- code examples
- strong real-world examples
- discussion prompts
- visual explanations for abstract ideas

A good rule:
- **AI creates the main deck**
- **you add the most important visual and practical pieces**

Engineers usually want at least:
- one codebase
- one implementation reference
- one concrete practical takeaway

---

### 8. Revise fast with ChatGPT
Use ChatGPT to revise instead of rewriting manually.

Example requests:
- make this shorter
- make this clearer
- add more technical depth
- improve the analogy
- add one discussion question
- make this more beginner-friendly
- make this more rigorous for researchers

---

### 9. Final quality check
Before presenting, make sure:
- the flow is easy to follow
- the session fits in time
- there is at least one practical repo or code reference
- there is one strong takeaway
- there is one prompt for discussion or self-research
- the visuals support the hardest ideas clearly

---

## Practical Notes

### What each tool is best at

#### Deep Research
Best for:
- finding the landscape
- gathering sources
- comparing viewpoints
- identifying what matters

#### ChatGPT
Best for:
- turning rough thoughts into structure
- compressing and refining outlines
- adjusting depth for different audiences
- revising language quickly

#### Gamma.app
Best for:
- fast generation of simple decks
- text-based slide creation
- quick first drafts

#### NotebookLM
Best for:
- understanding papers
- generating explanations from source material
- validating flow against real documents
- building decks for technical and research-heavy sessions

#### Manual editing
Best for:
- diagrams
- code
- repos
- standout visuals
- final teaching polish

---

## Best-Fit Use Cases

### This workflow is especially strong for:
- paper reading groups
- technical study groups
- AI architecture talks
- ML concept explainers
- sessions that mix beginners, builders, and researchers

---

## Summary Logic

### Simple topic
**Deep Research → ChatGPT outline → Gamma.app → manual polish**

### Complex topic
**Deep Research → ChatGPT voice mode + outline → compress outline → NotebookLM with sources → AI-generated main deck → manual final 20%**

---

## System Prompt

Paste your topic at the bottom of this prompt before using it.

```text
Role: You are a top-tier Technical Strategist and Researcher.


Topic:


Context
We are a study group of entrepreneurial engineers, ML founders, and PhD researchers. Our goal is to move beyond hype, understand the core technical walls of AGI, and identify real product opportunities.


Deck Structure (30–10–20 Format)


Part A — Strategic Overview (Slides 1–6)

Vision — the paradigm shift

Cognitive Architecture — the core loop

Industrial Schools — competing worldviews

Technical Taxonomy — how the system organizes space/time

Math / Objective — the optimization framework

Debate Slide — prompt a 20-minute discussion on which school will win


Part B — Break (Slide 7)
7. 10-Minute Break — include a research task students can do with their own tools


Part C — Deep Dive & Applied Future (Slides 8–13)
8. Current Research — state of the art
9. Gaps — what is still broken
10. Future Trends — next 12–24 months
11. Technical Deep Dive — one major bottleneck
12. Product Ideas — 3–5 practical, high-value project ideas
13. Summary — roadmap from this topic toward AGI


For Every Slide, include 3 boxes:

Builder Box — implementation, tooling, and industry backbones

Beginner Blog — one simple analogy-based paragraph

Researcher Sidebar — math, formalisms, and historical roots


Formatting Rules

Start every bullet with Bolded Two Words

Follow with a 2–5 word summary

Keep each point to 1–2 lines

Write for a mixed audience: builders, newcomers, and researchers