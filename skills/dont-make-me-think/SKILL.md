---
name: dont-make-me-think
description: "Apply Steve Krug's \"Don't Make Me Think\" usability principles to web and mobile interfaces — reducing cognitive load, removing needless choices, making pages self-evident, designing for scanning, fixing confusing navigation, and cutting clutter. Use this skill whenever the user is building OR reviewing any UI — including dense app UIs like dashboards, settings panels, multi-section forms, and wizards — and cares about clarity, simplicity, or ease of use: when a screen is \"confusing\" or \"overwhelming,\" has too many options/fields/steps, users \"can't figure out what to do\" or \"can't find\" something, controls are redundant or ambiguous, copy is bloated, navigation is unclear, or someone asks for a usability/UX review, a \"Krug-style\" critique, or wants an interface that's simpler and more self-explanatory. This is about whether users can effortlessly understand and use the interface (cognitive load, number of decisions, wording, scannability, conventions) — reach for it even when the user only says \"make this clearer,\" \"simplify this,\" \"this feels clunky,\" \"too much going on,\" \"improve the UX,\" or \"audit this flow,\" not just when they name the book."
metadata:
  category: design
---

# Don't Make Me Think — Usability Guidance

This skill operationalizes Steve Krug's *Don't Make Me Think* (and the *Revisited*
edition's mobile chapter) into guidance for building and reviewing interfaces.

It is **not** an aesthetics or visual-polish skill. It is about **usability**: can a
real person, glancing at this screen while distracted, instantly understand what it is,
what they can do, and how to do it — without stopping to think? When the work is about
visual taste, animation, or "make it beautiful," prefer a design/polish skill instead.
When it's about whether people can *figure the thing out*, this is the right tool.

It applies just as much to dense application UIs — dashboards, settings panels,
multi-section forms, wizards, checkout flows — as it does to marketing pages. In fact the
heaviest cognitive load usually lives in those dense screens, and the most valuable
Krug-style move there is often **simplification: having less on the screen**, not just
phrasing what's there more clearly.

## The one idea everything hangs on

> **Krug's First Law: "Don't make me think."**

Every time a user has to pause and puzzle over something — *Where am I? Where do I
start? Is that clickable? What does this label mean? Where did they put that?* — you've
spent a little of their attention and goodwill. These "question marks over the head" add
up. The job is to remove them so using the thing feels effortless and obvious.

A page exists on a ladder:

1. **Self-evident** (the goal) — obvious at a glance, zero thought required.
2. **Self-explanatory** (acceptable) — takes a moment, but the page itself answers the
   question; no outside help needed.
3. **Requires explanation** (failure) — the user needs a tooltip, a help doc, or a
   guess. Treat this as a bug.

When you build or review, push everything up this ladder.

## How people *actually* use interfaces (design around these, not against them)

Krug's three facts of life. Most usability problems come from designing for an
imaginary, patient, attentive user who does not exist.

1. **People scan, they don't read.** Users blast through pages looking for something
   that matches their goal or that's vaguely interesting. They don't read your carefully
   crafted prose. → Design for scanning: headings, short chunks, visual hierarchy, key
   words that pop.
2. **People satisfice — they don't seek the optimal choice.** They click the first
   reasonable option, not the best one. Weighing alternatives is more work than just
   trying one and backing up. → Make the first plausible thing they'll see be a good
   choice, and make going back cheap.
3. **People muddle through.** They rarely figure out how things are *intended* to work;
   they form a rough, often wrong, mental model and keep using it as long as it works. →
   Don't rely on users "getting it." Make the right path the obvious path.

## Core principles for *building* UI

Apply these as you write components, pages, and copy. Each is a way to remove a question
mark.

- **Use conventions; don't reinvent.** People know what a logo top-left, a cart icon
  top-right, underlined links, and a magnifying-glass search box mean. Conventions are
  cognitive shortcuts users already paid for. Innovate on your product's value, not on
  where the nav lives. If you must break a convention, the alternative has to be *so*
  clear it needs no learning.
- **Create a clear visual hierarchy.** More important = more prominent (bigger/bolder/
  more color/more whitespace). Related things are grouped visually. Things are "nested"
  to show what's part of what. A good hierarchy pre-processes the page so users don't
  have to.
- **Break the page into clearly defined areas.** Users decide fast which areas to focus
  on and which to ignore. Distinct regions (nav, main content, sidebar, actions) let them
  skip what's irrelevant to their goal.
- **Make it obvious what's clickable (and tappable).** Clickability should be
  unmistakable from shape, color, and placement — never something users have to test by
  hovering or guessing. Ambiguous "is this a button or just text?" is pure friction.
- **Minimize noise.** Visual clutter, competing demands for attention, and busy
  backgrounds all raise cognitive load. Every element fighting for attention makes the
  important things harder to find.
- **Format text for scanning, not reading.** Plenty of headings that describe content,
  short paragraphs, bulleted lists, and **highlighted key terms**. One idea per
  paragraph. The heading structure should let someone understand the page from headings
  alone.
- **Omit needless words — and needless choices.** Krug: "Get rid of half the words on each
  page, then get rid of half of what's left." Cut happy talk ("Welcome to our website!
  We're so glad you're here") and obvious instructions. Then apply the same knife to
  *controls*: every field, toggle, option, and step is a decision the user has to process,
  and decisions are heavier than words. On a dense form or settings screen, the
  highest-leverage simplification is almost always to **have fewer things on the screen** —
  for each control ask: can it be **removed**, given a sensible **default**, **derived**
  from something else, or **deferred** behind progressive disclosure? Fewer, clearer
  decisions beat more, finer-grained ones.
- **Hunt for redundant and overlapping controls.** When two controls appear to set the
  same thing (e.g. a set of radio buttons *and* a dropdown that both decide "when ordering
  stops"), the user is left thinking "which one wins?" — a pure question mark, and a common
  one in app UIs that grew feature by feature. Collapse them into a single source of truth.
  A control duplicated across a "simple" view and an "Advanced" section is the same bug.
- **Default the common case; defer the rare one.** Pick smart defaults so a typical user
  can accept the screen as-is and only touch what's unusual for them. Push rarely-needed
  options behind progressive disclosure (an "Advanced" section that's *collapsed by
  default* and doesn't duplicate anything already shown). The goal is that the screen looks
  simple to the 90% and is still complete for the 10%.
- **Make clicks mindless.** It's not about *minimizing the number* of clicks — it's that
  each click should be an unambiguous, no-thought choice. Three obvious clicks beat one
  click the user has to deliberate over. Don't agonize over click counts; agonize over
  click *difficulty*.
- **Label things in the user's words.** Buttons and links should say what will happen in
  language the user already uses ("Download", "Add to cart"), not internal jargon or cute
  names ("Get the goods!"). A link's text should match the title of the page it leads to.

## Two workflows

Figure out which the user needs (it's often both), then follow the matching reference.

### Building or improving UI
Keep the core principles above in working memory as you write. For depth on navigation
design, home pages, forms, and the full scanning toolkit, read
`references/building-checklist.md`. For anything touch/responsive/small-screen, read
`references/mobile-usability.md`.

### Reviewing / auditing UI
When asked to review, critique, or "make this clearer," produce a structured usability
audit rather than scattered notes. Read `references/audit-report.md` for the workflow
(including the lightweight "self-evidence test" you can run on any screen) and the exact
report format. Pull in `references/mobile-usability.md` if mobile/responsive is in scope.

## The cheapest usability test (recommend it freely)

Krug's most practical message: you can't make something usable by reasoning alone —
**watching one real person try to use it will teach you more than any amount of
debate.** When a team is stuck arguing about what's "intuitive," the answer isn't a
better argument; it's a quick test. Testing 3 users one morning, fixing the worst
problems that afternoon, and repeating beats an elaborate study. If the user is locked in
a "is this confusing?" debate, suggest a 15-minute hallway test over more theorizing.

## Spirit of the skill (read before you get dogmatic)

Krug is explicitly anti-dogma. These are **heuristics for reducing cognitive load, not
commandments.** The real test is always "does this make the user think?" — not "did we
follow the rule?" If a guideline here would, in a specific case, *increase* confusion,
the guideline loses. Reason from the user's experience and cite the specific question mark
you're removing.

Two failure modes to avoid, in tension with each other:

- **Don't pad.** Don't bury a review under rule-citations that don't help anyone; three
  real problems beat thirty restated guidelines.
- **Don't pull punches.** Avoiding padding does *not* mean softening genuine findings. When
  a screen carries real, heavy cognitive load — too many decisions, redundant controls, a
  wall of options — say so plainly and propose concrete cuts, even if that means
  recommending the design be substantially simplified rather than tweaked. "Looks mostly
  fine, minor wording nits" is the wrong answer for an overloaded screen. The honest,
  useful move is to name the load and show what to remove.

Good usability work is invisible; aim for the user never noticing how easy it was.

## Reference files

- `references/building-checklist.md` — Full building toolkit: navigation & "you are
  here" signage, breadcrumbs, the home page's job, search, forms, plus the complete
  scanning/visual-hierarchy detail.
- `references/mobile-usability.md` — The *Revisited* mobile chapter: touch targets,
  responsive trade-offs, the "we'll add usability later" trap, hidden navigation
  (hamburgers / "mystery meat"), flattened affordances, and small-screen scanning.
- `references/audit-report.md` — Review workflow, the self-evidence test, severity
  ranking, and the audit report template.
