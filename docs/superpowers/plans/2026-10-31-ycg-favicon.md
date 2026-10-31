# YCG Favicon Implementation Plan

> **For agentic workers:** REQUIRED SUB-SKILL: Use superpowers:subagent-driven-development (recommended) or superpowers:executing-plans to implement this plan task-by-task. Steps use checkbox (`- [ ]`) syntax for tracking.

**Goal:** Replace the browser's default globe favicon with a YCG brand icon.

**Architecture:** Add a standalone SVG favicon asset and reference it from the existing static HTML document head. Match the navbar's dark `YC` and orange `G` colors.

**Tech Stack:** HTML, SVG.

**Spec:** `docs/superpowers/specs/2026-10-31-ycg-favicon-design.md`

## Global Constraints

- Keep the existing static HTML site.
- Use the current brand treatment (dark `YC`, orange `G`).
- Do not change the navbar logo, page title, or other site visuals.

## Review Focus

- The favicon link must point to an existing `assets/favicon.svg`.
- SVG must display YCG initials with contrasting dark and orange brand colors.
- Do not alter unrelated page content.

---

### Task 1: Add and link the YCG favicon

**Files:**
- Create: `assets/favicon.svg`
- Modify: `index.html` in `<head>`

**Interfaces:**
- Consumes: Existing brand colors and static asset paths.
- Produces: A browser favicon link to `assets/favicon.svg` and a scalable YCG brand icon.

- [ ] **Step 1: Write a failing content check**

Create a temporary check that asserts `index.html` links to `assets/favicon.svg`, that the asset exists, and that the SVG includes the YCG initials and dark/orange brand colors.

- [ ] **Step 2: Run the check and verify it fails**

Run the check before editing the page; it should fail because no favicon is configured.

- [ ] **Step 3: Add the SVG and document link**

Create the SVG favicon and add its `<link rel="icon" type="image/svg+xml">` entry in `index.html`'s `<head>`.

- [ ] **Step 4: Run the check and verify it passes**

Run the same check and confirm the favicon reference and SVG content.

- [ ] **Step 5: Verify in the browser**

Reload the page and verify the favicon is served and the tab no longer uses the default globe icon.
