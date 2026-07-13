---
name: HomeTest Milestone Plan and Workshop Plan — State of Play as at 13 July 2026
description: Forensic handoff covering the two live HomeTest procurement artefacts — Plan Detail and Workshop Plan — that Scott owns as part of the Future State Team. Read before making any edit to either file.
type: handoff
snapshotDate: 2026-07-13
---

# HomeTest Milestone Plan and Workshop Plan — State of Play, 13 July 2026

## 1. Headline posture

Two web pages carry the HomeTest procurement plan. Both are live on GitHub Pages, both are behind a sessionStorage auth gate, both are hand-maintained HTML rather than a framework build. Scott owns both as part of the Future State Team commercial workstream. James Cowley has now provided feedback on both. The next chat (Fable 5) will apply that feedback. The files are stable, tag-balanced, and safe to edit as at 13 July.

The two files are:

- `HomeTest Operating Model - Plan Detail.html` — the milestone plan proper. Contains the Six Cornerstones panel, the roadmap dot view, the value scenario filter, the full matrix of stage activities, the Plan C detail section and a compact workshop strip that links to the workshop page.
- `HomeTest Operating Model - Workshop Plan.html` — the standalone workshop programme. Fifteen workshops distributed across S1 to S5, each a click-through with attendees, prep, objectives, decisions to land and outputs. Includes a value scenario filter that mirrors Plan Detail.

Both files are also mirrored to the NHS Commercial Model root as auth-stripped local viewing copies (`HomeTest Plan.html`, `HomeTest Workshop Plan.html`).

## 2. Timeline of the current phase

| Date | Event |
|------|-------|
| 6 Jun 2026 | HomeTest TOM deploy pattern moves to direct GitHub Pages; Desktop UPLOAD-THIS-ONE retired. |
| 22 Jun 2026 | Playback in Leeds. Deputy Director decisions land on open framework (~3yr+1) over dynamic framework. |
| 22 Jun 2026 | Recommendation Paper v1.1 finalised covering Plan A (NHSE-administered Open Framework under PA23, earliest Aug 2027) and Plan C (commissioner-led interim). |
| 23 Jun 2026 | RDUH MoU FINAL signed by NHSE; ~200 PSA-AS patients under direct mandate. |
| 9 Jul 2026 | Scott and James Cowley discuss milestone plan structure and framing. Transcript-driven changes queued. |
| 9 Jul 2026 | Six Cornerstones structure introduced (replaces earlier "Cardinal Four" framing). Plan A + Plan C both flowed through Plan Detail. |
| 10 Jul 2026 | Plan Detail restructured — matrix regrouped by cornerstone / sourcing / programme inputs / workshops / ITT. ITT specification x4 activities moved from S2 to S1. Chronological sequence numbering added then removed on user preference. |
| 10 Jul 2026 | Workshop Plan built as a standalone page mapped across S1 to S5 with fifteen workshops. Value scenario filter added. |
| 11 Jul 2026 | Owner labels standardised. Legend moved above roadmap. |
| 13 Jul 2026 | Mandie Holt moved from core group to optional-per-workshop. State of play captured for Fable 5 handoff. James Cowley feedback awaited. |

## 3. Work done and landed

### Files on the durable drive

**Live artefacts (edit these):**
- `NHS Commercial Model/Operating Model/HomeTest-TOM/HomeTest Operating Model - Plan Detail.html` (~217 KB)
- `NHS Commercial Model/Operating Model/HomeTest-TOM/HomeTest Operating Model - Workshop Plan.html` (~48 KB)

**Local viewing copies (auth stripped; overwritten each save from the live copy):**
- `NHS Commercial Model/HomeTest Plan.html`
- `NHS Commercial Model/HomeTest Workshop Plan.html`

**Deployed URLs (GitHub Pages, private repo `ScottEason1967/HomeTest-TOM`):**
- Plan Detail: `https://scotteason1967.github.io/HomeTest-TOM/HomeTest%20Operating%20Model%20-%20Plan%20Detail.html`
- Workshop Plan: `https://scotteason1967.github.io/HomeTest-TOM/HomeTest%20Operating%20Model%20-%20Workshop%20Plan.html`

