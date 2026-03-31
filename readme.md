# Slide Creation Workflow with NotebookLM + ChatGPT

## Goal
Create technical study group slides quickly by combining:
- NotebookLM for understanding papers and generating explanations
- ChatGPT for turning rough thoughts into a clean slide structure
- Manual edits for images, code, and final polish

## Workflow

### 1. Start with rough thinking
Open ChatGPT voice mode and talk through:
- the topic
- who the audience is
- what each section should roughly cover
- what facts still need research

Ask ChatGPT to turn that into a slide-by-slide outline.

### 2. Compress the outline
If the outline is too long, ask ChatGPT to shorten it by about 30–40%.

Goal:
- one clear text version of the deck before making slides

### 3. Use NotebookLM to learn faster
Upload the paper or source material into NotebookLM.

Use it to:
- understand the paper quickly
- generate explanations on subtopics
- check whether the flow of the deck makes sense

### 4. Generate the main deck
Use the system prompt below together with:
- the topic
- your source material
- the compressed outline

Let AI generate most of the deck structure and teaching flow.

### 5. Manually add the final 20%
Add these yourself:
- custom images
- diagrams AI misses
- GitHub repos
- code examples
- especially strong examples or discussion prompts

A good rule:
- AI creates the main deck
- you manually add the most important visual and practical pieces

### 6. Revise fast
Use ChatGPT to revise instead of rewriting manually:
- make this shorter
- make this clearer
- add more technical depth
- improve the analogy
- add one discussion question

### 7. Final quality check
Before presenting, make sure:
- the flow is easy to follow
- the session fits in time
- there is at least one practical repo or code reference
- there is one strong takeaway
- there is one prompt for discussion or self-research

## Practical Notes
- This workflow is especially good for paper reading groups and technical study groups
- NotebookLM is strong for understanding and explaining papers
- ChatGPT is strong for structure, shortening, and refinement
- Engineers usually want to see at least one codebase or implementation reference
- If AI cannot make the right visual, add it manually

## System Prompt
And to the bottom of this prompt, please also paste it in your topic of the session.

```
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
```