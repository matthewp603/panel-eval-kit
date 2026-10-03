# PANEL — Convene the panel. Trust the verdict.

PANEL is a training and workbench kit for running AI evaluations. It teaches a
repeatable 24-step method and gives you a place to actually do the work: plan
the eval, write the rubric, grade outputs yourself, run two LLM judges, measure
how much the judges agree with you, resolve the disagreements, check for bias,
and ship a readout a stakeholder can trust.

Everything runs from one file (`index.html`). There is no install, no account,
no server, and no internet needed. Your data stays in your browser.

Built by Matt Priore · October 2026

## What is in this repo

- **`index.html`** — the whole kit: the 24-step training path, the eval
  workspace, and the Step 22 generators (readout deck, results dashboard,
  offline package).
- **`WORKED_EXAMPLE_GUIDE.md`** — a copy-paste kit for the sample eval (alt
  text for PowerPoint images): eval plan fields, 12 inputs, the rubric, all
  108 grades, the judge prompt, adjudication verdicts, and bias notes. Paste
  each block into the matching panel to walk the full loop.

## How to open it

1. Download `index.html` (or clone this repo and open the file).
2. Double-click it. It opens in your browser. That is the whole setup.

Optional: host it free on GitHub Pages so the team can open it from a link
(see "Sharing with a team" below).

## Two doors

The first screen offers two ways in. You can switch any time from the nav.

- **New to AI evals?** — the guided path. Each step teaches one idea, then its
  DO IT HERE panel lets you do that step for real. Work top to bottom.
- **Done this before?** — the workspace. The same panels, dense and
  lesson-free, for people who already know the method. Link straight to it
  with `?mode=workspace`.

## The 24 steps at a glance

The method has three acts: set up, grade, and trust.

**Set up.** 0.1 Read the concepts. 0.2 Write the eval plan: the scenario, why
it matters, your evidence, your constructs, and your kappa trust bar. 1 Build
the input pool (inputs, reference outputs, candidate outputs, types, risk
tiers). 2 Write rubric v1 with plain-language anchors. 3 Red-team the rubric
and keep what survives.

**Grade.** 4 Read every input with fresh eyes, no scores yet. 5 Grade blind
yourself. 6 Log how each step was done (human-only, human plus AI, AI-only).
7 Generate the judge prompt. 8 Run Judge A and paste its grades. 9 Run Judge B
and paste its grades. 10 Confirm the judges worked independently.

**Trust.** 11 Measure agreement (Cohen's kappa, per construct) against your
trust bar. 12 Read the verdict in plain language. 13 Work the disagreement
queue, worst first. 14 Adjudicate each disagreement with the decision tree:
rubric ambiguity, grader error, broken input, wrong reference, or a policy
call. 15 Fold rubric fixes back into a new rubric version. 16 Compare rounds.
17 Check for position bias. 18 Check for verbosity bias. 19 Generate synthetic
inputs to fill thin slices of your pool, then validate a sample by hand.
20 Read the live dashboard. 21 Write the summary. 22 Ship the proof.

## How to run your first eval

1. Open `index.html` and pick the guided path.
2. Do Step 0.2 in its DO IT HERE panel: name the eval, describe the scenario,
   set the kappa trust bar (0.60 is the usual starting point).
3. Do Step 1: add your inputs. The worked example in
   `WORKED_EXAMPLE_GUIDE.md` gives you 12 ready-made rows to practice with.
4. Do Step 2: write the rubric. Every construct gets a definition, 2/1/0
   anchors, and a boundary rule.
5. Do Steps 4 and 5: read through, then grade blind. No judge results in view.
6. Do Step 7: copy the generated judge prompt, run it once per judge in fresh
   sessions, then paste each judge's full output into Steps 8 and 9. PANEL
   parses the scores for you.
7. Do Steps 11 to 14: read the kappa table, open the disagreement queue, and
   adjudicate. This is where the eval earns its keep.
8. Do Step 21: write the summary from the five boxes. Do Step 22: generate the
   deck, the dashboard, and the offline package.

Check each step's box as you finish it. The card collapses, the progress bar
moves, and your place is saved if you close the tab.

## DO IT HERE panels

Every step card has a DO IT HERE panel. That is the workspace: real forms,
tables, and generators, not instructions about other tools. Definitions and a
worked example sit above every field, so nobody has to guess what a field
means. Editable tables come with shaded example rows you can delete.

## Step 22: ship the proof

When all 24 boxes are checked, you get a small celebration, then Step 22
builds three things from your data, in the browser:

1. **A PowerPoint deck** (`.pptx`): title, what was measured, the rubric,
   judge agreement, adjudication highlights, bias checks, the summary, and how
   to read the result.
2. **A standalone HTML dashboard**: filters by construct, grader, and input,
   kappa charts, score distributions, the disagreement queue, and the mode log.
3. **An offline ZIP package**: every file the workflow would have produced by
   hand (eval plan, tasks, rubric, judge prompt, gold set, agreement report,
   adjudications, bias notes, mode log, red-team findings, synthetic inputs,
   summary), plus the dashboard and the deck. Unzip it and it is a complete,
   commit-ready record of the eval.

## Your data

- Everything you type is saved in your browser (localStorage) on your device.
  Nothing is uploaded anywhere.
- **Export any time**: Step 22 gives you the stakeholder packet, CSVs, the
  agreement report, and the offline package.
- **Start over**: the workspace header has a "Start new eval" button. Export
  first, because it clears your saved data.

## Trying the sample eval

Open `WORKED_EXAMPLE_GUIDE.md` and follow it block by block, pasting each
block into the matching step's panel. In about an hour you will have a
complete eval: kappa tables, adjudications, bias notes, and a readout. The
grades in the guide are sample data for learning the loop, not blind grades
from a real study. A real eval means you grade blind (Step 5) before any
judge runs.

## A note on judges

The kit is judge-neutral. It calls them Judge A and Judge B, and it works
with any two models (or the same model twice, or one model and one human).
Pick whatever judges your team actually uses.

## Sharing with a team

1. Push this repo to GitHub.
2. In the repo: **Settings → Pages** → Source: **Deploy from a branch**,
   branch `main`, folder `/ (root)` → **Save**.
3. After about a minute the kit is live at
   `https://<your-name>.github.io/<repo-name>/`.

Share the link. Anyone who opens it gets their own blank workspace on their
own device.

## What PANEL is not

PANEL does not call any AI for you. You run the judges yourself (in whatever
tool your team uses) and paste the results back in. That is deliberate: the
method stays independent of any vendor, and your data never leaves your
machine.