Both sit behind a sessionStorage auth gate. Access code: `hometest2026`.

**Backups written this week (in the HomeTest-TOM folder alongside the live file):**
- `HomeTest Operating Model - Plan Detail.bak_pre_transcript_update_20260709_144755.html`
- `HomeTest Operating Model - Plan Detail.bak_pre_itt_move_20260710_122912.html`
- `HomeTest Operating Model - Plan Detail.bak_pre_deepdive_20260710_124018.html`
- `HomeTest Operating Model - Plan Detail.bak_pre_priority_20260710_125732.html`
- `HomeTest Operating Model - Plan Detail.bak_pre_workshop_rebuild_20260710_133145.html`
- `HomeTest Operating Model - Plan Detail.bak_pre_swap_*.html`
- `HomeTest Operating Model - Plan Detail.bak_pre_cleanup_20260711_084356.html` (last clean snapshot before source/owner cleanups)

### Structure of Plan Detail as it stands

Reading top to bottom:

1. **Title banner** with programme name and file title.
2. **Deliverables mapped to the plan** paragraph block (the "v6 workbook" paragraph has been removed; only the intro text and the two-caveat callout remain).
3. **Workshop strip** — a compact panel with a "View full workshop programme →" button linking to the Workshop Plan page. Sits directly under the deliverables section and above the value scenario filter.
4. **Route toggle** (Both routes / Plan A only / Plan C only) and **Value scenario filter** (~£30m NHSE + DHSC 12 months vs £250m+ CO + HMT 16 months).
5. **Filter bar** for critical path only / commercial only / dependencies only.
6. **Six Cornerstones callout** — the six cornerstone tiles, each with a "Fed by:" sub-line showing which activities feed them. Cornerstones are: 1 ITT specification, 2 Volume and value, 3 Commercial models, 4 Interim route (Plan C), 5 Framework administration, 6 Go-live date.
7. **Roadmap** section with legend at top (Critical path · Commercial-led · Dependency-led · Procurement process step), phase-by-phase dot tracks for Plan A and Plan C. Dots in S1 and S2 are grouped into visual dotted boxes. Each dot deep-links to its matrix activity.
8. **Matrix** — five columns S1 to S5, activities inside as expandable `<details>` cards. S1 has six groups (Cornerstones · Framework administration · Sourcing strategy · Programme inputs · Workshops and engagement · ITT specification). S2 has four groups (Approvals · Assurance and legal · Watch · Adoption). S3, S4, S5 are single-lane chronological (no groups) because they are process-sequential.
9. **Plan C — Commissioner-led interim, full detail** — the S1-S5 breakdown for the Plan C track.

### Structure of Workshop Plan as it stands

1. **Hero** with title, back-link to Plan Detail.
2. **Core group panel** — the anchor group who attend every workshop.
3. **Value scenario filter** — All workshops / Low scenario / High scenario. Three buttons in a shared flex container so they stay on one line.
4. **Timeline strip** — S1 to S5 tiles, clickable, jump to that stage section.
5. **Stage sections** S1 through S5, each with its workshop cards inside as `<details>` accordions.
6. **Standing meetings** section (Commercial team standup, weekly).

### The 15 workshops as currently placed

- **S1 (Jul–Oct 26):** Cornerstones foundation (23 Jul, full day), Volume and value (w/c 27 Jul, 2hr), Commercial models (w/c 27 Jul, 2hr), Framework administration decision (w/c 3 Aug, 2hr), Interim route Plan C design (w/c 3 Aug, 2hr), ITT specification kickoff (w/c 17 Aug, half day).
- **S2 (Nov–Dec 26):** Approvals stack sequencing (early Nov, half day), IG and clinical safety deep-dive (mid Nov, 2hr), Evaluation criteria calibration (late Nov, 2hr).
- **S3 (Jan–Feb 27):** Supplier briefing preparation (early Jan, 2hr), Evaluation panel constitution (late Jan, 2hr).
- **S4 (Feb–Jun 27):** Evaluation calibration workshop (post-panel, half day), Award moderation and standstill readiness (pre-award, 2hr).
- **S5 (Jun–Aug 27):** Mobilisation planning (post-signature, half day), Measurement framework stand-up (steady-state prep, 2hr).

