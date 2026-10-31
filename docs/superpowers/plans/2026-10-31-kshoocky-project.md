# KSHOOCKY Project Card Implementation Plan

> **For agentic workers:** REQUIRED SUB-SKILL: Use superpowers:subagent-driven-development (recommended) or superpowers:executing-plans to implement this plan task-by-task. Steps use checkbox (`- [ ]`) syntax for tracking.

**Goal:** Add a KSHOOCKY e-commerce project card to the portfolio projects grid.

**Architecture:** Extend the existing static HTML project grid with one card that matches the current card layout. Reuse the provided screenshot and Fullstack label; do not add details or a project link.

**Tech Stack:** HTML, existing Tailwind CSS utility classes.

**Spec:** `docs/superpowers/specs/2026-10-31-kshoocky-project-design.md`

## Global Constraints

- Keep the existing static HTML, responsive grid, category filter behavior, and asset path conventions.
- Do not add a description, technology list, or project link.
- Do not modify other project cards.

## Review Focus

- The image path must match the existing `assets/Kshoocky.png` filename exactly; verify the image file exists.
- The displayed category and title must be `Fullstack` and `KSHOOCKY – E-Commerce Website`.
- The new card must use the existing responsive project-card presentation without changing other cards.
- The category filter buttons only visually change selection; do not imply or add filtering behavior.
- The supplied image must have descriptive alternative text.

---

### Task 1: Add the KSHOOCKY project card

**Files:**
- Modify: `index.html` in the `#projects` grid
- Use: `assets/Kshoocky.png`

**Interfaces:**
- Consumes: Existing project-card markup and Tailwind classes.
- Produces: One additional card labeled `Fullstack`, with the title `KSHOOCKY – E-Commerce Website` and descriptive image alt text.

- [x] **Step 1: Write a failing content check**

Create a temporary check in the task workspace that parses `index.html` and asserts the `#projects` section contains an image using `assets/Kshoocky.png`, descriptive alt text, the `Fullstack` category, and the exact title `KSHOOCKY – E-Commerce Website`. Also assert that the referenced asset exists.

- [x] **Step 2: Run the check and verify it fails**

Run the check before editing `index.html`; it must fail because the KSHOOCKY card is not present.

- [x] **Step 3: Add the card**

Add a card after the existing project cards, following their image-frame, browser-chrome, overlay category, category caption, and title pattern. Use `assets/Kshoocky.png` and do not add a description, technology list, or link.

- [x] **Step 4: Run the check and verify it passes**

Run the same check and confirm the exact asset path, category, title, alt text, and local file are valid.

- [x] **Step 5: Verify presentation**

Open the portfolio page and confirm the new card appears in the grid, its image loads, and the existing card layout and filter-button visual behavior remain unchanged.
