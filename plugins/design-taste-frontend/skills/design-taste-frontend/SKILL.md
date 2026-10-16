---
name: design-taste-frontend
description: Anti-slop art direction for landing pages, portfolios, marketing and editorial pages, and redesigns. Distilled from a study of 247 curated gallery sites (One Page Love, Awwwards Sites of the Day); builds from an idea taken from the subject, a strict no-slop house style, and a look-and-fix loop on screenshots. Use whenever you build, design, redesign, restyle, polish or review a landing page, marketing site, portfolio, product page, one-pager, hero or any public-facing web page, in any stack (HTML/CSS, React, Next.js, Vue, Svelte, Astro, Tailwind) - also when the user says a page looks generic, templated, "AI-made", sloppy, or asks to make it look designed, premium, award-level or less like every other site. Not for dashboards, data tables, multi-step product UI, or app screens (including HCB Desktop caption UI).
---

# tasteskill v2

> **Scope guard.** This skill is for landing pages, portfolios, marketing and editorial pages, and
> redesigns of those. It is NOT for dashboards, data tables, multi-step product UI, app screens or
> Electron product UI such as the HCB Desktop caption overlay. If the request is one of those, say it
> is out of scope for this skill, do not apply its landing-page styling (large display type, bold
> colour fields, motion layer, editorial imagery), and follow the project's own design system instead.
> Everything below is contextual: read the brief first, then use only what fits it.

A page built by a model usually looks like the average of every page the model has seen: a centred
headline over three lines, a little label above it, a row of icon cards, a soft gradient, a few thin
rules and a monospace caption. Nothing in it is wrong and nothing in it was decided.

This skill replaces those defaults with decisions, in four ways:

1. **You compare directions before choosing one.** Asked to invent a look, a model picks the category
   default every time. Draft three distinct directions from the references, choose the one that
   carries the subject's idea, and then fix its type system, palette, hero and section compositions
   from the references, which are distilled from 247 real sites.
2. **The idea comes from the subject.** In the study, what separated the best sites from the forgettable
   ones was a concept taken from the thing itself, not the styling.
3. **A house style with no ornaments,** checked against the rendered page (see the gate in step 7),
   so the rules are checked rather than hoped for.
4. **You look at what you made.** Screenshots at three widths, a juror's rubric, fix, look again.

One warning learned in testing. Taking the ornaments away is only half the job; a page that has lost its
labels, rules and cards and gained nothing in their place reads as thin, and blind jurors rightly prefer
a richer page with tells over an empty page without them. The other half is substance: type set
larger, whole fields of colour, real pictures of this subject's world (found or drawn), and every
section carrying its full content. Do not trade it for restraint.

This plugin ships this file and the `references/` folder only. The references were written for the
upstream toolchain and sometimes mention its scripts (`draw.mjs`, `inspect.mjs`, `lint.mjs`,
`assets.mjs`), a `library/` folder and an `assets/` folder. None of those are included here. Do not
look for them and do not try to run them; take the design guidance and apply the check by hand.

## The run

Do these in order. Steps 1–5 take a few minutes and decide whether the page is any good.

### 1. Read the brief and the project

Find out what is real: the subject, the audience, the one thing the page must get someone to do, the
stack, any existing brand (colours, fonts, logo), and above all **what imagery truly exists**: the
project's own photographs or product shots, a real interface that can be shown, an image generation
tool you can call, or nothing. Do not plan around pictures you do not have. Nothing of its own is
rarely nothing at all: the subject's city, street, materials and history are in open archives and
museums, free to use with a credit (step 6).

If the request is vague, decide and state your reading in one line instead of asking. Ask only when a
missing fact blocks the work (for example, no product name).