### Scenario tagging on workshops

Each workshop carries a scenario badge:

- **Decides the scenario** (2): Cornerstones foundation, Volume and value. Both carry a blue note explaining the answers here dictate the downstream approvals path.
- **Content shifts by scenario** (3): Commercial models (pricing ceilings), Framework administration decision (route viability under 12-month window), Approvals stack sequencing (NHSE + DHSC only under low, full CO + HMT under high).
- **Both scenarios** (10): everything else.

### Attendees model

Core group appears on every workshop card. Additional specialists appear in a "Plus for this session" panel per workshop. As at 13 Jul the core group is:

Martin O'Neill · Rachel Flower · Chris Leary · Richard Samuel · Shirley Gaynor-Ward · James Cowley · Simone Bilton · Scott Eason · Matt Thomas · Matt Visser.

Mandie Holt has been moved OUT of the core group and now appears as "Mandie Holt (optional)" in every workshop's "Plus for this session" panel (15 instances).

Specialist attendees per workshop (only those that survived the two rounds of pruning):

- Cornerstones foundation → Simon Leigh · Meera Parkash · Wendi Higgins · Will Twells
- Volume and value → Simon Leigh
- Commercial models → Simon Leigh
- ITT specification kickoff → Meera Parkash · Wendi Higgins · Will Twells
- IG and clinical safety deep-dive → Meera Parkash · Wendi Higgins
- Supplier briefing preparation → Annie Wakefield
- Evaluation calibration → Evaluation panel
- Award moderation and standstill readiness → Evaluation panel
- Mobilisation planning → Will Twells · Awarded suppliers
- Measurement framework stand-up → Will Twells · Data lead (TBC)

Five workshops carry only the Core group plus Mandie: Framework administration decision, Interim route Plan C, Approvals stack, Evaluation criteria calibration, Panel constitution.

## 4. The thinking

### Why two pages, not one

The milestone plan is dense. Workshops are dense. Cramming both into one page produced a scroll of doom that hid detail. Splitting workshops onto their own page let each artefact breathe and let the workshop programme develop its own filters (scenario dependency) that don't belong on the milestone plan. The workshop strip at the top of Plan Detail links the two so nobody misses the workshop content.

### Why cornerstones first, then roadmap, then matrix, then Plan C detail

Editorial sequence. Cornerstones state what we are solving for. Roadmap shows when. Matrix shows what. Plan C detail shows the interim track. Anything else out of that order confused readers on the 9 July walk-through.

### Why chronological numbering was rejected

Tried once (10 Jul). Scott's reaction: numbers looked random because activities in the roadmap dots are grouped by pot (Cornerstones, Sourcing strategy, etc), and numbering them chronologically inside those groupings did more harm than good. Removed all badges. Do not reintroduce sequence numbers without checking with Scott first.

### Why S1 and S2 have group boxes but S3, S4, S5 don't

S1 and S2 contain parallel workstreams that make sense to visually group by topic (Cornerstones vs Sourcing strategy vs ITT). S3, S4, S5 are single-lane chronological process stages — publish, brief, receive bids, evaluate, moderate, award, mobilise. Grouping them would misrepresent the natural sequence. Scott specifically endorsed leaving S3, S4, S5 flat and chronological (10 Jul).

### Why value scenario is a filter rather than two separate plans

The two scenarios share the same procurement backbone. Most workshops and most activities apply either way. Only three workshops change materially by scenario (Commercial models, Framework administration decision, Approvals stack sequencing) and no activity is completely absent under low. A filter makes the shared structure visible and the branch points explicit, which is closer to reality than two disjoint pages.

