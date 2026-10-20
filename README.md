# Shreya & Omkar: Engagement Invitation

A single-page, mobile-first digital invitation for the engagement of **Shreya & Omkar**.

- **Date:** Sunday, 27 December 2026, 11:00 AM
- **Venue:** The Purple Orchid Suites, Rabale, Navi Mumbai

The whole site lives in one file, `index.html`. There is nothing to install or build.

---

## Features

- **Envelope opening:** guests see a sealed envelope. Tapping it opens the flap, lifts out the letter, and parts the "curtains" to reveal the invitation.
- **Soft background music:** a gentle ambient tune generated in the browser (no audio file). It starts when the envelope is tapped. A "♪ Music" button in the corner pauses and resumes it.
- **Marathi blessing:** ॥ श्री गणेशाय नमः ॥ at the top of the first page.
- **Live countdown:** days, hours, minutes, and seconds until the engagement.
- **Event details:** date, time, and venue cards.
- **Google Maps button:** one tap opens the venue in Google Maps.
- **Scroll transitions:** the first page fades as you scroll, and every section's content rises into view in sequence. A bouncing arrow cues guests to scroll, and the page also scrolls on by itself a few seconds after opening (unless the guest scrolls first).
- **Light and dark mode:** follows the guest's phone setting.
- **Accessibility:** respects "reduce motion" settings (animations and auto-scroll are skipped).

---

## Project structure

```
index.html   # the complete invitation (HTML + CSS + JavaScript)
README.md    # this file
```

---

## How to edit

Open `index.html` in any text editor and search for the items below.

### Date, time, and countdown

Near the bottom of the file, find the `CONFIG` block:

```js
var CONFIG = {
  dateISO: "2026-12-27T11:00:00+05:30",   // drives the countdown (IST)
  dateText: "Sunday, 27 December 2026",   // shown on the first page and details card
  timeText: "11:00 AM"                    // shown on the details card
};
```

Change all three together. `dateISO` uses the format `YYYY-MM-DDTHH:MM:SS+05:30`.

### Names

Search for `Shreya` and update every place it appears: the envelope letter, the first-page heading, the intro card, the footer, the `<title>`, and the meta description.

### Venue and Google Maps link

- Venue text: search for `The Purple Orchid Suites` (details card and map card).
- Map button: search for `maps.app.goo.gl` and replace the link with your own Google Maps share link.

### Colours

Edit the variables at the top of the `<style>` block:

```css
--wine: #651d2b;
--wine-dark: #3e101a;
--gold: #caa65b;
--gold-light: #f0d99b;
```

Dark-mode colours are in the two `dark` blocks just below.

### Music

The tune is a slow chord loop (C, Am, F, G) in the `Music` section of the script. To change the mood, edit the `chords` array. Lower the `.8` in `master.gain` to make it quieter.

To use a real song instead, add an `<audio>` element and replace the `Music` code with `audio.play()` and `audio.pause()` calls. Keep the file small so the page loads quickly.

### Timing of the opening animation

In the envelope click handler, the two `setTimeout` values (`1500` and `3000`) control when the curtains part and when the cover is removed. The `4500` controls the delay before the automatic scroll.

---

## Hosting

Any static host works. Upload `index.html` to one of these:

- **Vercel / Netlify:** drag and drop the folder, or connect a Git repository.
- **GitHub Pages:** push to a repo and enable Pages.
- **Claude artifact:** if published from Claude, use the Share option to get a link for guests.

Share the final link on WhatsApp. Guests only need to tap it.

---

## Notes

- Fonts (Cormorant Garamond, DM Sans, Tiro Devanagari Marathi) load from Google Fonts. Without internet, the page falls back to the system serif and sans-serif fonts.
- Browsers do not allow sound to start on their own, which is why the music begins on the envelope tap.
- The countdown shows zeros once the date has passed.
- The page uses no images, so it loads fast even on slow connections.

---

Made with love. 💍
