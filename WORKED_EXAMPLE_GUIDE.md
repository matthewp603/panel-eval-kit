# PANEL copy-paste kit — alt-text pilot

Everything you need to type into PANEL tonight, step by step, in order. Open PANEL,
pick either door, and work top to bottom: paste each block into its panel, then tick
the step complete (the mode log fills itself).

## Honesty note (read once)

These grades are **sample data, not blind grades** — they exist so you can walk the
full loop tonight without spending hours grading. If you show the packet to Michael
or Nancy, say exactly that: "sample data so you can see the full loop." A real eval
means you grade blind (Step 5) before any judge runs.

---

## Step 0.2 — Eval plan

**Eval name:** `Alt-text pilot — PowerPoint images (SAMPLE DATA)`

**Scenario:** A PowerPoint presenter puts images on slides; audience members using
screen readers need to know what each image shows and why it is there.

**Why it matters:** When alt text is wrong, thin, or missing, screen-reader users miss
the point of the slide. Copilot-generated alt text ships to millions of presentations
— we need to know it is good before it does.

**Kappa trust bar:** `0.60`

**Evidence log** (3 rows — source, then note):

1. `W3C alt decision tree (WCAG technique H37)` / Decorative vs informative images;
   informative images need purpose-equivalent text alternatives.
2. `WebAIM Screen Reader User Survey` / Users prefer concise alt text that conveys
   purpose; long or empty alt text is a top complaint.
3. `Microsoft Accessibility Insights guidance` / Non-text content needs a text
   alternative that serves the equivalent purpose.

**Constructs** (3 rows — name, then one-sentence meaning):

1. `descriptive_accuracy` / The alt text correctly describes what is visible — objects,
   setting, salient details.
2. `functional_usefulness` / The alt text serves the listener's need — what the image
   is doing on the slide.
3. `concision` / The alt text is brief — complete in one breath, no filler.

---

## Step 1 — Inputs (12 rows)

Columns: ID | Input (image) | Reference output (ideal alt text) | Type | Risk

- **INPUT-01** | Golden retriever puppy lying in grass | Golden retriever puppy lying in green grass, looking at the camera. | photo | standard
- **INPUT-02** | Barista steaming milk at an espresso machine | Barista steaming milk at an espresso machine in a café. | photo | standard
- **INPUT-03** | Mountain lake at sunset, sun rays through clouds | Mountain lake at sunset, sun rays breaking through clouds over the water. | photo | standard
- **INPUT-04** | Indoor farmers market, vegetable crates and shoppers | Shoppers browsing vegetable crates at an indoor farmers market. | photo | standard
- **INPUT-05** | City at night, traffic light trails and billboards | City street at night with traffic light trails and glowing billboards. | photo | standard
- **INPUT-06** | Child riding bicycle past colorful playground slides | Child riding a bicycle past colorful playground slides. | photo | deep
- **INPUT-07** | Honey bee on a flower (macro) | Honey bee covered in pollen on a flower, extreme close-up. | photo | standard
- **INPUT-08** | MacBook, iPhone, and coffee cup on a table | MacBook, iPhone, and coffee cup arranged on a wooden table. | photo | standard
- **INPUT-09** | Ocean wave crashing | Ocean wave crashing, white spray against deep blue water. | photo | light
- **INPUT-10** | Elderly couple walking together | Elderly couple walking together outdoors, holding hands. | photo | deep
- **INPUT-11** | Red vintage convertible parked by a wooden fence | Red vintage convertible parked beside a wooden fence. | photo | standard
- **INPUT-12** | Hot air balloons over Cappadocia rock formations | Hot air balloons floating over Cappadocia's rock formations at dawn. | photo | standard

**What the panel graded** — the mock candidate alt texts (keep this list open while grading):

