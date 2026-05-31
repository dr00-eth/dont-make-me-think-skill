# Building Checklist — the full Krug toolkit

Depth behind the core principles in SKILL.md. Read the section relevant to what you're
building; you rarely need all of it at once.

## Contents
- [Designing for scanning](#designing-for-scanning)
- [Visual hierarchy in practice](#visual-hierarchy-in-practice)
- [Navigation & signage](#navigation--signage)
- [Breadcrumbs and "you are here"](#breadcrumbs-and-you-are-here)
- [The home page's job](#the-home-pages-job)
- [Search](#search)
- [Forms](#forms)
- [Omitting needless words in practice](#omitting-needless-words-in-practice)
- [Goodwill — the usability reservoir](#goodwill--the-usability-reservoir)
- [Accessibility as usability](#accessibility-as-usability)

---

## Designing for scanning

Users scan because (a) they're usually in a hurry, (b) they know they don't need to read
everything, and (c) they're good at it from years of practice. Support the scan:

- **Lots of meaningful headings.** Headings are the skeleton of the page. Someone reading
  only the headings should grasp the structure and find their section. Make heading
  levels visually distinct enough that the hierarchy is obvious — and keep a heading
  visually closer to the text it introduces than to the text above it.
- **Short paragraphs, one idea each.** Walls of text repel scanners. Break them up.
- **Bulleted lists** for anything that is, in fact, a list. Prose that hides a list
  ("you'll need a passport, a ticket, and proof of vaccination") scans worse than bullets.
- **Highlight key terms** — the words a scanning user is hunting for. Don't over-highlight;
  if everything is bold, nothing is.
- **Keep the line of sight clean.** The path a user's eye takes to the next action should
  be unobstructed by ads, callouts, or decorative noise.

## Visual hierarchy in practice

A good page is "pre-processed" for the user — the visual relationships mirror the logical
ones, so the brain does less work:

- **Importance → prominence.** Size, weight, color, and whitespace signal what matters.
- **Logical grouping → visual grouping.** Things that belong together look together
  (proximity, shared background, a box, alignment).
- **Containment → nesting.** Sub-items are visually inside their parent (indentation,
  enclosure). The structure should be readable without reading the words.

When hierarchy is wrong or absent, users must read everything to find anything — exactly
the thinking you're trying to eliminate.

## Navigation & signage

Navigation isn't a feature; it *is* the site to a user. It tells them what's here, how to
get to it, and — crucially — where they are. Persistent, predictable navigation reduces
the constant low-grade anxiety of "am I lost?"

Conventional web nav elements users expect:

- **Site ID / logo**, top-left, linking home. It's the "you can always start over" anchor.
- **Sections (primary nav)**, persistent across pages, with the current section visibly
  highlighted.
- **Utilities** (account, help, cart, search) in a consistent, secondary spot.
- **A search box** that looks like a search box (input + button, magnifying glass).
- **Page name**, prominent, matching the link/label that brought the user here. A page
  with no clear name leaves users unsure they arrived where they intended.

Persistent nav can be sensibly omitted on a few pages — forms/checkout flows where you
*want* focus, and any full-screen task — but that's a deliberate exception, not a default.

## Breadcrumbs and "you are here"

Two cheap, high-value orientation tools:

- **"You are here" indicators** — highlight the current section/page in the nav so users
  always know their location in the structure. Without it, every nav is a guess.
- **Breadcrumbs** — show the path from home to here (Home > Products > Bread > Sourdough).
  Best for deep hierarchies. Keep them small, put them at the top, boldface the current
  page, and make the rest clickable.

## The home page's job

The home page carries more burden than any other and can't please everyone — accept that.
It must, in a glance, answer: **What is this? What can I do here? Why should I be here
rather than somewhere else? Where do I start?** Specifics:

- **Site identity and mission**, clear and immediate. A **tagline** — a pithy phrase that
  characterizes the whole — does enormous work; a vague or missing one leaves visitors
  guessing.
- **Show the big picture *and* an obvious entry point.** Don't make users hunt for where
  to begin.
- **Resist the pressure to cram.** Every stakeholder wants their thing on the home page;
  the result is noise. Prioritize ruthlessly toward the few things users and the business
  most need.

## Search

Many users are "search-dominant" — they ignore nav and head straight for the box. So make
it findable and plain: a simple text field with a clearly labeled button, in the expected
spot, without fancy wording ("Search" beats "Find it!" or "Quick Jump"). Don't make people
choose a category or scope before searching unless it's genuinely necessary.

## Forms

Forms are where vague labels and unclear requirements cost the most:

- **Label every field unambiguously**, and place the label where its association is
  obvious.
- **Ask only for what you need.** Every extra field is friction and a small insult ("why
  do they need my phone number?"). Cutting fields is a usability win.
- **State requirements up front** (password rules, accepted formats) rather than punishing
  users with an error after they submit.
- **Make errors recoverable and specific**: say what's wrong, where, and how to fix it —
  in plain language, next to the field.

## Omitting needless words in practice

Two big targets:

- **Happy talk** — content-free welcome/promotional chatter ("Welcome to our site! We
  hope you'll enjoy exploring all the wonderful things we have to offer"). Delete it.
- **Instructions** — most can be eliminated by making the thing self-explanatory. The ones
  that remain should be as short as humanly possible.

The payoff isn't just brevity: every word you cut reduces noise, so the words that
*matter* become easier to find. Aim to cut half, then half again — you'll be surprised how
little is lost.

## Goodwill — the usability reservoir

Users arrive with a reservoir of goodwill. Each frustration drains it; each "oh, that was
easy" refills it. Things that **drain** goodwill (avoid them):

- Hiding information people obviously want (prices, contact info, shipping cost).
- Punishing users for not doing things your way (rigid format requirements you could
  parse, e.g. credit-card numbers with/without spaces).
- Asking for more info than you need.
- Shucking and jiving — fake urgency, dark patterns, burying the unsubscribe.
- An amateurish, unmaintained, or sloppy appearance that signals "we don't care."

Things that **refill** it: knowing the common questions and answering them, saving users
steps, making it easy to recover from errors, and not treating users as marks.

## Accessibility as usability

Accessibility isn't a separate compliance chore bolted on at the end — it's usability for
more people. Most things that help users with disabilities (clear headings, real text,
proper labels, good contrast, keyboard operability, alt text, descriptive links) also make
the interface more usable for *everyone* and more scannable for *everything*, including
search engines and screen readers. Build it in; don't make people think *or* lock them out.
