# MichaelTravels

Source for **[michaeltravels.org](https://michaeltravels.org)** — travel journals and photographs.

A plain static site. No build step, no framework, no dependencies. Every page is a single
self-contained HTML file with its CSS and JavaScript inline, and a folder of photographs beside it.

## Layout

```
index.html            home page — one card per trip, newest first
_redirects            Netlify redirect rules
.gitignore
<trip>/index.html     one folder per trip
<trip>/photos/        hero.jpg + <section>_<n>.jpg
<trip>/videos/        italy2024 only — self-hosted mp4s
```

Trips: `nz2026` · `italy2025` · `colorado2025` · `italy2024` · `italy2022` · `antarctica`

## Editing

Work in this folder. Open the HTML file for the trip you want to change, edit it, save, and
double-click it to check in a browser — there is nothing to compile.

Each trip page follows the same shape:

- a full-bleed `.hero` image with the title over it
- a `.stats` strip
- `.timeline` of `section.day` blocks — label, heading, paragraphs, `.tags`, photo grid
- a footer linking to every other trip
- a lightbox (`#lb`) for the photographs

Photo grids are driven by a `MANIFEST` object in the `<script>` at the bottom of each page, with a
matching `CAPTIONS` map. To add photographs: drop the files into `<trip>/photos/`, then add their
filenames to `MANIFEST` and captions to `CAPTIONS`. Nothing else needs touching.

### Two rules worth remembering

1. **Use relative photo paths** — `photos/foo.jpg`, never `/photos/foo.jpg`. The `/photos/*` rule
   in `_redirects` catches root-absolute paths site-wide and silently redirects them into the
   New Zealand gallery.
2. **Films go to YouTube**, linked as `<a class="tag vid" href="https://www.youtube.com/watch?v=…">`,
   not embedded as large files in the repo. Keeps the repo small and the pages fast.

## Publishing

Netlify is connected to this repository and deploys the `main` branch automatically.

```
edit → commit → push → Netlify builds → live in about a minute
```

No build command; publish directory is the repository root.

To undo a bad deploy: Netlify → Deploys → pick the last good one → **Publish deploy**. That is
instant and does not touch this repository.

## Adding a trip

1. Copy an existing trip folder as a starting point and rename it.
2. Replace the photographs in `photos/`, and update `MANIFEST` and `CAPTIONS`.
3. Rewrite the hero, stats and section text. Give the page its own accent colours in `:root`.
4. Add a card to `index.html` — cards run newest first, oldest last.
5. Add a link to the new trip in the footer of every other trip page.
6. Commit and push.

## Working with Git day to day

Four places, three verbs:

```
working folder --stage--> staging --commit--> local repo --push--> GitHub --> Netlify deploys
      ^                                                                |
      +-------------------------------- pull -------------------------+
```

A **commit** is a labelled snapshot that never leaves this PC. **Push** sends commits to GitHub.
**Pull** brings GitHub's commits down here. Committing publishes nothing — push is what publishes.

### In GitHub Desktop

| What you want | Where |
|---|---|
| See what you changed | **Changes** tab; the checkboxes are the staging area |
| Save a snapshot | Summary box → **Commit to main** (local only) |
| Publish it | **Push origin**, top bar |
| Check GitHub for changes | **Fetch origin** — becomes **Pull origin** if GitHub is ahead |
| See past commits | **History** tab |

The habit: fetch before starting, commit in small pieces with a real message, push when you stop.
Messages are one line, plain — `Add Antarctica page`, `Fix footer links on Italy pages`.

### Pull matters even working alone

GitHub gets ahead whenever a file is edited in the browser on github.com, or another machine
pushes, or an assistant commits on your behalf. Pull first and there is nothing to untangle.

### Undoing things

| Situation | Fix |
|---|---|
| Edited a file, not committed | Changes tab → right-click the file → **Discard changes** |
| Bad commit, not pushed | History → right-click → **Revert** (makes an undo commit; nothing is lost) |
| Bad commit, already pushed | Same **Revert**, then push |
| Bad *deploy* | Netlify → Deploys → last good one → **Publish deploy**. Instant, doesn't touch Git |

Conflicts only happen when the same lines change in two places. Editing only in this folder means
you will most likely never see one.

### Two things not to do

- **Don't edit the old OneDrive copy** (`…\OneDrive\Pictures\Michael Hancock\michaeltravels site`).
  It is a frozen backup as of 2026-09-01. Edits there will never reach the site.
- **Never force-push.** Nothing about this site needs it.
