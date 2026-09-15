# Organization Profile Manifesto Implementation Plan

> **For Claude:** REQUIRED SUB-SKILL: Use superpowers:executing-plans to implement this plan task-by-task.

**Goal:** Rewrite the E-Dialect organization profile as a concise, factual open-engineering manifesto with clear initiative, product, participation, and governance boundaries.

**Architecture:** Keep the GitHub-supported `profile/README.md` entry point. Organize it as community manifesto, current initiative, reusable ecosystem flow, experimental capabilities, participation paths, and trust/governance links; use only verified repository and documentation URLs.

**Tech Stack:** GitHub-flavored Markdown, Git, GitHub organization profile rendering.

---

### Task 1: Establish the factual baseline

**Files:**
- Read: `profile/README.md`
- Read: `GOVERNANCE.md`
- Read: `LICENSING.md`
- Read: `ASSET_AND_DATA_POLICY.md`

**Step 1:** Confirm E-Dialect is the community and 乡声万语 is the current initiative.

**Step 2:** Confirm the live repositories and Project #7 URL through GitHub.

**Step 3:** Exclude the proposed `.profile` repository, MIT badge, empty URLs, unverified metrics, and a fictional mature 万语引擎.

### Task 2: Rewrite the organization profile

**Files:**
- Modify: `profile/README.md`

**Step 1:** Add a centered `E-Dialect | 地方语言数字化基础设施` hero and the slogan `一乡一声，万乡万语。让下一种地方语言，不必再从零开始。`

**Step 2:** Explain the repeated one-off digitization problem and the platform/local-community division of responsibility.

**Step 3:** Present 乡声万语 as the current flagship initiative, not the whole organization.

**Step 4:** Present 万语校坊, 乡声集盒, and 兴化语记 as a reusable workflow and list current experimental intelligence repositories without claiming product maturity.

**Step 5:** Add distinct calls to action for developers, researchers, and local contributors, with valid links to the website, Project #7, contributing guide, and governance.

**Step 6:** Retain concise community/company, licensing, CLA, and data-asset boundaries.

### Task 3: Verify and publish through a pull request

**Files:**
- Verify: `profile/README.md`

**Step 1:** Run `git diff --check` and expect no output.

**Step 2:** Scan for `.profile`, `License-MIT`, empty Markdown links, `AGPL-3.0-or-later`, exaggerated claims, and incorrect replacement terminology; expect no unsafe matches.

**Step 3:** Confirm all local relative links resolve and all referenced GitHub repositories remain public and unarchived where represented as active.

**Step 4:** Review `git diff` for factual parity with governance and licensing documents.

**Step 5:** Commit with `docs(profile): present community infrastructure vision`, push the independent branch, and open a focused pull request without mixing CLA PR #7.
