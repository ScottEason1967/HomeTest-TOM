# Joe&apos;s Journey: Gemini illustration brief

Six stage illustrations for the HomeTest Operating Model &mdash; Joe Journey page. Filenames already wired into the page&apos;s `stage-image` slots, so the generated files just need to drop into `Assets/JoeJourney/`.

## House style (apply to every prompt)

A consistent visual style is non-negotiable across the six stages. Lead every prompt with this block, then add the scene-specific detail.

> **Style:** clean, modern, lightly stylised editorial illustration in the style of a flat-but-warm corporate annual report. Soft, slightly grainy texture. Restrained palette anchored on NHS-blue `#005EB8` and a deep navy `#003087`, with warm cream `#FFF9EC`, muted gold `#FFB91D`, and a single fresh green accent `#5BC093` for objects of progress. Characters drawn with calm, professional confidence &mdash; not cartoonish, not photoreal. Faces expressive but composed. Wide aspect ratio (3:2 landscape) suitable for an inline page panel. No text, no logos, no NHS marque, no branded UI. No watermarks, no signatures.

> **Character continuity (Joe):** mid-thirties, mixed-heritage, neatly trimmed beard, wire-frame glasses, dark navy zip-neck pullover over a plain white t-shirt, smart casual. Approachable, focused, slightly weary in the early stages, increasingly assured as the story progresses. Same Joe in every illustration &mdash; this is the same person across six scenes.

> **Setting:** the early stages are in a working office (Joe&apos;s business). Not corporate-glossy, not start-up-scrappy &mdash; somewhere between. Small team. Light from a window on one side. Plants. Whiteboard. A printer in the background somewhere. No NHS visual identity in his office.

> **No screens that contain readable copy.** Where a screen appears, the content is suggested through layout shapes and colour blocks &mdash; never spelt out in text.

> **Avoid:** stock-photo poses, exaggerated smiles, thumbs-up clich&eacute;s in the body of an image (one moment of celebration in stage 4 only), cluttered backgrounds, gradients with too much saturation, hands holding nothing.

---

## Stage 1 &mdash; Find the framework

**Scene:** Joe at his desk in his small office, laptop open in front of him. He is reading. Calm concentration. His expression: this is the first time he has seen an NHS procurement pack that did not feel like a closed door. The screen shows abstract shapes suggesting a published criteria pack &mdash; a header band, then a 7-card grid of design principles (don&apos;t spell anything out). On his desk: a notebook, a single coffee mug, a pen. Through the window behind him, a glimpse of a city street &mdash; soft, out of focus. Time of day: late afternoon, warm light. One small plant on the desk. No one else in frame.

**Tone:** discovery. The supplier-side equivalent of finding a door that opens.

**Filename:** `joe-s1-find-the-framework.png`

---

## Stage 2 &mdash; Self-assess

**Scene:** Joe at a small meeting-room table inside his office, working with his clinical safety officer (a woman in her forties, glasses, mid-tone skin, dark hair tied back, wearing a soft cardigan over a plain blouse). The two of them are mid-discussion. The printed criteria pack is on the table between them &mdash; pages and pages, marked up with sticky tabs. A laptop sits to one side, screen suggesting a checklist grid (no readable text). Two coffee cups, half-finished. A pen is in Joe&apos;s hand, hovering over a page. Both look focused, neither tense &mdash; this is a working session that is going well. The whiteboard behind them carries abstract shapes representing the five criteria dimensions.

**Tone:** competent self-assessment. They know what they are doing.

**Filename:** `joe-s2-self-assess.png`

---

## Stage 3 &mdash; Submit the EOI

**Scene:** Close-up over Joe&apos;s shoulder at his desk. His finger or cursor is poised over a submit button on the laptop screen. The screen suggests an EOI submission form &mdash; upload tiles representing evidence files, a sidebar suggesting form sections, a primary action button highlighted in the muted gold `#FFB91D`. Around the laptop: a small stack of bound documents on the desk (the evidence pack), a coffee mug, his glasses folded next to the keyboard. The lighting is focused on the screen and his hand; the wider office sits in soft, slightly out-of-focus warmth behind. Joe&apos;s face is in three-quarter profile, calm, committed. A second browser tab visible on the screen in shadow suggests the published criteria pack still open behind the form.

**Tone:** decisive. The point of commitment.

**Filename:** `joe-s3-submit-the-eoi.png`

---

## Stage 4 &mdash; Through the gate

**Scene:** Joe at his desk reading the conformance certificate on screen. The certificate is suggested by a centred document shape in fresh green `#5BC093` and gold `#FFB91D`, with a seal-like circular flourish in the upper right corner of the document &mdash; no readable text. His expression: relief and quiet pride, the kind of smile that follows a long-held breath out. In the doorway behind him: his clinical safety officer (from stage 2) and his data protection officer (a man in his late forties, lighter skin, short greying hair, casual shirt) &mdash; both have stopped on their way past, one giving a small thumbs up, the other smiling. This is the only moment of celebration in the six-stage set; keep it understated.

**Tone:** unlock. Earned.

**Filename:** `joe-s4-through-the-gate.png`

---

## Stage 5 &mdash; First commissioner calls off

**Scene:** A wide laptop-screen view of a video call between Joe (left tile, recognisably the same Joe in the same office) and a Local Authority commissioner on the other tile (right tile: a Black woman in her late thirties, professional appearance, lanyard visible, in front of a soft public-sector backdrop &mdash; civic building light, no logos). Between the two tiles, a shared document is visible on screen &mdash; a call-off contract suggested by the document shape, with two signature blocks at the foot. Both people are relaxed, mid-conversation. The body language between them is collaborative &mdash; neither is the gatekeeper. Soft afternoon light. A wall clock just visible in Joe&apos;s tile reads a working hour.

**Tone:** partnership. The conversation is about deployment dates, not whether he should be allowed.

**Filename:** `joe-s5-first-commissioner.png`

---

## Stage 6 &mdash; Reuse across the cohort

**Scene:** Joe at his desk looking at a dashboard map of England on a wide monitor. The map shows multiple deployment markers in different colours &mdash; clusters of NHS-blue dots for one type of commissioner, fresh-green dots for another, muted gold for a third &mdash; scattered across the country, with concentration around the major urban areas. In the top-right corner of the screen, a small certificate icon (same fresh-green tone as stage 4). In the bottom corner of the screen, a supplier badge shape. Joe&apos;s expression: settled, slightly amazed, recognising the scale of what has just become possible. His clinical safety officer is at her own desk in the background, quietly working. Late-day light. The office feels lived-in: a few coffee cups, a printer running.

**Tone:** scale. The same business, eighteen months on. One certificate, many deployments.

**Filename:** `joe-s6-reuse-across-cohort.png`

---

## Production notes

Generate at 3:2 landscape. Target 1800 x 1200 minimum so the inline page panel does not blur on retina. Export as PNG with a transparent or warm-cream `#FFF9EC` background.

If the generator struggles with character continuity across the six stages, lock the look on stage 1 first, then reference that frame explicitly in stages 2-6 (&ldquo;same Joe as the first illustration, same office&rdquo;). The clinical safety officer in stage 2 should also recur in stages 4 and 6.

After generation, drop the six files into `Assets/JoeJourney/` and update the six `stage-image` blocks on `HomeTest Operating Model - Joe Journey.html` from the placeholder pattern to a regular `<img>` tag with the matching filename.