- **INPUT-01:** "A cute dog lying in the grass outside."
- **INPUT-02:** "Image of a person making coffee with a machine."
- **INPUT-03:** "Mountain lake at sunset with dramatic clouds."
- **INPUT-04:** "People shopping for vegetables at an indoor market with crates of produce."
- **INPUT-05:** "A city at night."
- **INPUT-06:** "A kid on a bike near a playground."
- **INPUT-07:** "Close-up of a bee on a yellow flower."
- **INPUT-08:** "Overhead flat-lay of a laptop, smartphone, and coffee cup on a desk, styled workspace photography."
- **INPUT-09:** "In this image we can see a large ocean wave crashing down with white foam spray everywhere."
- **INPUT-10:** "An old couple walking down a street together."
- **INPUT-11:** "A beautiful shiny red vintage convertible car from the 1960s parked on the street next to a rustic wooden fence on a sunny day with a bright blue sky and fluffy white clouds overhead."
- **INPUT-12:** "Colorful hot air balloons flying over rocky landscape."

---

## Steps 2/3 — Rubric v1 (enter this; v2 comes later at Step 15)

### descriptive_accuracy
- **Definition:** The alt text correctly describes what is actually visible — objects,
  setting, and the salient visual details a sighted person would notice.
- **User evidence:** W3C alt decision tree (WCAG technique H37): purpose-equivalent
  text alternatives.
- **2 =** All salient elements named correctly; nothing invented. A listener could
  picture the scene.
- **1 =** Broadly correct but misses a salient detail, or one minor inaccuracy.
- **0 =** Misidentifies the subject or scene, or invents prominent details not present.
- **Boundary:** If the missing detail IS the point of the image (the sun rays in a
  sunset photo), two reasonable graders can still disagree on what counts as 'the
  point' — that disagreement is rubric material, not grader error.

### functional_usefulness
- **Definition:** The alt text serves the listener's actual need in context — a
  PowerPoint audience member on a screen reader learns what the image is doing on
  the slide, not just what it looks like.
- **User evidence:** WebAIM Screen Reader User Survey: users prefer alt text that
  conveys purpose, kept concise.
- **2 =** Conveys both content and function — why this image is on this slide.
- **1 =** Describes content accurately but gives no functional framing.
- **0 =** Content-free ('image of...') or misleading about the image's purpose.
- **Boundary:** Pure description with zero functional signal is a 1, not a 0. 0 is
  reserved for misleading or content-free text.

### concision
- **Definition:** The alt text is appropriately brief — complete in one breath, roughly
  under 125 characters, with no filler phrases like 'image of' or 'in this image we
  can see'.
- **User evidence:** WebAIM survey + platform guidance: screen readers announce alt
  text inline; verbosity taxes every listener.
- **2 =** About 125 characters or fewer, no filler; nothing a listener would want cut.
- **1 =** 125-200 characters, or one filler phrase; still listenable.
- **0 =** Over ~200 characters, or padded with filler.
- **Boundary:** Character count is a guide, not a law — a 140-char text with zero waste
  can be a 2; a 90-char text with 'image of a' filler is a 1.

**Step 15 v2 edit** (do this live after the INPUT-06 adjudication — hit Bump, paste
this as the changelog note):

- In `descriptive_accuracy`, change **1 =** to: "Broadly correct but misses a salient
  detail, or one minor inaccuracy. (v2: a missed salient detail caps the score at 1 —
  it can never be a 2, but the miss alone does not make it a 0.)"
- Changelog note: `INPUT-06 adjudication: a missed salient detail caps accuracy at 1,
  not 0.`

---

## Step 5 — Your blind grades (36 cells)

