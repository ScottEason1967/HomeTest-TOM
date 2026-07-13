# Fable 5 — Instruction pack for updating HomeTest Milestone Plan and Workshop Plan

Read this pack in full before making any edit. Do not skim. The rules below exist because the two files have been broken more than once by well-meaning edits that skipped a check.

## What you are working on

Two live HTML pages that run the HomeTest procurement plan for NHSE. Both are hand-maintained HTML with inline CSS and JavaScript. Both sit behind a sessionStorage auth gate. Both deploy via GitHub Pages from the repo `ScottEason1967/HomeTest-TOM`.

**Live artefacts (edit these):**
- `C:\Users\scott\Documents\Claude\NHS\NHS Commercial Model\Operating Model\HomeTest-TOM\HomeTest Operating Model - Plan Detail.html`
- `C:\Users\scott\Documents\Claude\NHS\NHS Commercial Model\Operating Model\HomeTest-TOM\HomeTest Operating Model - Workshop Plan.html`

**Local viewing copies (auth stripped; must be kept in sync with the live copies):**
- `C:\Users\scott\Documents\Claude\NHS\NHS Commercial Model\HomeTest Plan.html`
- `C:\Users\scott\Documents\Claude\NHS\NHS Commercial Model\HomeTest Workshop Plan.html`

Every save to a live file must also save an auth-stripped copy to the root local viewing file. The regex to strip auth is:

```python
import re
root_html = re.sub(
    r'<script>\s*\(function\(\)\{\s*if\s*\(sessionStorage\.getItem\(.hometest-auth.\)[^<]+\}\s*\}\)\(\);\s*</script>',
    '',
    live_html,
    flags=re.DOTALL,
)
```

**Deployed URLs:**
- Plan Detail: `https://scotteason1967.github.io/HomeTest-TOM/HomeTest%20Operating%20Model%20-%20Plan%20Detail.html`
- Workshop Plan: `https://scotteason1967.github.io/HomeTest-TOM/HomeTest%20Operating%20Model%20-%20Workshop%20Plan.html`

Auth code: `hometest2026`.

## The task

Scott is going to paste James Cowley's feedback into your chat. James is one of the three people in the Future State Team (with Rachel Flower and Scott). His feedback covers both the milestone plan and the workshop programme.

Your job: apply his feedback methodically, one item at a time, verifying each edit and confirming with Scott before moving on to the next non-trivial change.

You must not:
- Batch all changes silently.
- Rewrite anything not touched by the feedback.
- Reintroduce anything Scott has removed (list below).
- Push to git yourself.

## Read the MATTER-STATE first

`MATTER-STATE-260713.md` sits in this same folder. It captures the full state of both files, the thinking behind the current structure, and the rules Scott operates under. Read it before you read James's feedback. If any of his feedback conflicts with a standing rule in the state file, flag it to Scott before you apply it.

## Standing rules that never break

1. **UK English throughout.** No em-dashes in body text.
2. **No source citations** on the Plan Detail. James's feedback may reference source docs — do not add those references to the page.
3. **No individual names in the Plan Detail** — owner labels are functional descriptors (Future State Team, NHSE Commercial, IG Lead, Sponsor, Clinical Safety Lead, Product Manager, Head of Technology & Product, Partnerships, Health Economist, NHSE Legal, NHSE Strategic Finance, SLT). Adding a person's name to an owner cell is an error.
4. **Individual names ARE allowed in the Workshop Plan attendee lists** — that page is a working document for the workshop programme itself. Names appear in Core group and "Plus for this session" panels only.
5. **No employer or contractor labels next to individual names.** Annie Wakefield is "Annie Wakefield", not "Annie Wakefield (Servita)".
6. **No sequence numbers on activity dots or cards.** Scott removed all 90 badges on 10 July. Do not reintroduce them.
7. **No references to "Operating Model Owner" as an owner label.** Replaced with Future State Team on Plan Detail. Do not put it back.
8. **Never cite Scott's meeting transcripts as a source in any output.**
9. **Never disclose Claude / AI involvement.** All work attributed to Scott.
10. **Never disclose internal file paths in any output the user might share.**

## The standard role vocabulary on Plan Detail

Use only these functional descriptors in owner labels. Any variant must be normalised.

- Future State Team (= Rachel Flower + Scott Eason + James Cowley)
- NHSE Commercial (= James Cowley + Mandie Holt)
- IG Lead (= Wendi Higgins)
- Clinical Safety Lead (= Meera Parkash)
- Sponsor (senior sponsor; replaces both SRO and Deputy Director DTx)
- Product Manager (person not yet named)
- Head of Technology & Product (= Matt Visser)
- Partnerships
- Health Economist (= Simon Leigh)
- NHSE Legal
- NHSE Strategic Finance
- SLT

Retained specialist / distinct labels that are not in the standard set but are legitimate:
- HomeTest Principal Delivery Manager (= Matt Thomas)
- Commercial Finance
- Service Lead
- Clinical Safety Group
- DPO
- NHSE Pricing
- Adoption (workstream, not role)
- Evaluation Panel, MHRA, Admitted Suppliers, independent deployer-side CSO — external references

If James's feedback introduces a new owner label, decide if it maps to the standard set. If it doesn't, ask Scott whether to add it as a new standard or a one-off.

