# GitHub Profile Refresh Implementation Plan

> **For agentic workers:** REQUIRED SUB-SKILL: Use superpowers:subagent-driven-development (recommended) or superpowers:executing-plans to implement this plan task-by-task. Steps use checkbox (`- [ ]`) syntax for tracking.

**Goal:** Publish an English-only GitHub profile README that positions Jarry as a current agent systems engineer and improves visible activity through real, low-cost maintenance work.

**Architecture:** The profile repository contains one README as the public presentation layer and a small local validation script for links and required copy. Existing personal repositories receive only focused documentation or example updates that can be explained in their histories. Upstream forks, if created, are limited to three and are explicitly attributed.

**Tech Stack:** Markdown, GitHub-flavored Markdown, GitHub API/CLI, Python standard library for validation.

---

### Task 1: Create the profile README

**Files:**
- Create: `README.md`
- Modify: `docs/superpowers/specs/2026-10-01-github-profile-design.md` only if implementation constraints change

- [ ] **Step 1: Write the README sections**

Add an English-only README with: concise headline; current agent focus; SJTU education; ByteDance agent role; one short WeRide historical line; focus areas for orchestration, retrieval, memory, tools, evaluation, and observability; selected links to personal projects; a compact skills list; stats and contribution widgets with stable fallback links; interests and the motto “When things are ambiguous, take one deliberate step forward.”

- [ ] **Step 2: Validate required claims and links**

Run a local script or Python checks that confirm the README includes the exact profile repository owner, links to `my-co-researcher` and `hybrid-rag-mcp-server`, English-only section text, visible upstream attribution for any fork links, and no placeholder contact URLs.

- [ ] **Step 3: Commit the profile README**

```bash
git add README.md
git commit -m "feat: publish agent engineer profile README"
git push
```

### Task 2: Curate public project visibility

**Files:**
- Modify: GitHub repository metadata for `my-co-researcher` and `hybrid-rag-mcp-server`
- Optional: Create at most three GitHub forks selected from OpenAI Agents Python, Microsoft AutoGen, and CrewAI

- [ ] **Step 1: Update descriptions and topics**

Use GitHub CLI to add accurate descriptions and agent-related topics to the two personal repositories. Do not claim capabilities that are absent from their code.

- [ ] **Step 2: Verify upstream repositories before any fork**

Check that each candidate exists, is active, and allows forks. Create no more than three forks, and keep upstream attribution visible in the fork metadata and README.

- [ ] **Step 3: Record project curation**

Commit a small `docs/project-curation.md` in the profile repository listing personal work versus upstream forks and why each is relevant. Push the change.

### Task 3: Add real low-cost activity

**Files:**
- Modify: focused README, examples, tests, or configuration files in existing local repositories only where the change improves usability or correctness

- [ ] **Step 1: Inspect each target repository’s contribution guidelines**

Read repository-local `AGENTS.md`, README, and contribution instructions before editing.

- [ ] **Step 2: Make one or two substantive maintenance changes per suitable repository**

Prefer documentation corrections, runnable examples, smoke tests, evaluation fixtures, or configuration explanations. Keep each commit narrowly scoped and explainable.

- [ ] **Step 3: Run the repository’s smallest relevant checks**

Run existing markdown checks, unit tests, or syntax checks appropriate to each change. Avoid adding tests that only mirror unchanged documentation.

- [ ] **Step 4: Commit and push each repository separately**

Use descriptive commit messages and preserve the current author identity. Do not backdate commits or create empty commits.

### Task 4: Verify the public profile

**Files:**
- Create: `scripts/validate_profile.py` if a reusable local validator is useful

- [ ] **Step 1: Validate README content**

Check English-only copy, current-agent emphasis, concise WeRide history, motto, interests, required links, and fallback URLs.

- [ ] **Step 2: Validate remote state**

Confirm the profile repository is public, named `jiarongli517021911144/jiarongli517021911144`, and the pushed commit is visible through the GitHub API.

- [ ] **Step 3: Inspect rendered output**

Open the public README URL and check desktop, mobile-width, light-theme, and dark-theme readability. Confirm broken image services leave meaningful alt text or fallback links.

- [ ] **Step 4: Report contribution scope accurately**

Report only commits and repositories that were actually changed. State that activity begins from the current date and that prior inactive dates were not fabricated.
