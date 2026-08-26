<a href="https://silkie.io"><img src="assets/banner.png" alt="SiLKiE — Standardized List for Kit and Equipment" width="100%"></a>

## Hello there.

I'm Chris Grimsley. Building SiLKiE — inventory, loadouts and SOPs for people who keep gear ready.

It's inventory tracking, repeatable loadout checklists and SOP documents in one
place — for shooters, campers, and anyone whose packing list currently lives
across four notes apps. React 19 and Django 5, running at
**[silkie.io](https://silkie.io)**.

The code is in a private repo, so this page is generated rather than written. A
script reads the local git history and task queue each night, drops what
shouldn't be public, and rewrites this file. There's a note at the bottom on how
it decides.

[![silkie.io](https://img.shields.io/badge/silkie.io-0e0e0c?style=for-the-badge&logo=firefoxbrowser&logoColor=93b571)](https://silkie.io)
[![Email](https://img.shields.io/badge/support@silkie.io-0e0e0c?style=for-the-badge&logo=maildotru&logoColor=93b571)](mailto:support@silkie.io)
[![Instagram](https://img.shields.io/badge/Instagram-0e0e0c?style=for-the-badge&logo=instagram&logoColor=93b571)](https://www.instagram.com/silkie.io/) [![X](https://img.shields.io/badge/X-0e0e0c?style=for-the-badge&logo=x&logoColor=93b571)](https://x.com/Silkieio)

---

## 📦 Shipping log

Most recent first. `×N` means a run of commits that collapsed to one line.

| Date | Area | What changed |
| :--- | :--- | :--- |
| `2026-08-26` | Accounts | Test coverage |
| `2026-08-26` | Harness | Cover the harness backup repo, clips and the QR fix |
| `2026-08-26` | Harness | Document the profile README generator |
| `2026-08-26` | Frontend | Use the reticle mark as the favicon and nav logo |
| `2026-08-25` | Repo | Untrack the autonomous harness from the app repo |
| `2026-08-25` | Backend | Register WeasyPrint DLL dir so PDF tests run on Windows |
| `2026-08-25` | Harness | Fix |
| `2026-08-25` | Frontend | Fix |
| `2026-08-25` | Inventory | Fix |
| `2026-08-25` | Frontend | Maintenance |
| `2026-08-25` | Ad Studio | New work |
| `2026-08-24` | Ad Studio | Move Ad Studio into its own switchable top-level tab |
| `2026-08-24` | Ad Studio | Local ad creative generator + dashboard integration |
| `2026-08-24` | Frontend | New work |

Recently in: **Frontend** (4) · **Harness** (3) · **Ad Studio** (3) · **Accounts** (1) · **Repo** (1) · **Backend** (1)

> 7 of the rows above show a generic summary instead of the real
> commit subject — the filter drops any subject carrying a file path, a line
> number, or hardening language.

---

## 📊 By the numbers

<img src="assets/card-activity.svg" alt="Build activity: 467 commits all time, 363 in the last 7 days, 408 in the last 30, 9 days with a commit, 3-day current streak, 3-day longest, 55 test files, building since 2025-12" width="49%">
<img src="assets/card-harness.svg" alt="Autonomous harness: 82 cycles over 3 nights, 75 tasks shipped unattended, 65 tasks completed, 0 queued, 10 blocked, 7.7 machine hours, last run 2026-08-26" width="49%">

<img src="assets/card-languages.svg" alt="Language mix across the codebase" width="100%">

---

## 🤖 The night shift

SiLKiE has a second contributor: an autonomous Claude Code harness that runs
between 00:00 and 08:00 and is not allowed to touch anything outside that window.

It works one task per cycle. A runner script — never the model — owns git and the
queue: it claims the top task, cuts an `ai-dev-*` branch, dispatches a worker
agent that may only edit files, then runs the real gates (`tsc`, `eslint`,
`vitest`, `vite build`, `ruff`, `pytest`) against whatever came back. Green
merges to the dev branch and the task is marked done. Red marks it blocked, keeps
the branch, and moves on. `main` is read-only to every agent, enforced by a shell
hook rather than a promise in a prompt.

Audits run separately and read-only: security, performance, mobile, feature
completeness and compliance sweeps each file their findings back into the queue
as tasks instead of editing anything themselves.

---

## 🎬 See it

<table>
<tr><td align="center" valign="top"><a href="https://silkie.io" title="SiLKiE product spot"><img src="assets/clip-spot.webp" width="200" alt="SiLKiE product spot"></a><br><sub><b>The spot</b></sub></td><td align="center" valign="top"><a href="https://silkie.io" title="SiLKiE landing page walkthrough"><img src="assets/clip-landing.webp" width="200" alt="SiLKiE landing page walkthrough"></a><br><sub><b>Landing</b></sub></td><td align="center" valign="top"><a href="https://silkie.io" title="Tracking gear down to the mag count"><img src="assets/clip-inventory.webp" width="200" alt="Tracking gear down to the mag count"></a><br><sub><b>Inventory</b></sub></td><td align="center" valign="top"><a href="https://silkie.io" title="Finding people to train with"><img src="assets/clip-tribe.webp" width="200" alt="Finding people to train with"></a><br><sub><b>Tribe Finder</b></sub></td></tr>
</table>

---

## 🧰 Built with

![React](https://img.shields.io/badge/React_19-0e0e0c?style=for-the-badge&logo=react&logoColor=93b571)
![TypeScript](https://img.shields.io/badge/TypeScript-0e0e0c?style=for-the-badge&logo=typescript&logoColor=93b571)
![Vite](https://img.shields.io/badge/Vite_7-0e0e0c?style=for-the-badge&logo=vite&logoColor=93b571)
![Tailwind](https://img.shields.io/badge/Tailwind_v4-0e0e0c?style=for-the-badge&logo=tailwindcss&logoColor=93b571)
![Django](https://img.shields.io/badge/Django_5-0e0e0c?style=for-the-badge&logo=django&logoColor=93b571)
![Python](https://img.shields.io/badge/Python-0e0e0c?style=for-the-badge&logo=python&logoColor=93b571)
![Postgres](https://img.shields.io/badge/PostgreSQL-0e0e0c?style=for-the-badge&logo=postgresql&logoColor=93b571)
![Stripe](https://img.shields.io/badge/Stripe-0e0e0c?style=for-the-badge&logo=stripe&logoColor=93b571)
![Cloudflare](https://img.shields.io/badge/Cloudflare-0e0e0c?style=for-the-badge&logo=cloudflare&logoColor=93b571)
![Playwright](https://img.shields.io/badge/Playwright-0e0e0c?style=for-the-badge&logo=playwright&logoColor=93b571)
![Claude](https://img.shields.io/badge/Claude_Code-0e0e0c?style=for-the-badge&logo=anthropic&logoColor=93b571)

---

<table>
<tr>
<td width="180" valign="middle">
<img src="assets/qr.png" alt="QR code to silkie.io" width="160">
</td>
<td valign="middle">

### Try it

Point a camera at that, or go to **[silkie.io](https://silkie.io)**.
Questions, bug reports, or you want in on the beta — **[support@silkie.io](mailto:support@silkie.io)**.

Development progress in public: **[silkie_public_progress](https://github.com/CGGrimsley/silkie_public_progress)**

</td>
</tr>
</table>

---

#### About this page

A Python script in the private SiLKiE repo builds this file nightly from local
git and the task queue. It is allow-first: a commit subject is published only if
it is plain prose with no path, no line reference, no internal task id and no
hardening vocabulary. Everything else becomes the generic line you see above.
Task text, branch names, spend and file paths never leave the machine.

A false positive there costs a dull row and a false negative costs a leak, so it
fails closed.

<sub>Last generated 2026-08-26 05:01 UTC · latest commit 2026-08-26</sub>
