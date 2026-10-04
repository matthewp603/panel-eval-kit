# PANEL — the AI eval workbench

An interactive, single-file web companion to the **Office AI Eval SOP** — a visual training
module that walks through all 22 steps (WHO / WHAT / WHERE / WHEN / WHY / HOW), plus:

- **Kappa lab** — drag the trust bar and watch real agreement-script output flip between pass/fail
- **Adjudication simulator** — walk the Step 14 decision tree on real sample disagreements
- **Quiz** — 12 questions (recall + scenario) with instant feedback and a personalized study guide
- **Eval workspace** — do the eval inside the module: plan, tasks, rubric, grading grids,
  judge transfer, adjudication log, bias notes, auto mode log, live dashboard, one-click
  stakeholder packet + CSV/report exports

Built by Matt Priore · Worked example: alt text for PowerPoint images · October 2026

## View it locally

Just open `index.html` in a browser. No build step, no dependencies.

## Host it free on GitHub Pages

1. Create a new repo on GitHub (e.g. `ai-eval-training-module`). Don't add a README/license — you'll upload your own files.
2. Upload `index.html` (and this README) to the repo — via the web UI ("Add file → Upload files") or:
   ```bash
   git init && git add index.html README.md && git commit -m "AI eval training module"
   git branch -M main && git remote add origin https://github.com/<you>/ai-eval-training-module.git
   git push -u origin main
   ```
3. In the repo: **Settings → Pages** → under "Build and deployment", set **Source** to
   **"Deploy from a branch"**, branch `main`, folder `/ (root)` → **Save**.
4. Wait ~1 minute. Your module is live at `https://<you>.github.io/ai-eval-training-module/`.

Share that link with anyone — no login required to view it.

## Front door: guided path vs workspace

First visit (or no saved choice) opens the **guided path** — the full training module.
Two doors in the hero, plus a Guided/Workspace toggle in the nav:

- **New to AI evals?** → guided path: learn each step, then do it in the step cards'
  🛠 DO IT HERE panels.
- **Done this before?** → workspace: a dense 9-phase workbench (Setup → Inputs → Rubric →
  Grade → Judges → Agreement → Adjudicate → Bias checks → Ship) reusing the same panels,
  no lessons in the way.

Your choice persists on the device; `?mode=workspace` deep-links straight to the
workbench. The workspace header shows live stats (inputs · graded · rubric version ·
open disagreements) and a **Start new eval** button (export first — it clears local state).

## Worked example — copy-paste kit

`WORKED_EXAMPLE_GUIDE.md` holds everything needed to walk the 12-image alt-text
pilot end to end, step by step: eval plan fields, all 12 inputs with reference
outputs and mock candidate outputs, rubric v1 anchors (+ the v2 edit for Step 15),
all 108 grades with evidence quotes, the judge prompt, 6 adjudication verdicts with
live reasoning-out-loud scripts, bias notes, and dashboard talking points.
Kappa values are verified against `compute_agreement.py`.

## Do the eval inside the module (workspace)

Each step card has a **🛠 DO IT HERE** panel — a real workspace, not just instructions:

- **Step 0.2**: eval plan form (scenario, evidence log, constructs, kappa bar)
- **Step 1**: tasks table (add/edit rows, load 12 samples, CSV-shaped)
- **Steps 2/3/15**: rubric builder (anchors per construct, version bumps with changelog)
- **Step 5**: blind grading grid (scores + evidence quotes; builds itself from your tasks × constructs)
- **Steps 8/9**: judge grade transfer grids
- **Step 14**: adjudication log · **Steps 17/18**: bias notes · **Step 6**: auto-appended mode log
- **Step 20**: live dashboard — pass rates, kappa vs your bar, open disagreements, coverage,
  all computed from your workspace data as you go

Everything saves in the browser (localStorage). The Kappa Lab reads your workspace
grades directly, or paste any Gold Set CSV.

## Hand the repo to stakeholders

**Step 20 → Download stakeholder packet (HTML)**: a self-contained `eval-packet.html`
with your plan, rubric, kappa table, adjudications, bias notes, and mode log —
commit it to the repo. **Download data** gives you `gold_set.csv`, `tasks.csv`, and
`agreement_report.txt` in the SOP's exact CSV conventions (grader-grouped columns),
so the files round-trip with the Google Sheets workbook both ways.

Suggested repo layout:

```
my-eval/
  eval-packet.html        # the stakeholder handoff (start here)
  gold_set.csv            # grades: matt_*, claude_*, chatgpt_ per construct
  tasks.csv               # inputs + reference outputs
  agreement_report.txt    # kappa table + triage list
```

The module is the cockpit; the repo is the system of record. (Prefer Google Drive?
the per-step "Open template" buttons from `TEMPLATE_LINKS` take you to the
Docs/Sheets versions of the same artifacts.)

## Connect your templates (one-click "Open" buttons)

Every step card has a slot for a button that opens the exact template for that step
(Eval Plan, Rubric, Blind Grading Sheet, Gold Set, Mode Log, Judge Prompt, Dashboard…).
To enable them:

1. In Google Drive, set your Templates doc copy, Workbook copy, `compute_agreement.py`,
   and Concepts Guide to **"Anyone with the link can view"**.
2. Open `index.html`, find `TEMPLATE_LINKS` near the top of the `<script>` and paste
   the four URLs in. Re-upload.
3. Users click through and do **File → Make a copy** for their own eval.

Until the links are filled in, the module shows a quiet hint instead of buttons —
and the in-browser kappa calculator (Kappa Lab → "Run it on your own data") works
with zero setup: paste any Gold Set CSV and get the kappa table + triage list,
computed locally, nothing uploaded.
