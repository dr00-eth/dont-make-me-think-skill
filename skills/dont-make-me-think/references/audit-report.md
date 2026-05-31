# Usability Audit — workflow and report format

Use this when the user asks you to review, critique, audit, or "make clearer" an existing
interface (a screenshot, a live URL, a component, a flow, or a description). The goal is a
focused, prioritized usability report grounded in Krug's principles — not a scattershot
list of opinions.

## The self-evidence test (run this first, on every screen)

Before listing issues, simulate a hurried, distracted first-time user and answer these out
loud for the screen/flow. Each "I'm not sure" is a usability finding:

1. **What is this?** Is the page/section identity obvious at a glance?
2. **Where am I, and where can I go?** Is location-in-the-site and navigation clear?
3. **What can I do here, and where do I start?** Is the primary action obvious?
4. **What's clickable/tappable?** Can I tell without hovering or probing?
5. **Where's the thing I came for?** Can I scan to it, or must I read everything?
6. **What do these labels mean?** Any jargon, cute names, or ambiguous links?
7. **Is anything making me work needlessly?** Happy talk, clutter, redundant steps,
   over-long copy, unnecessary form fields?
8. **How many decisions is this screen actually asking me to make — and are any of them
   redundant?** (See "Count the load" below. This is the most important question on dense
   forms, settings, and wizards, and the one most often missed.)

This test *is* the review. Findings fall out of the questions a real user can't answer.

## Count the load (do this on every dense screen)

On a form, settings panel, dashboard, or wizard, the biggest usability lever is rarely
wording — it's the **number of decisions**. Make the load explicit:

1. **Enumerate every decision** the screen asks the user to make — each field, toggle,
   radio group, dropdown, and step. Literally count them.
2. For each one, ask the **reduction questions**:
   - **Remove** — does this need to exist at all, or is it here because it was easy to add?
   - **Default** — can a sensible default let the typical user skip it entirely?
   - **Derive** — can the system compute this from something it already knows?
   - **Defer** — is this a rare/advanced option that belongs behind collapsed progressive
     disclosure rather than in the main flow?
3. **Flag redundancy explicitly.** Look for two controls that set the same thing (a radio
   group *and* a dropdown deciding the same behavior, or a setting that appears in both the
   main view and an "Advanced" section). Each one forces a "which one wins?" question and
   should collapse to a single control.

The output of this pass is a concrete simplification proposal — "this screen asks ~9
decisions; 3 can be defaulted, 2 are redundant and should merge, 1 is advanced and should
collapse, leaving ~3 the user actually needs to touch." That is usually the single most
valuable thing in the whole review, so don't soften it.

## Workflow

1. **Establish context.** What is it, who's the user, what's the top task they're trying to
   accomplish? A review without a user goal is just decoration critique.
2. **Run the self-evidence test** on each key screen/step of the flow.
3. **Count the load** on any dense screen (forms, settings, wizards) — enumerate the
   decisions and run the reduction questions. Don't skip this; it's where the biggest wins
   usually hide.
4. **Walk the primary task end to end**, noting every point where you (as the stand-in
   user) have to stop and think. These pause-points are the raw findings.
5. **Check mobile** if in scope — read `mobile-usability.md` and re-run the test on a small
   screen, watching for hidden nav, tiny targets, and reflow damage.
6. **Rank and write up** using the format below.
7. **Recommend a real usability test** when appropriate. Your audit is an expert review —
   valuable, but no substitute for watching real users. If the team is debating what's
   "intuitive," say so and suggest a quick 3-person hallway test.

## Severity ranking

Prioritize by how much each issue makes users think, and how many users it hits. Don't
bury a showstopper under nitpicks.

- **Showstopper** — users can't complete the task, or are very likely to fail/leave (a
  primary action that's invisible, a label that misleads, a broken mental model).
- **Major** — significant friction or confusion; users get through but with avoidable
  effort or doubt.
- **Minor** — small papercuts; worth fixing but won't break the experience.
- **Polish** — refinements and nice-to-haves.

## Report format

Use this structure. Keep it tight — practice what the book preaches and omit needless
words.

```
# Usability Review: [what was reviewed]

## Context
- What it is, the target user, and the primary task evaluated.

## Verdict
- 2–4 sentences: overall, how much thinking does this interface demand? For a dense
  screen, state the rough decision-count and the biggest opportunity to cut it. What's the
  single most important thing to fix?

## Simplify (for dense forms / settings / wizards)
- The result of the "Count the load" pass: which decisions can be removed, defaulted,
  derived, deferred, or merged, and roughly how many the user would actually be left with.
- Lead with this when the core problem is overload — it usually matters more than any
  individual wording or layout finding. Omit this section only for screens that genuinely
  aren't decision-dense.

## Findings
For each issue, in severity order:

### [Severity] Short title of the problem
- **Where:** the specific screen/element.
- **The question mark:** what the user has to stop and think about, and which Krug
  principle it touches (scanning, conventions, clickability, omit-needless-words, nav,
  labels, goodwill, mobile, etc.).
- **Why it matters:** the cost to the user / likely behavior.
- **Fix:** a concrete, specific change. Show the before→after wording or layout when it
  helps.

## Quick wins
- A short bulleted list of low-effort, high-impact fixes the team could do today.

## Recommended next step
- Usually: a 15-minute test with 3 real users on the primary task, or the top fix to ship
  first.
```

## Tone and judgment

- **Be specific, not abstract.** "The 'Continue' button is the same gray as disabled text,
  so users won't see it's the primary action" beats "improve visual hierarchy."
- **Cite the question mark, not the rule.** Lead with the user's confusion; mention the
  Krug principle as support, not as the point.
- **Don't pad.** A review with three real showstoppers is more useful than thirty
  rule-citations. If something's genuinely fine, say it's fine.
- **Respect intentional choices.** If a convention is broken but the alternative is
  genuinely self-evident, that's a pass — note it and move on. The standard is "does it
  make me think?", never "did they follow the rulebook?"