### Why the six cornerstones replaced the "Cardinal Four"

James Cowley's language on 9 July. Cardinal Four was the previous framing (volumes, clinical proportion, lotting, buyer identification). Six Cornerstones adds ITT specification, commercial models, interim route (Plan C), framework administration, go-live date. Broader because it now spans the full sourcing strategy not just the value-driving questions. The four cornerstones from Cardinal Four are still visible inside CS2 (Volume and value) — they feed it.

### Why Scott's title changed from Commercial Lead to Commercial Operations to Future State Team

Iterative feedback. Commercial Lead is Rachel Flower's title. Scott's is Commercial Operations. But Rachel + Scott + James Cowley act together as the Future State Team, so ownership labels default to that team designation rather than any individual title. Applied across the Plan Detail on 11 July.

### Why no source citations, no owner names by individual, no employer references

Standing rules from Scott's feedback across the last two months. External-facing artefacts (this one included) show functional descriptors only. Named individuals or supplier/contractor labels (like "Servita" for Annie Wakefield) get stripped. This is why owner labels use "Commercial Operations", "IG Lead", "Clinical Safety Lead" rather than Scott Eason, Wendi Higgins, Meera Parkash. It is also why source citations were removed from the Plan Detail on 11 July.

### Why Mandie Holt is optional not core

Mandie is Mandie Holt (spelled with 'ie'). She is James Cowley's boss in NHSE Commercial. Scott's judgement (13 Jul): keeping her in the core group makes every workshop look mandatory for her, which is not the working reality. Moving her to optional-per-workshop reflects the actual attendance pattern where she attends selectively.

## 5. Live strategy / plan

James Cowley has provided feedback on both files. That feedback is the driver for the next round of changes. Scott is handing this off to Fable 5 so it can apply the feedback methodically without losing the structure that has been built.

The Fable 5 chat should:

1. Read this state file and the FABLE5-INSTRUCTIONS.md in the same folder before touching anything.
2. Read the current live copies of both HTML files to establish baseline.
3. Take Scott's paste of James's feedback and process it item-by-item.
4. For each feedback item, make the change carefully with tag-balance verification, save both live and root copies, and confirm with Scott before moving on to the next contentious item.
5. Push to GitHub Pages once Scott confirms the batch is ready to deploy.

Do not batch a full set of changes silently. James's feedback likely spans structural, wording and attendee-list edits. Some will be trivial. Others may reopen decisions (e.g. cornerstone framing, workshop count, role labels). Every non-trivial edit should go past Scott before it lands.

## 6. Working files offloaded

Not needed. Both live files are already on Scott's own drive under `NHS Commercial Model/Operating Model/HomeTest-TOM/`. Backups from every editing session sit alongside them in the same folder. The GitHub repo `ScottEason1967/HomeTest-TOM` on `main` is the deploy source.

## 7. Factual additions for merge into SKILL.md

The following facts were established this week that belong in the broader HomeTest / DTx OM matter skill on next refresh (not in this state file):

- Mandie Holt spelling: with `ie`, not `y`. Wendi Higgins spelling: with `i`, not `y`. Will Twells (not Twelves). Martin O'Neill (double L) per KB primary source, though Scott sometimes uses O'Neil.
- Simone Bilton is now Product Owner Pathway 2 (moved from HIV HomeTest PO, handed to Jamie). She sits in the Future State Team's meeting orbit.
- Simon Leigh confirmed as Health Economist, engaged from 9 June 2026 at 2.5 days/week, priority list PSA → COPD → standard model.
- Future State Team = Rachel Flower + Scott Eason + James Cowley as the collective ownership label for commercial workstream activities.
- Value scenarios split at ~£30m (NHSE + DHSC only, 12 months) vs £250m+ (Cabinet Office + HMT, 16 months).

## 8. Hazards and things not to repeat

**Naming.** Do not silently correct KB-verified names to what you think is right. Scott has explicitly overridden the KB on some spellings (Wendi vs Wendy — Scott confirmed Wendi with i). If a name looks wrong, ask Scott before changing it.

