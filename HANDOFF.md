# Signature Home Renovations LLC — handoff at ~60%

**Live:** https://10elizabethbell.github.io/signatureHomeRenovations/ (GitHub Pages, main /) · **Repo:** https://github.com/10elizabethbell/signatureHomeRenovations · **Built:** 2026-10-08 from Muse brief (run 2026-10-08)

## What's built
- **World:** a wet cobalt-tile shower wall with gold grout, taken from their best photo (cobalt tile + brass fixtures = their navy + gold flyer). Navy and porcelain sections joined by moving waterline seams with a gold edge.
- **Signature element:** canvas tile wall in the hero and the closing section. Tiles catch the light as a three-sine swell passes, bulge slightly, get shoved and carried by mouse or finger and spring back with a wobble; taps and fast swipes send ripple rings; water beads hang, slide down, get pushed aside, and fast swipes shed new ones. Their photos sit in the wall as gold-framed tiles that ride the same water. Gallery photos and the desktop feature photo bob and dodge the pointer.
- **Sections:** hero (logo, "Results you can be proud of." — their words, pitch, Text + Call, three checks) → gold price plaque (their published bathroom price) → five services, each row one tap to a pre-filled text (small plain arrow cue), with their published bathroom price as plain, non-clickable type after the list (beside it on desktop) → recent work (6 photos) → how it works → close (logo, their own quote, area, Text + Call) → footer with "Demo one-pager — free sample."
- **Contact:** every text link is `sms:+16096495069?&body=…` with a per-service message (decoded and checked); call links `tel:+16096495069`. Sticky Text/Call dock on phones once the hero buttons scroll away (hides again at the closing buttons). Desktop shows the number on the text button.
- **Tunables:** `TUNE` at the top of the script (tile size, swell speed/amp, push radius, stiffness, damping, ripple, bead counts, seam speed). One CSS section per block.
- **Weight:** 370 KB single file; photos are WebP base64 in `<script type="text/plain">` blocks at the end, assigned lazily; the hero wall has a CSS tile fallback before JS runs. Processed crops are also in `assets/`.

## Assumptions I made
- **Price:** the brief's OCR said "FULL RENOVATION"; the full-res flyer clearly reads "FULL BATHROOM RENOVATION $7,000 - $10,000 (LABOR ONLY)". Used that. Confirm it's current before sending.
- **Service one-liners are inferred** from the photos and their caption, kept minimal after review: bathrooms "tile, walk-in showers, tubs, niches and vanities" (all visible in photos); decks "Decks, stairs and railings" (stairs photo); flooring "New floors, installed and finished"; painting "Painting with attention to detail" (their phrase); repairs "and home upgrades, big or small" ("home upgrades" is theirs).
- **Gallery:** no captions (Ellie's call); alt text describes each photo. Kitchens and the sunroom floor are their posted work but kitchens aren't on their service list.
- **"I" voice:** the closing quote is their caption, lightly cased. The quote byline is the company because the owner's name is unknown.
- **Area:** kept to their flyer wording, "South Jersey and surrounding areas". BBB's Toms River street address is not on the page (could be a home address).
- **Phone:** flyer number only. BBB's (848) 226-6564 is not used.
- **Colors:** navy #0f2140 sampled near their flyer's navy; gold #d6aa4e from the logo; tile cobalt from their shower photo.
- **Type:** system font stack per house style (Impeccable's craft floor prefers a sourced display face; house style wins).
- **Unattended:** Impeccable's interactive world-picker was skipped (pitch-site runs unattended); the world was chosen from the brief.

## Placeholders and gaps
- Photos: Ellie supplied sharper screenshots for five of the six (cobalt shower, marble shower with tub, white marble shower, wood-look niche, navy kitchen), exported at 720×540 or native size. Two sunroom screenshots (herringbone brick floor) are shown at native size as full-width panoramas (only the PIC·COLLAGE strip trimmed off the bottom, no zoom); forcing them into 4:3 had blurred them. Gallery order: three showers, then wood niche + navy kitchen larger, then the two sunroom panoramas. The stairs and stove photos were dropped.
- No before/after pairs, no reviews, no hours, no email, no owner name: nothing about them appears on the page.
- `og:image` / `og:url` point at the GitHub Pages URL (`assets/og.jpg`, 1200×630 hero capture). Update them if the site moves to its own domain.
- The Facebook link uses the profile id (page info was restricted to Muse); check it opens the right page.

## Questions for the owner
- Is the $7,000–$10,000 labor-only bathroom price still current? Anything to say about materials?
- Owner's first name (for the quote byline and "text Mike" style buttons)?
- Full-size photos of these jobs, and any before/after pairs (bathrooms especially)?
- Do kitchens count as a service? Any towns you most want to work in?
- Hours / best times to text? License number to show?
- Any reviews or past clients happy to be quoted?

## Review round (Impeccable finish reviewer, once)
Applied: wall no longer rebuilds on scroll-driven resizes (FB/iOS toolbar) and the tile pattern is seeded by position; closing wall visible on phones (copy sits on a navy panel instead of a full scrim); beads spawn only where visible and have a solid body; price plaque is flat gold with "Full bathroom renovation" as its heading (no label-over-big-number); fewer repeated numbers/claims; service copy trimmed to evidence; cooler porcelain (#f3f4f6) instead of cream; gallery graph-paper ground removed and gallery bob driven by the shared swell; desktop feature photo switched to work-04.
Deferred to you: set the six gallery photos into a tile wall of their own (reviewer's preferred version); wet trails behind sliding beads; moving specular sheen across tiles; whether to cut "How it works" (reviewer says it restates the hero).

## Ideas not built (yours to pick)
- **Runner-up world:** steamed shower glass you wipe clear with a finger to reveal their finished work, with condensation beads running down. Very touchable, bathroom-first; swaps in for the tile wall in the hero.
- Other worlds considered: deck boards and wood shavings drifting in gold light; wet paint stroke you can smear; floor planks laid in a rolling wave.
- Booking form page (`book.html`) that composes the same pre-filled text, with a copy fallback.
- Before/after sliders once pairs exist (bathroom row on phones, beside the list on desktop).
- Tap a gallery photo to open it larger (worth it only with full-size photos).
- Tiles pushed hard enough could crack loose and fall (like the detailer's suds breaking free).
- Fall booking hook in the hero ("Booking fall bathroom jobs now") — Muse's note, but not in their own words, so left out.

## Not verified
- Real-device touch on iOS/Android and inside Facebook's in-app browser (checked with simulated touch events headlessly).
- Real SMS handoff with the pre-filled body on iOS and Android.
- Frame rate on older phones (phone wall is ~160 tiles + 12 beads; desktop ~420 tiles + 30 beads).
- Headless captures of the canvas at 1440×900 show the CSS fallback (known headless capture quirk); a pixel probe confirmed the canvas animates and responds.
- Impeccable's detector ran in degraded regex mode (its HTML parser modules aren't installed), so its findings undercount.