Then **inventory the subject** in your notes: eight to twelve things that belong to this client and to
no competitor. Look for its name and what the name means; its address, door number, street and
neighbourhood, and what that place looks like (its tiles, signs, paint colours, typefaces on its shop
fronts, its light, its weather); the numbers in the brief (seats, rooms, minutes to the sea, the
price, the year); the constraint it lives with (only one batch a month, closed in winter, by
appointment); its materials and colours; its rituals and hours (the oven lit at five, the ferry at
seven); the printed things of its world (a timetable, a label, a ticket, a sign). This list is where
the idea comes from in step 4. In blind tests, the page that won each brief was built from an item on
such a list (the client's name and what it means, the street it stands in, the one constraint that
makes it what it is), and the pages that lost had a good composition with a category idea. The list
is also your picture search: each place, material and printed thing on it is a query for step 6.

### 2. Write the argument

Before any design, list the page as claims with their proof, one line per section, the way
`references/copy.md` §1 shows. The claims decide which sections exist and in what order. Delete any
section that has no claim. This is how you avoid the stock sequence of hero, logos, three features,
testimonial, pricing, call to action.

### 3. Choose the direction

Draft three genuinely different directions in your notes, each in two or three lines: how the page is
composed (the hero, the rhythm of sections), the type approach, the palette proportions, the kind of
imagery. Use `references/layout.md`, `references/type.md`, `references/colour.md` and
`references/imagery.md` for the options and their reasons. Hold each one against your inventory: which
way of composing can carry something only this client has? Choose that one, not the most familiar, and
write one line in your notes on why. A direction that did not suit the subject was the commonest cause
of a weak page.

Then write the **direction sheet** in your notes. It is the art direction for this build:

- the idea (step 4), the hero composition, and one composition per section (different from its
  neighbours), in the order of your argument;
- the type system (one family, two at most) and the colour roles: one ground, one ink, one accent,
  plus any fields of flat colour, with their proportions;
- the imagery plan and what really exists (see step 6);
- one signature move for step 9.

Adopt it. Do not blend it with the layout you would have made anyway. If it feels unfamiliar, good:
the familiar layout is the one this skill exists to prevent.

- Change a decision only for a reason you can state: it contradicts a stated brand constraint, or
  needs an asset that does not exist. Never change it to get something more comfortable. Record every
  change in your report.
- When a section composition cannot hold the real content (it compares three plans and there is one
  price; it wants five quotations and there are none), do not bend the content to fit; choose a
  composition whose assumptions match the content.
- **Check the palette against the subject.** A palette is a set of proportions (one ground, one ink,
  one accent, fields) as much as a set of colours. If its colours fight the subject's own material
  (candy pastels for a peat whisky, neon for a mountain hut), change it; if the subject has
  unmistakable colours of its own (its material, the paint of its street, the landscape outside its
  windows), keep the proportions and take the colours from the subject, and say so in the report.
- **An existing brand.** When the brand already fixes colours or typefaces, keep them, map their values
  onto the roles, and decide only the composition.
- Re-read the direction sheet before each section you build.

### 4. Find the idea

The direction is a way of composing. The idea is what makes the page belong to this subject and no
other. Write this sentence in your notes and do not start building until both blanks are filled from
the subject itself:

> On this page, **[something that belongs to the subject]** becomes **[the device the direction calls for]**.

Places to look for the first blank:

- **Its output.** What does the thing produce? Put the real output on the page as material. (A camera
  that prints poems delivered its copy as paper slips.)
- **Its object or shape.** What does it physically look like, in cross-section, in silhouette?
  Enlarge it, crop it, make it the frame or the one motif.
- **Its name.** Can the letters hold a photograph, stack into a wall, split to two corners?
- **Its place.** Is there one view that makes someone want to be there?
- **Its ritual.** Is there a sequence the page can perform as it scrolls?
- **Its artefact.** What printed thing already exists in its world: ticket, menu, label, receipt,
  invitation, folder, manual?
- **Its opposite.** Which other category owns the feeling this one lacks?

Fill the first blank from your inventory (step 1), not from the category. **The competitor test:** put
the nearest real competitor in the sentence (the bakery two streets away, another oak furniture maker,
another hut on the same mountain). If the sentence still works, the idea belongs to the category: a
loaf of bread is every bakery; the seven doors of the street this one is named after are only this one.
"Clean and modern" is not an idea. The sites the study's panel scored lowest were the ones whose idea
was recorded as "none beyond the standard formula".

