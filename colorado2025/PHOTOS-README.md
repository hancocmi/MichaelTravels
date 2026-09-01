# Colorado 2025 — build notes

Upload the whole `colorado2025/` folder to `michaeltravels.org/colorado2025/`.
Self-contained: one `index.html` plus `photos/`. No external CSS or JS.

**Total size: ~24 MB** (51 JPEGs + hero). Grid images are lazy-loaded, so the
initial page load is only the hero plus whatever is on screen.

## Source

- **Photos:** `D:\Users\Michael\OneDrive\Pictures\Michael Hancock\Colorado 2025`
  — 71 HEIC files, converted to progressive JPEG (grid 1600px / q82, hero 2400px / q80),
  EXIF rotation applied.
- **Notes:** `Colorado 2025.md` from the Obsidian vault.

51 of the 71 photos were used. The rest were near-duplicate frames from the same
burst — easy to swap in if you want a different pick from any group.

## Sequence

The photo timestamps reconstruct the day cleanly. All times MDT.

**April 7** — Colorado College 09:34–10:04 · snow road up 11:45 · Cripple Creek
district 12:14–14:07 · Pikes Peak Highway 15:12–15:41 · Ute Pass overlook 15:50 ·
Garden of the Gods 16:22–16:28

**April 8** — first ski area 16:31 · second ski area 16:48

## Sections and filenames

| Section | Files |
|---|---|
| Hero | `hero.jpg` |
| Arrival | `arrival_1.jpg` |
| Castle Rock | *(no photos — text only)* |
| Colorado Springs | `cosprings_1–8.jpg` |
| Into the high country | `goldcamp_1–4.jpg` |
| Cripple Creek | `cripplecreek_1–8.jpg` |
| Pikes Peak | `pikespeak_1–8.jpg` |
| Ute Pass | `utepass_1–6.jpg` |
| Garden of the Gods | `gardenofgods_1–8.jpg` |
| Loveland & A-Basin | `ski_1–8.jpg` |

Any missing image degrades to a labeled placeholder tile rather than a broken-image
icon, so you can add or reorder without breaking the layout.

## Things to check

**Captions I kept deliberately vague.** I could identify the Colorado College signage,
the Poverty Gulch marker, and the Ute Pass overlook sign directly from the photos.
I did *not* name individual campus buildings, the specific open-pit operation at
Cripple Creek, or which ski area is which — the two April 8 sets are 17 minutes apart,
which fits Loveland and A-Basin in either order. Tell me the right answers and I'll
tighten the captions.

**Castle Rock has no photos.** Nothing in the folder covers it, or the arrival, or
Manitou Springs town proper. That section is text only right now.

**8 video clips (~100 MB) were not used** — `.MOV` files from both days. Say the word
and I'll transcode them to web MP4 and add "Watch →" chips the way the New Zealand
page does.

**Two claims worth a second look:**

1. Your note says A-Basin and Loveland were "the only two ski resorts still operating
   in April." Breckenridge, Copper, and Winter Park typically run into April too, so
   I softened it to "the diehards… long after the rest of the state has moved on to
   mud season." Easy to put back.
2. Pikes Peak, Cripple Creek, Manitou Springs, and Garden of the Gods were bare
   headings or absent in your notes. I wrote those from general knowledge — elevations,
   the 1890 gold strike, the 1991 gambling vote, the Perkins family gift of 1909, the
   mineral springs, the Incline. All checkable, none of it personal. Swap in what you
   actually did and I'll rewrite.

## Link audit

All 35 external links were fetched and confirmed live. Five were wrong in the first
draft and are now fixed:

| Was | Now | Why |
|---|---|---|
| `stfranciscastlerock.org` | `stfranciscr.org` | Domain didn't exist — you caught this one |
| `manitoumineralsprings.org` | `manitousprings.org/mineral-spring-water/` | Ditto — your second correction |
| `coloradosprings.gov/pikespeak` | `coloradosprings.gov/pikes-peak-americas-mountain` | Old path, dead |
| `wikipedia.org/wiki/Castle_Rock_(Colorado_butte)` | `..._(Colorado)` | Wrong article title |
| `wikipedia.org/wiki/Gold_Camp_Road` | uncovercolorado.com | No such Wikipedia article |

Two links removed outright:

- **Mollie Kathleen Gold Mine** — their site now reads "closed for the foreseeable
  future." Linking it as a thing to go do would have been misleading.
- **Cave of the Winds** — tangential and unverified; replaced with the City of
  Colorado Springs' Garden of the Gods page.

Also corrected in the prose:

- **Space Command.** I originally wrote it in the present tense. The HQ was ordered
  moved to Huntsville in September 2025 — after your April visit — and the phased
  relocation is underway, so the sentence is now anchored to "that spring."
- **Cripple Creek population.** I'd written "a town of ten thousand." The district
  peaked near fifty thousand; the railway's own history page says the population
  "approached over 50,000." Changed, and added the stock exchange.
- **Ute Pass.** Added the Ute name for the pass — *El Puerto del Sierra Almagre*,
  the doorway to the red earth mountains — from the Ute Pass Historical Society via
  Wikipedia.

## Sources for the researched sections

- [Pikes Peak – America's Mountain, City of Colorado Springs](https://coloradosprings.gov/pikes-peak-americas-mountain) — 14,115 ft, the 19-mile highway, Crystal Reservoir
- [Ute Pass, Wikipedia](https://en.wikipedia.org/wiki/Ute_Pass) — US 24, the buffalo trail, the Ute name
- [Cripple Creek & Victor Gold Mine, Wikipedia](https://en.wikipedia.org/wiki/Cripple_Creek_%26_Victor_Gold_Mine) — over 23M oz since 1890, the Cresson pit
- [Cripple Creek & Victor Narrow Gauge Railroad](https://www.cripplecreekrailroad.com/) — district population near 50,000
- [Visit Cripple Creek, City of Cripple Creek](https://visitcripplecreek.com/) — 9,500 ft
- [Manitou Incline, City of Colorado Springs](https://coloradosprings.gov/parks/page/manitou-incline) — 2,000 ft gain in under a mile
- [Garden of the Gods Visitor & Nature Center](https://gardenofgods.com/) — the 1909 deed, "forever free"
- [Pikes Peak Cog Railway opens after four-year hiatus, CPR](https://www.cpr.org/2021/05/20/pikes-peak-cog-railway-opens/) — closed 2017, reopened May 2021
- [Space Command begins phased move to Alabama, SpaceNews](https://spacenews.com/space-command-begins-phased-move-to-alabama/) — HQ relocation
- [St. Francis of Assisi, Castle Rock](https://www.stfranciscr.org/) and [Manitou mineral springs](https://manitousprings.org/mineral-spring-water/) — supplied by you