| Input | accuracy | usefulness | concision |
|---|---|---|---|
| INPUT-01 | 1 — ""A cute dog" — misses golden retriever + puppy; "cute" is editorial" | 1 | 2 |
| INPUT-02 | 1 — ""making coffee" vague; misses steaming milk" | 1 | 1 — ""Image of a" filler" |
| INPUT-03 | 1 — "cand misses the sun rays — the money detail of this image" | 1 | 2 |
| INPUT-04 | 2 | 1 | 2 |
| INPUT-05 | 1 | 0 — ""A city at night." tells the listener nothing" | 2 |
| INPUT-06 | 2 — "listener pictures the right scene" | 1 | 2 |
| INPUT-07 | 2 | 1 | 2 |
| INPUT-08 | 2 | 1 — "describes well; no signal for why it is on the slide" | 2 |
| INPUT-09 | 2 | 1 | 1 — ""In this image we can see" filler" |
| INPUT-10 | 1 — "misses holding hands; "old" is reductive" | 1 | 2 |
| INPUT-11 | 0 — "invents 1960s, blue sky — not verifiable" | 1 | 0 — "~210 chars, padded" |
| INPUT-12 | 1 — ""rocky landscape" — never names Cappadocia" | 1 | 2 |

_Score first, evidence quotes where shown. These are the reference standard._

---

## Step 7 — Judge prompt (paste into a FRESH Claude session, then a FRESH ChatGPT session)

> You are a grading judge for PowerPoint image alt text. Score the CANDIDATE alt
> text against the rubric below — score the candidate, not the image. Rules: quote
> the shortest span of the candidate that justifies each score; never invent details
> the candidate doesn't state; if the candidate is ambiguous, score "Unknown" rather
> than guessing; score each input independently, never comparing candidates to each
> other. Output one line per input: INPUT-ID | construct: score | evidence quote.
>
> Then paste the full rubric (all three constructs with 0/1/2 anchors).

_Run it once per judge. Neither session sees the other's grades._

---

## Step 8 — Claude grades (transfer each SCORE)

| Input | accuracy | usefulness | concision |
|---|---|---|---|
| INPUT-01 | 1 | 1 | 2 |
| INPUT-02 | 1 | 1 | 1 |
| INPUT-03 | 2 — "all named elements present; rays are atmosphere" | 1 | 2 |
| INPUT-04 | 2 | 1 | 2 |
| INPUT-05 | 1 | 0 | 2 |
| INPUT-06 | 1 — "misses "colorful slides", a named salient detail" | 1 | 2 |
| INPUT-07 | 2 | 1 | 2 |
| INPUT-08 | 2 | 1 | 2 |
| INPUT-09 | 2 | 1 | 1 |
| INPUT-10 | 1 | 1 | 2 |
| INPUT-11 | 0 | 1 | 0 |
| INPUT-12 | 1 | 1 | 2 |

---

## Step 9 — ChatGPT grades (transfer each SCORE)

| Input | accuracy | usefulness | concision |
|---|---|---|---|
| INPUT-01 | 1 | 1 | 2 |
| INPUT-02 | 1 | 1 | 1 |
| INPUT-03 | 1 | 1 | 2 |
| INPUT-04 | 2 | 1 | 2 |
| INPUT-05 | 1 | 0 | 2 |
| INPUT-06 | 2 | 1 | 2 |
| INPUT-07 | 2 | 1 | 2 |
| INPUT-08 | 2 | 2 — ""styled workspace photography" signals the slide's remote-work theme" | 2 |
| INPUT-09 | 2 | 1 | 2 — "under 125 chars" |
| INPUT-10 | 1 | 1 | 2 |
| INPUT-11 | 1 — "car and fence are right; era/sky are plausible" | 1 | 2 — "detailed and vivid" |
| INPUT-12 | 1 | 1 | 2 |

---

## Steps 10-13 — Agreement (what you should see)

Bar 0.60. Verified against compute_agreement.py:

| Construct | you vs Claude | you vs ChatGPT |
|---|---|---|
| descriptive_accuracy | **0.71** PASS | **0.84** PASS |
| functional_usefulness | **1.00** PASS | **0.64** PASS |
| concision | **1.00** PASS | **0.44** FAIL |

**Triage queue (6 items)** — log verdicts in Step 14:

1. INPUT-03 · accuracy — you 1 · Claude 2 · ChatGPT 1
2. INPUT-06 · accuracy — you 2 · Claude 1 · ChatGPT 2
3. INPUT-08 · usefulness — you 1 · Claude 1 · ChatGPT 2
4. INPUT-09 · concision — you 1 · Claude 1 · ChatGPT 2
5. INPUT-11 · accuracy — you 0 · Claude 0 · ChatGPT 1
6. INPUT-11 · concision — you 0 · Claude 0 · ChatGPT 2

---

## Step 14 — Adjudication log (6 entries)

Do **#1, #3, #4 live** — scripts below. Pre-log #2, #5, #6 any time (or all six live
if the room is into it).

**#2 — INPUT-06 · accuracy · rubric ambiguity** (pre-log)
Action: Two reasonable graders split on whether 'colorful slides' is salient. v2
anchor: a missed salient detail caps accuracy at 1. Rubric bumped to v2.

**#5 — INPUT-11 · accuracy · grader error** (pre-log)
Action: ChatGPT credited invented details (1960s, blue sky). Judge prompt already
forbids invention — flagged in readout, no rubric change.

**#6 — INPUT-11 · concision · grader error** (pre-log)
Action: ChatGPT scored a ~210-char padded output 2 on concision. Verbosity-bias note
filed (Step 18); ChatGPT blocked from concision until re-prompted.

### Live scripts — reasoning out loud

**#1 — INPUT-03 · accuracy — you 1, Claude 2.**
"Claude gave this a 2 — 'all named elements present.' I gave it a 1. The candidate
says 'mountain lake at sunset with dramatic clouds' — but the image is *sun rays
breaking through clouds*, that's the money detail, the reason the photo exists.
Claude scored the words; I scored the picture. Verdict: grader error — and it's a
useful one, because it shows the judge can be technically right and still miss the
point. No rubric change."

**#3 — INPUT-08 · usefulness — you 1, ChatGPT 2.** (the humble one)
"ChatGPT gave this a 2, citing 'styled workspace photography' as functional framing.
I gave it a 1 — pure description, no signal for why it's on the slide. But sitting
with it... 'styled workspace photography' *does* tell a remote-work audience what
this image is doing. ChatGPT's right. Verdict: my grade was wrong — correcting to 2,
no rubric change. The method caught *me*. That's the point."

**#4 — INPUT-09 · concision — you 1, ChatGPT 2.**
"Ninety-eight characters, but it opens with 'In this image we can see' — pure filler,
the exact phrase the rubric names. ChatGPT scored it a 2 anyway. Same pattern as
INPUT-11. Verdict: grader error, second data point for the verbosity-bias note. This
is why ChatGPT doesn't grade concision in this eval."

---

## Steps 17/18 — Bias notes (2 entries)

- **Verbosity** · chatgpt: "Generous to long outputs: scored 2 vs human 0 on INPUT-11
  concision (~210 chars); 2 vs 1 on INPUT-09. Do not trust ChatGPT on concision until
  re-prompted."
- **Position** · claude: "No position effect observed — single-output grading, no
  pairwise presentation in this pilot."

---

## Step 20 — Dashboard talking points

- Human pass rates: accuracy **42%**, usefulness **0%**, concision **75%**.
- "Usefulness is 0% — none of the mock outputs tell the listener *why* the image is
  on the slide. The candidate describes; it never serves. That's the product gap this
  eval found."
- Agreement: two constructs green, concision red for ChatGPT (0.44) — the story that
  produced the bias note and the ship/hold call.
- Export: stakeholder packet (HTML) + gold_set.csv + tasks.csv + agreement_report.txt.
  "This is what the team gets."

## The one-line story

"PANEL convenes a panel — me plus two model families — and measures whether the
models judge like I do. Two constructs green, one red, and the red one told us
exactly what to fix. That's not a demo of AI grading. That's a demo of *trust*."