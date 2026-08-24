# Portfolio — Dandrell E. Johnson II

One HTML file. No build step, no framework, no install. Open
`index.html` in a browser and it runs.

Editing instructions are in a comment at the very top of
`index.html` — open the file and read the first sixty lines.

---

## Putting it online (GitHub Pages, free)

1. Create a repo named **exactly** `yourusername.github.io`
2. Put `index.html` at the top level, not in a folder
3. Add the `assets/` folder alongside it
4. Settings → Pages → Source: `main` branch
5. Live in about two minutes at `https://yourusername.github.io`

To update anything later, edit the file, commit, push. The live site
follows within a minute.

---

## The old Google Site

Don't delete it. Strip the homepage down to your name and one button
pointing at the new address. Old links stay alive and it costs
nothing.

If you later buy a domain (~$12/year), point it at GitHub Pages. Then
the address changes in one place. **Put the domain on your resume, not
the github.io address** — that way the resume never goes stale if you
move hosts.

---

## Files

| File | What it is |
|---|---|
| `index.html` | The entire site |
| `PHOTO-CHECKLIST.md` | Every photo, its filename, its shape |
| `EXPLODED-VIEW-HOWTO.md` | Exporting CAD frames from SolidWorks / Inventor / Fusion |

---

## Before you ship

- [ ] Open it on your own phone **with wifi off** — this is the real test
- [ ] Real photos in, then re-check layout at phone width
- [ ] Check it once on a wide desktop monitor
- [ ] Lighthouse in Chrome, mobile preset — watch performance and LCP
- [ ] Turn on reduced motion in phone settings, confirm it still reads
- [ ] Both press links open, and open in a new tab
- [ ] Phone number and GPA settled and consistent everywhere

---

## Known performance issues

Not broken, but worth fixing before this gets heavy traffic:

1. **Frame sequence preloads all 90 images before showing anything.**
   On cellular that's a stall. Should load a first chunk, start
   playing, fill in the rest behind it.
2. **Duotone runs grayscale + blend on full-size photos every scroll
   frame.** Expensive on mid-range Android.
3. **Three font weights load render-blocking from Google's CDN.**

---

## How it's built, briefly

Five scroll mechanisms all run off one helper that answers "how far
through this element are we, 0 to 1." One `requestAnimationFrame`
loop drives everything. Reduced motion is respected throughout. No
browser storage is used anywhere.

The numbered ruler across the top is the signature element — the lit
column is your actual position in the document, not decoration.

Typefaces: Anton for display, IBM Plex Sans and Mono for everything
else. Colours: vellum paper, near-black ink, drafting blue, one brick
red used *only* for links and folios — so red always means "there's
something here."

If you change one thing, keep that last rule. It's what stops the
page from looking decorated.