**One live thing.** Give the page one thing the visitor can do, or that is different for each visit,
made from the idea: pick a wood and see the chair in it; type your name and see it cut in the
foundry's letters; set the loan and read the real monthly figure; see whether the hut's stove is lit
right now and how long until the last ferry; choose a size and see it against the room. In blind tests every winning page had one and the jurors named it first. Rules: it uses the subject's real content, it works on a phone with a thumb, it has a plain
fallback without script, it never blocks reading, and it is one thing, not a playground. It is
built in step 6 as part of the page, not added as motion in step 9.

### 5. Write the words

Write the whole page as a copy deck (plain text) before markup, following `references/copy.md`:

- **Every headline fits in two lines or fewer at every width.** Do the arithmetic in copy.md §2 before
  committing to a sentence: about 32 characters is safe everywhere at a confident size. The studied
  gallery heroes have a median of 5 words and 32 characters.
- One supporting sentence. One primary action, named for what it does, as a real button on the first
  screen.
- **The first screen answers the visitor's first question in large type.** For an event: what it is,
  when and where (the dates belong in the headline or at the second size, never only in small text).
  For a product: what it is and what it costs or does. For a person: who and what they do. Every
  section the visitor came for (the line-up, the menu, the rooms, the price) has its own heading and
  its own place in the navigation.
- **Write the full content.** Every section the brief asks for delivers its information completely:
  the whole menu with prices, each room with its own details, every speaker and talk, the price with
  what it includes, an answer for each real question. Thin sections are the commonest reason a clean
  page loses to a busier one.
- Sample details are expected where the brief leaves gaps (dish names, room names and rates, project
  titles) so the design is seen at full density; list them in the report for the client to confirm.
  Proof is never invented: no customers, quotes, reviews, press, logos or business statistics.

### 6. Build it, still

Build the page with motion switched off in your head; a page that needs animation to look finished is
not finished. Order of work:

1. **Tokens.** Colour and type roles from the direction sheet as CSS custom properties (or the stack's
   equivalent). Everything downstream references tokens only.
2. **The hero, exactly as your direction sheet describes it,** at desktop and at phone width. Get the big
   thing big and the small things small before anything else exists.
3. **Each section from its planned composition,** with this project's content. Neighbouring sections must not share a layout. **Carry the idea into every section,**
   pricing, FAQ and footer included: the commonest failure in the study, even among good sites, is a
   distinctive first screen followed by stock blocks.
