# Photo checklist

Every filename below is exactly what the site is looking for.
Lowercase, hyphens not spaces, `.jpg` not `.jpeg`.

Missing files don't break anything — you get a grey box with the
filename printed in it. So add them one at a time and watch the
boxes disappear.

---

## Folder layout

```
index.html
assets/
    resume.pdf
    gallery/
        racecar.jpg
        rover.jpg
        ncsa.jpg
        trane.jpg
        shop.jpg
        fsae-chassis.jpg
        harness.jpg
        spl.jpg
        manifold.jpg
        arm.jpg
        print.jpg
    seq/
        frame_0001.jpg  ...  frame_0090.jpg
```

---

## The five chapter photos

These are the big ones. Shape matters here — the layout reserves a
specific box, so a photo of the wrong shape gets cropped to fit.

| File | Shape | What it should be |
|---|---|---|
| `racecar.jpg` | 4:5 tall | The finished Formula SAE car. Best single photo you have of it. |
| `rover.jpg` | 4:3 wide | NASA HERC rover — on the course if possible, in the shop if not. |
| `ncsa.jpg` | 4:5 tall | NCSA. A screen of the crack segmentation output works if there's no photo of you there. |
| `trane.jpg` | 4:3 wide | La Crosse. The assembly cell, the line, anything from that plant. |
| `shop.jpg` | 4:3 wide | Heil, Fort Payne. Production floor. |

**Two of these are clickable press links** — `racecar.jpg` goes to the
AL.com article, `rover.jpg` to the NASA HERC piece. Those URLs still
need pasting in. Search `PRESS LINK` in index.html.

---

## The six strip photos

The strip slides sideways as you scroll. These alternate shape
automatically — 1st, 3rd, 5th sit wide, 2nd, 4th, 6th sit tall and
drop down a little. So order changes the rhythm.

| File | What it should be |
|---|---|
| `fsae-chassis.jpg` | Chassis mid-build, tubes visible |
| `harness.jpg` | Wire harness work |
| `spl.jpg` | Special Projects Laboratory |
| `manifold.jpg` | Intake / air manifold |
| `arm.jpg` | Capstone arm, current state |
| `print.jpg` | Something on the print bed |

**Adding more:** copy a whole `<figure>` block, paste it after the
last one, change the filename in both places. As many as you like.

---

## Sizing

- Longest edge around **1600px**. Bigger is wasted — they never
  display larger than that.
- Save at **JPEG quality 80**. Aim under 300 KB each.
- Don't colour-correct them. The site pushes every photo through a
  blue duotone that clears to full colour as it crosses the middle of
  the screen. Mismatched lighting and backgrounds get evened out
  automatically — that's the whole reason it's built that way.

If a background is genuinely distracting, cut the subject out and
leave it transparent. The page colour becomes the background.

---

## The exploded view frames

`assets/seq/` wants `frame_0001.jpg` through `frame_0090.jpg`.
Four digits, zero-padded. Export instructions are in
EXPLODED-VIEW-HOWTO.md.

Whole sequence should total **under 5 MB**. If it's over, drop to 60
frames and lower the quality — you won't see the difference while
scrolling.

If the folder is empty the page still works. That section just shows
a static placeholder instead of animating.

---

## Also needed

`assets/resume.pdf` — the contact section links to it for download.

**Before you upload that PDF:** your resume and your old Google Site
listed two different phone numbers, and your resume and cover letter
listed two different GPAs. Settle both first. A hiring manager who
spots a mismatch reads it as carelessness, and it's the cheapest
possible thing to fix.
