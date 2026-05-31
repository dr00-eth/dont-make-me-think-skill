# Mobile Usability — the *Revisited* additions

The *Don't Make Me Think: Revisited* edition added a chapter on mobile. The core law is
unchanged — **don't make me think** applies identically on a phone — but small screens,
touch input, and on-the-go contexts make violations hurt more and introduce new traps.

## The mindset: same principles, harsher constraints

A phone gives you less room, a blunter pointer (a finger, not a pixel-precise cursor), no
hover, frequently a worse connection, and a user who is often distracted, one-handed, and
in a hurry. None of that changes *what* good usability is — it just removes your margin for
error. Everything in the web checklist still applies; this file covers what's *different*
or *amplified*.

## Real estate vs. usability is a false trade-off

The central mobile tension: a small screen tempts you to hide things to "save space."
Krug's warning is that designers too often sacrifice usability to cram more in, when the
right move is to **prioritize ruthlessly** — decide what matters most and give it the room
it needs. Hiding everything behind menus and icons saves pixels but spends the user's
thought. Cut content and features before you bury them.

## Don't hide navigation behind mystery

Hidden navigation (the hamburger menu and friends) is a reasonable space-saver, but it has
a real cost: **out of sight, out of mind.** People use what they can see far more than what
they have to go find. Guidance:

- If something is important, **keep it visible**, not buried in a menu.
- Make the menu **affordance obvious** — a recognized icon plus, ideally, the word "Menu."
  Bare, unlabeled icons are the return of **"mystery meat navigation"**: the user has to
  tap to find out what something does. Every "what is this icon?" is a question mark.
- Don't hide your *primary* actions. A hamburger for secondary nav is fine; the main thing
  users came to do should be a visible, tappable control.

## Touch targets and the disappearance of affordances

- **Make tap targets big enough and well-spaced.** Fingers are imprecise; tiny or crowded
  targets cause mis-taps, which are pure frustration. Give actionable elements generous
  size and breathing room.
- **There is no hover on touch.** Anything that relied on hover to reveal itself (tooltips,
  hover menus, "this is clickable" cues) must be rethought — the information or affordance
  has to be visible without it.
- **Flat design flattened affordances.** When buttons stopped looking like buttons, "what's
  tappable?" got harder — a direct hit to Krug's "make it obvious what's clickable." On
  mobile especially, make tappable things *look* tappable; don't rely on users probing the
  screen to discover what reacts.

## Scanning on a small screen

Scanning matters *more* on mobile, because less fits in view and the user is more
distracted. Tighten everything: front-load the important content, keep headings and chunks
short, and make sure the single most important action is visible without scrolling. Long
intros, big hero images that push content "below the fold," and multi-step preambles cost
more here than on desktop.

## The "we'll make it usable later" trap

Krug calls out a specific organizational failure: teams ship a cramped, hard-to-use mobile
experience and promise to "fix the usability when we have time" — which never comes.
Usability is not a later phase. If you're building mobile or responsive UI, bake these
principles in from the first pass; retrofitting clarity onto a cramped layout is far
harder than designing for clarity up front.

## Responsive trade-offs

Responsive/adaptive layouts are good, but reflowing a desktop design into a column is not
automatically usable. Check the *result* on a real small screen:

- Did important controls get pushed far down or into a hidden menu?
- Did touch targets end up too small or too close once reflowed?
- Did multi-column relationships (label ↔ field, item ↔ price) survive the stack, or did
  they get visually separated so the association is now unclear?
- Is text still scannable, or did it become a wall in a narrow column?

The test is always the same: pick up the phone, glance at it the way a hurried, distracted
person would, and see whether you have to *think*.