## The core group and specialist attendees on Workshop Plan

Core group who attend every workshop (as at 13 Jul):

Martin O'Neill · Rachel Flower · Chris Leary · Richard Samuel · Shirley Gaynor-Ward · James Cowley · Simone Bilton · Scott Eason · Matt Thomas · Matt Visser

Mandie Holt is OPTIONAL and appears in every workshop's "Plus for this session" panel as `Mandie Holt (optional)`. Do not put her back in the core group.

Name spellings — canonical:
- Mandie Holt (with `ie`)
- Wendi Higgins (with `i`)
- Will Twells (not Twelves)
- Martin O'Neill (double L)
- Simone Bilton
- Meera Parkash
- Simon Leigh
- Annie Wakefield

If James's feedback spells a name differently, ask Scott before you change it. Some KB spellings conflict with Scott's preferred spellings.

## HTML editing constraints

Both files have a **pre-existing `div` balance of `-2` for Plan Detail** and **`0` for Workshop Plan** as at 13 July 2026. Every edit must preserve that exact baseline.

Before saving after any edit:

```python
d = text.count('<div') - text.count('</div>')
dt = text.count('<details') - text.count('</details>')
# Plan Detail: assert d == -2
# Workshop Plan: assert d == 0
# Both: assert dt == 0
```

If the balance moves, refuse to save. Restore from the most recent backup and try a different approach.

**Backup before any structural edit.** Naming convention:
```
HomeTest Operating Model - Plan Detail.bak_pre_<label>_YYYYMMDD_HHMMSS.html
HomeTest Operating Model - Workshop Plan.bak_pre_<label>_YYYYMMDD_HHMMSS.html
```

**Do not use plain regex for anything that spans multiple `<details>` blocks or that reorders elements.** Nested `<div>` structures inside `<details>` have broken every regex-only approach. Use depth-based matching:

```python
def find_close(s, after_open_pos):
    pos = after_open_pos
    depth = 1
    while depth > 0 and pos < len(s):
        mo = s.find('<div', pos)
        mc = s.find('</div>', pos)
        if mc < 0:
            return -1
        if 0 <= mo < mc:
            depth += 1
            pos = mo + 4
        else:
            depth -= 1
            if depth == 0:
                return mc
            pos = mc + 6
    return -1
```

## Process for each feedback item

1. **Read the item.** Restate it back in one sentence to check you understand.
2. **Classify it:** trivial (typo, single word change) or substantive (restructure, new element, deletion of existing).
3. **For trivial items** — apply, verify tag balance, save live and root copies, move on.
4. **For substantive items** — propose the change to Scott before applying. Include the diff or the before/after view. Wait for confirmation.
5. **Verify** — read a small region of the file where the change happened to confirm it landed as intended.
6. **Log** — keep a running list of what has been done so Scott can see progress.

## Deploying to GitHub Pages

When a batch is done and Scott confirms:

1. Ask Scott to open his terminal at `C:\Users\scott\Documents\Claude\NHS\NHS Commercial Model\Operating Model\HomeTest-TOM\`.
2. Provide the git commands:
   ```bash
   git add "HomeTest Operating Model - Plan Detail.html" "HomeTest Operating Model - Workshop Plan.html"
   git commit -m "Apply James Cowley feedback batch <N>"
   git push
   ```
3. Wait 1–2 minutes for GitHub Pages to rebuild.
4. Ask Scott to open both deployed URLs in an incognito window to confirm they render correctly.

Do not invoke git yourself. You do not have credentials and the working tree lives on Scott's machine.

## Rendering checks after any structural edit

If you have reshuffled `<details>` blocks, reordered group boxes, moved sections or restructured containers, run these post-edit checks:

1. Tag balance (see above).
2. File ends with `</html>` (no null-byte tail truncation).
3. The number of `<details class="activity"` blocks matches what it should be (24 in S1 as at 13 Jul, 9 in S2, 4 in S3, 5 in S4, 5 in S5).
4. Every activity `id` is unique — `re.findall(r'id="a-S\d+-\d+"', text)` should have no duplicates.
5. The tooltip CSS rule `.stage:nth-child(n+3) .why-tooltip{left:auto;right:calc(100% + 6px);}` is still there — this fix prevents CP tooltips from being clipped in the right-hand matrix columns.
6. The `.stage{overflow:visible;}` override is still there — this is what lets tooltips escape the column edge.

## What you do NOT touch unless James's feedback explicitly asks

- The auth gate script.
- The value scenario filter logic.
- The route toggle (Plan A / Plan C).
- The Plan C detail section structure.
- The Status page deep-linking pattern.
- The GitHub Pages deploy pattern.
- Anything in `NHS Commercial Model/Digital Therapeutics Operating Model/` — that is the broader DTx OM matter and has its own skill.

## If James's feedback contradicts the standing rules

Flag it to Scott before applying. Do not silently apply a change that breaks a rule. Example: if James says "put source references back in", tell Scott before doing it — the rule against source references is his standing preference.

## When you are done

Report to Scott succinctly:
1. Which feedback items you applied.
2. Any items you flagged and why.
3. Confirmation both files pass the tag-balance and render checks.
4. That both files are saved to live and root copies.
5. Prompt Scott to deploy.

No celebration. No summary of what a good job was done. Just the punch list.