**Sources and attributions.** Never cite Scott's meeting transcripts as a source in any output. Never name suppliers, contractors or employers next to individual names in the artefacts. Never attribute facts to specific people's emails or instructions in the pages themselves — state the facts.

**Individual names in the artefacts.** Owner labels are functional descriptors (Future State Team, NHSE Commercial, IG Lead, Sponsor). Individual names only appear in the Workshop Plan attendee lists because those are working documents for the workshop programme itself. Do not sprinkle individual names into the Plan Detail.

**Tag balance.** Both HTML files sit at a baseline `div` imbalance of `-2` (a pre-existing quirk from an early backup that the browser tolerates). Every edit must preserve that exact baseline. If you finish a session with a different balance, the file will render blank in some browsers. Compute `text.count('<div') - text.count('</div>')` before and after every edit and refuse to save if it moved.

**Backup before atomic operations.** Any operation that reshuffles or extracts multiple `<details>` blocks must write a backup first. Naming convention: `HomeTest Operating Model - Plan Detail.bak_pre_<label>_YYYYMMDD_HHMMSS.html`. This has already saved the file three times.

**Do not regex across nested tags without depth-aware walks.** Nested `<div>` structures inside `<details>` blocks have broken every regex-only approach. Use depth-based matching (find opening tag, walk to matching close counting nesting) for anything that touches structure.

**Do not re-add features Scott has explicitly asked to remove.** These include:
- Chronological sequence badges on activities
- Individual names or employer labels in workshops or Plan Detail owners
- Source citations
- The "v6 mapping workbook" paragraph
- "Operating Model Owner" as an owner label

**Deploy step is separate.** Editing the live copy does not deploy it. Scott's git working directory is his Windows drive; you need to prompt him to run `git add`, `git commit`, `git push` (or offer to draft the commands) when he confirms a batch is ready. Do not attempt to invoke git yourself.

## 9. Open decisions / pending

1. Apply James Cowley's feedback on both Plan Detail and Workshop Plan. Owner: Fable 5 chat. Needs: Scott to paste the feedback into the new chat. Status: awaited.
2. Confirm the "Data lead (TBC)" specialist on the S5 Measurement framework workshop. Owner: Scott. Needs: identity/role confirmation.
3. Decide whether "HomeTest Principal Delivery Manager" (Matt Thomas's title, one instance) should stay as-is or fold into a standard label. Owner: Scott.
4. Decide fate of remaining non-standard role labels on Plan Detail: Commercial Finance, Service Lead, Clinical Safety Group, DPO, NHSE Pricing. Owner: Scott.
5. Task 40 open on the wider tracker: add a dependencies column to the deliverables spreadsheet and push offloadable items to programme.
6. Task 42 in progress: review Preventx and SH:24 supplier cost breakdown emails re the clinical >50% question.

## 10. Communication style and working preferences

- UK English throughout.
- No em-dashes in body text of outputs.
- Sentence length varied, not uniform.
- No stock corporate softeners.
- No three-point summary structures where a paragraph would do.
- Be specific and anchor to files, dates, numbers.
- Challenge weak logic and optimistic assumptions directly. Do not agree for the sake of it.
- Do not narrate progress in the middle of a task. Do the work, then report succinctly.
- When Scott asks a question about a decision, answer with a view before implementing.
- Backup before destructive operations; verify tag balance after every HTML edit.
- Never disclose Claude's involvement in any document, metadata or trace.

## 11. How to use this file

Read this file first. Then read `FABLE5-INSTRUCTIONS.md` in the same folder for the operating rules for the incoming Fable 5 chat. Then read the two live HTML files at their paths above to establish baseline before you touch anything.

Take James Cowley's feedback from Scott. Work through it item-by-item. For each item, propose the change first if it is anything more than a spelling or a bullet reword. Save. Verify. Move on.

When the batch is done, prompt Scott to deploy via git push and confirm the live URLs render correctly.
