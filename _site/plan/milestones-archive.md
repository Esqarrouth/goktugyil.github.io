# Milestone 1: Build the Cockpit

**Goal:** From a brand-new Mac, reach the point where I can clone the website, run it locally, edit it with Codex, verify it in a browser, commit, push, and deploy.

**Status: Complete.** The reproducible setup was committed in `0a8100e`, and the branch/PR/edit/verify/merge workflow was subsequently exercised through the typo PR and focused Milestone 2 commits.

**Estimated time: 2-4 hours**

## 1. Machine Setup

- [x] Install Apple Command Line Tools
- [x] Install Homebrew
- [x] Install Git
- [x] Configure Git name + email (`Goku`, GitHub-linked email)
- [x] Install GitHub CLI (`gh`)
- [x] Authenticate GitHub as `Esqarrouth` over HTTPS
- [x] Install VS Code (optional for visual diff/file inspection; Codex can be primary)
- [x] Install Codex CLI
- [x] Sign into Codex using my ChatGPT account
- [x] Node.js decision: not required by this repo/setup right now; install later only if a tool requires it

## 2. Repository Setup

- [x] Clone `Esqarrouth/goktugyil.github.io` to `~/Documents/Code/goktugyil.github.io`
- [x] Decide editor workflow: Codex CLI/App primary; VS Code optional for visual diffs/manual inspection
- [x] Inspect:
  - [x] `README`
  - [x] `Gemfile` (confirmed absent)
  - [x] `_config.yml`
  - [x] theme configuration
  - [x] layouts/includes
  - [x] pages
  - [x] posts
  - [x] assets
  - [x] deployment configuration
- [x] Confirmed Jekyll + vendored Simon Freytag **Friday Theme**
- [x] Confirmed GitHub Pages legacy branch build
- [x] Confirmed production source is `master` branch, `/` path
- [x] Confirmed GitHub Pages serves `goktug.io` through `CNAME`

## 3. Local Jekyll Environment

Only do what the repo actually requires.

- [x] Install non-system Ruby via `chruby` + `ruby-install`
- [x] Ruby **3.4.1** active; Bundler **2.6.2** available
- [x] Run `bundle install`
- [x] Start the existing site locally
- [x] Open localhost in the browser
- [x] Confirm the local site matches production closely enough to use for development
- [x] Confirm the site builds cleanly with the locked dependencies (reverified August 10, 2026)

**Architecture decision:** If the existing Jekyll setup builds cleanly, **do not migrate frameworks in this project.**

## 4. Git Workflow

Learn the small set of commands/concepts actually required:

- [x] `git status`
- [x] `git pull`
- [x] create/switch branch
- [x] inspect `git diff`
- [x] stage changes
- [x] commit
- [x] push
- [x] open PR
- [x] merge
- [x] recover/correct a bad change (the rejected Venge removal was restored in a later focused commit)

**Important:** `git checkout` is not the prerequisite. The prerequisite is understanding the basic **clone → branch → edit → diff → commit → push → PR/merge** workflow.

## 5. Codex Workflow

- [x] Run Codex from inside the repo
- [x] Ask Codex to explain the repository structure
- [x] Ask Codex how the website is built and deployed
- [x] Ask Codex to identify the safest file for a trivial test edit
- [x] Learn how to:
  - [x] give Codex a bounded task
  - [x] inspect its diff
  - [x] ask it to test/verify
  - [x] undo/reject bad changes
  - [x] ask it questions before allowing execution

## Milestone Exit Test

I can independently:

> clone/open repo → run site locally → ask Codex for a small change → inspect result → verify in browser → commit → push → deploy.

Do not continue until this works.

---

# Milestone 2: Tutorial Zone

**Goal:** Make deterministic, low-risk, easy-to-verify production changes. Practice the full agent workflow without requiring product judgment.

**Status: Complete (August 10, 2026).** The focused typo, placeholder, broken-link, formatting, production-deployment, and mobile/layout checks are complete.

**Estimated time: 1-2 hours**

## Obvious Fixes

- [x] Fix known typos and grammar errors
  - [x] `worl`
  - [x] `3 time a week`
  - [x] `Produest`
  - [x] other obvious spelling/grammar issues Codex found during the focused audit
- [x] Fix duplicated headings such as:
  - [x] Fitness → Fitness
  - [x] eSports → eSports
- [x] Remove `Investments: Coming soon` (placeholder cleanup only; final Investments decision remains open for Milestone 3)
- [x] Review Advisor @ Venge.io reference; decision: keep it (restored and updated after the removal was rejected)
- [x] Remove the currently broken LinkedIn link
- [x] Verify and remove clearly dead/outdated external links found during the focused audit
- [x] Replace the broken METU eSports Wayback link with the visually intact October 17, 2014 capture
- [x] Use the October 20, 2015 Wayback capture for Mobile Monday Ankara
- [x] Audit social/profile links and remove the broken LinkedIn profile
- [x] Remove obviously obsolete placeholders found during the focused audit
- [x] Fix visibly broken formatting found in Book Notes and the portfolio heading
- [x] Complete the deferred mobile/layout check and fix any trivial bugs discovered

**Mobile/layout decision (August 10, 2026):** Goktug manually checked Home, About, Blog, Quotes, Book Notes, navigation, and external profile links on mobile. Everything worked, no layout bug was found, and the deliberately simple mobile presentation should remain unchanged unless a concrete usability problem appears.

**Note (August 10, 2026):** During an ad hoc About-page cleanup, the retired CocoaPods badges were replaced with verified historical download totals and the four Swift projects were consolidated into a nested list. Each project shows its GitHub star count beside its linked name, followed by separate description and historical CocoaPods-download bullets. This was not a pre-existing Milestone 2 task.

## Agent Exercises

**Status: Completed** through separate focused commits for discovery, approved edits, placeholders, links, formatting, and build verification.

Use separate small tasks/commits where practical:

1. "Find obvious spelling mistakes. Show me the list before editing."
2. "Fix only these approved mistakes."
3. "Find dead placeholders and stale empty sections. Do not edit yet."
4. "Remove these approved sections."
5. "Run/build the site and report anything broken."

## Verification

For every task:

- [x] Read the diff
- [x] Run/build locally
- [x] Check affected page visually
- [x] Commit
- [x] Push
- [x] Confirm production after deploy

## Milestone Exit Test

I am comfortable giving Codex a **clear, deterministic task** and letting it execute without hand-holding every line.

---