4. **Imagery,** in this order of preference:
   1. the project's own;
   2. generated, if you have an image tool;
   3. **real pictures of the subject's world from the open collections,** whenever an honest one
      exists (Wikimedia Commons, Openverse, the Art Institute of Chicago and the Met; only licences that
      allow commercial use). Search them yourself with whatever web tools you have; if you have none,
      skip this rung and say so in the report. Search the inventory, not the category: its street in
      old postcards, an old map of the neighbourhood, its material up close, its trade in engravings, a
      museum object of its kind, a botanical plate, a star chart. Use them large and with intent: one
      archival photograph as the hero, an engraving enlarged into the page's motif, the real map of the
      street as the contact section. Look at each before choosing, download it into the project and
      record its title, creator, licence and source page for the footer credit. A found picture shows
      the world around the client and is never presented as the client's own product, room, dish,
      person or team;
   4. **drawn in code from the subject itself,** for what no honest picture exists of (its objects,
      its tiles, its windows, its product's interface, made as one consistent flat graphic language in
      the palette's real colours);
   5. generic photographs, only where an honestly generic picture fits (the sea for a
      sea house), never as a stand-in for the subject;
   6. type and colour alone.

   **Never fake the client's own work.** On a portfolio, case study or product page where the
   real work has no images yet, do not draw, mock up or invent the client's projects, screens or
   products, and do not leave empty image frames or "slot for later" boxes. Carry the work with type
   (a typographic project index, name-led rows, the real numbers and outcomes) and use only
   atmosphere pictures that are clearly about the world around the work, listed in the report for
   replacement. Rung 4 is for the subject's world, never for the client's own output.

   **The floor:** at least four real pictures on the page, usually six to
   twelve (photographs, archival images, maps, engravings, footage, raster artwork; for software, its
   cropped interface fragments count too). SVG drawings do not count toward the floor: draw what no
   picture exists of, and still carry real pictures. Add one moving picture wherever an honest clip
   exists: find it the same way and use it as a muted loop with a poster frame. Models skip pictures and footage because finding them is work; the page fails without them. When the client's own work has no images, meet the floor with atmosphere pictures only, never with stand-ins for the work.

   `references/imagery.md` covers searching, licences and credits, video, drawing, crops and treatments.
5. **The live thing** from step 4, built into the section where it proves the claim (often the hero
   or the booking), with real content, a thumb-sized phone version and a plain fallback.
6. **Fullness.** Look at each desktop screen as a poster: one dominant thing and the content it
   carries. A screen that is mostly empty ground is an underbuilt section, not a rest; one deliberate
   rest per page is the limit; a page with two or more near-empty screens fails.
   Running text is in the full ink at 16px or more; grey is for secondary notes.
7. **States and semantics.** Real links and buttons, visible focus, alt text, a phone layout that is
   its own composition.

Read `references/type.md`, `references/colour.md` and `references/layout.md` when you need the detail
behind a decision; the laws below are the short form.

### 7. Gate

Open the page in a real browser (or the nearest tool you have) at 1440, 768 and 390 pixels and save a
screenshot of each. Check by hand, against the house rules below:

- every headline, and the main line of the first screen, sets in two lines or fewer at every width;
- no eyebrow labels, monospace outside code, index numbering, thin rules, gradients, shadows at rest,
  glass, icon-topped card rows, tiny uppercase tracked labels or styled accent words;
- at least four real pictures, text contrast readable on every ground, no horizontal overflow on the
  phone, nothing lying on top of a headline or button;
- search the source for the stock phrases in `references/tells.md` and `references/copy.md` (unlock,
  supercharge, seamless, elevate, and the like).

Fix every failure. Treat anything doubtful as wrong unless you can defend it to a designer in one
sentence. Do not hide things from the check. If the page must also open straight from the file system,
open `index.html` that way once before you finish. If you cannot render the page at all, say so in
the report and do not claim visual checks you did not run.

### 8. Look

Passing the gate means nothing banned was measured. It does not mean the page is good. Open the
screenshots you saved in step 7 (every viewport, with your image viewer or Read tool) and critique them
with `references/critique.md`: the fourteen passes, the Awwwards-weighted score, the caps. Write the critique
down in its format, fix the top three problems, run the gate again, look again. Three rounds at
most.

Judge only the pictures. If a problem is visible in a screenshot, it is real, whatever the code says.

### 9. Move

Now build the motion layer. It is required, and it is more than one fade: count the
elements that really move while the page loads and is scrolled; fewer than eight is a failure and
fewer than sixteen is thin. The layer has four parts:

1. **The signature move** named on your direction sheet: one, done well.
2. **An entrance for the parts of every section:** the heading, then the text, then the picture,
   staggered by 60–90ms, rising 16–32px with opacity, triggered once as the section enters. Not one
   fade for the whole block, and never content that stays hidden if the script fails.
3. **Feedback on every control:** press, hover and focus on buttons, links, cards and the live thing.
4. **One moving picture:** a found clip as a muted loop, a slow scale or drift on a photograph, or a
   scroll-linked move on the hero picture.

Transform and opacity only; every move has a `prefers-reduced-motion` fallback that keeps the content
and drops the travel. A move that changes the colour or the layout of whole screens (colour by
chapter, a pinned story) is part of the composition, so build it in step 6 and let every look round see
it. `references/motion.md` has the tokens and tested recipes. Then re-run the gate and check every
screenshot for content that failed to appear.

### 10. Report

Tell the user, briefly: the direction chosen and any changes to it with reasons; the idea
sentence and the live thing; the final scores from your last critique round and what still falls short;
every found picture and clip with its title, creator, licence and source page and where its credit sits on the page; which generic photographs and which drawings stand in
for photography (so they can be replaced); and any sample content that must be swapped before launch.
Do not claim a check you did not run.

## House rules

These hold on every build, whatever the direction. Check them in step 7.

| Rule | Instead |
| --- | --- |
| **Headlines: two lines or fewer, at every width.** Every `h1`–`h6`, and the main line of the first screen whatever its tag. | Cut words. Then widen the measure. Size last. |
| **Statements are paragraphs.** An intro sentence or a quotation set large is marked up as `<p>` or `<blockquote>`, stays at statement size (36px or less on desktop, 24px on a phone) and runs to about 25 words, three lines. | Larger than that it is a headline and the two-line rule applies. In blind tests jurors read a 42px sentence over four lines as a four-line headline. |
| **No eyebrows.** No small label above a heading, no pill badge above the headline, no "New ·" chip. | Put the information in the heading or the first sentence, or drop it. |
| **No monospace** outside real code blocks. | The text face. Tabular figures where numbers align. |
| **No index numbering.** No 01 / 02 / 03, no (001), no "Step 2". | Order shown by position, size, or the words. A real `<ol>` if order matters. |
| **No thin rules.** No hairline dividers, no 1px outlined boxes, no grid lines, crosshairs or crop marks. | Space. A step in background tone. A change of scale. A filled shape. |
| **No gradients.** Not as backgrounds, not on buttons, not in text. | Flat colour, or a real photograph. A neutral scrim under text on a photo is the one exception. |
| **No shadows on things at rest.** No glows. | A tone step between surfaces. Shadows only on what truly floats: a menu, a dialog. |
| **No assistant palette.** No yellow-cream ground with terracotta or rust; no violet or indigo. | The palette from your direction sheet. |
| **No tiny uppercase letter-spaced labels.** | Sentence case at a readable size. |
| **No icon-topped feature cards, no rows of identical cards.** | A composition from your direction sheet. |
| **No glass.** No backdrop blur panels, no floating pill navigation. | A plain bar: wordmark, a few links, one action. |
| **No emoji, no gradient blobs, no decorative shapes, no fake dashboards of grey bars.** | A real picture, a real interface fragment, or nothing. |
| **No styled accent word** in a headline (italic, serif, coloured, underlined). | One face, one colour. The words carry the emphasis. |
| **Two typefaces at most,** usually one. | The type system from your direction sheet. |

Three places keep their own conventions and are exempt: real code in
`<pre>`/`<code>` (monospace is correct there), real tables and form fields (they may have lines), and
a real interface fragment whose root carries the attribute `data-ui` (the product's own borders and
menus; see `references/imagery.md` §7).

Why these, honestly. Some are what the study measured: among the 247 sites, those the panel scored
7.5 or higher used icon feature cards 1% of the time against 28% for sites under 6.5, pill badges 14%
against 34%, gradients 22% against 52%, shadows 24% against 48%, tiny tracked caps 16% against 57%.
Others are the owner's taste and go against current gallery fashion: monospace labels, index numbers
and hairline grids are actually *more* common on award sites than on weak ones, which is exactly why
generators imitate them and why they now read as costume. They are banned here without exception.
`references/tells.md` keeps the dated registry.

Removing ornament leaves space. Never fill it with another ornament. Fill it with scale (make the main
thing larger), with the full content, with a picture made for this subject, or with a field of flat
colour. Leave it empty on purpose once per page at most.

## Laws of the craft

Short form. Numbers are from the study unless marked as house style.

**Type**
- Two or three sizes do the visible work: one very large, one small, nothing in between. Median
  headline-to-body ratio on the studied sites is 4.3; the best go far beyond (largest type: median
  8.4vw on the top sites against 5.0vw on the weak ones).
- Display type: tracking -0.02 to -0.05em, leading 0.85–1.05. Text: 16–20px, leading 1.45–1.6,
  45–75 characters per line.
- Five sizes on a page is the ceiling. One family is normal (a third of the studied sites); two is the
  limit.
- Left-aligned by default. Centre at most one moment.

**Space**
- One grid, one pair of tight margins (16–32px), used everywhere; large things run to the edges. Text
  blocks share two or three left edges on the whole page.
- The gap between sections is clearly larger than any gap inside one: 120–220px on desktop.
- Each section has a different composition from its neighbours; none is a card grid.

**Colour**
- One ground, one ink, one accent. The accent appears on the action and perhaps one other thing.
- Running text in the full ink. A page set in soft grey reads unfinished.
- Surfaces are separated by a small step in tone, never by a line or a shadow.
- A section may change the whole field colour. Nothing fades into anything.

**Imagery**
- One dominant image beats six small ones. On the top-scored sites the hero media covers at least half
  the first screen 68% of the time.
- Same crop ratios, same treatment, square corners unless the direction says otherwise (73% of the
  studied sites leave media square).
- No image is better than a placeholder, an icon, or an abstract shape. A picture drawn for this
  subject, in its colours and with care, is better than either. A real picture of its world, found
  and credited, is better still.
- Every found picture is downloaded into the project, credited on the page and listed in the report.
  None is presented as the client's own.
- Nothing ever lies on top of a headline or a statement (a failure).

**Components**
- Buttons: flat, one fill colour, either square-cornered or fully round, decided once (top sites: 52%
  square, 23% pill; the 9–16px "soft" radius is the weak-site default). Most strong heroes have no
  button at all, or one.
- Navigation: wordmark, three to five plain links, one action. No bar chrome.
- The footer is a designed close, not a sitemap: on most strong sites the name returns at full width.

## Special cases

**An existing brand or design system.** Keep the brand's colours and faces, map them onto the roles, and
decide only the composition. The house rules still apply; if the brand itself requires a banned device
(its logo sits in a gradient, its accent is violet), keep the brand asset and say so in the report.

**Redesign or review of an existing page.** Render it and run the step 7 checks on it first and report
what they find, then critique the screenshots with `references/critique.md`. For a redesign, choose a
direction and proceed from step 2, keeping the page's real content and working behaviour.

**A component or a single section, not a page.** Skip the direction work unless there is none to
follow. Match the surrounding design, apply the house rules and the laws, and still check the result.

**No checkout, no form backend.** The primary button goes to the real destination when the brief names
one. Otherwise it opens an email with a written subject and body (`mailto:` with the visitor's choices
filled in), or, for a shop, it points at `#checkout` and the report says it must be wired before
launch. Never fake a payment form.

**No browser to render with.** Review the source against the house rules, and say in the report that the
page was not rendered.

**No network.** If you cannot search the open collections, draw the pictures and say in the report that
they could not be searched.

## Files

| File | Read it when |
| --- | --- |
| `references/copy.md` | Writing the argument and the copy deck (steps 2 and 5). The two-line arithmetic. |
| `references/type.md` | Setting type: scales, tracking, measure, loading fonts, pairing. |
| `references/colour.md` | Applying the palette: roles, proportions, tone steps, dark pages, contrast. |
| `references/layout.md` | Grid, margins, rhythm, section variety, navigation, footer, the phone composition. |
| `references/imagery.md` | Choosing, finding, crediting, cropping and treating pictures; what to do with none. |
| `references/motion.md` | Step 9. Budget, tokens, recipes, reduced motion. |
| `references/critique.md` | Step 8. How to look, how to score, what to fix first. |
| `references/tells.md` | The dated registry of generated-page tells and what each is replaced by. |
| `references/research.md` | The study: method, numbers, what the best and worst sites do. Cite it, do not guess. |
