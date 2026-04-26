# Marlee & Cameron — Wedding Invitation Website

A luxury, cinematic wedding invitation built as a single deployable HTML file.
No build tools, no dependencies — pure HTML, CSS & JS.

---

## 🚀 Deploy to Vercel (3 steps)

1. **Install Vercel CLI** (if not already):
   ```
   npm install -g vercel
   ```

2. **Deploy from this folder:**
   ```
   cd wedding-site
   vercel
   ```
   Follow the prompts — choose "No" to all framework questions.

3. **Share the link** — that's it! 🎉

---

## 📁 Folder Structure

```
wedding-site/
├── index.html         ← The entire website
├── vercel.json        ← Vercel deployment config
├── public/
│   └── images/        ← Drop your photos here
│       ├── hero.jpg         (hero background — landscape, min 1920px wide)
│       ├── story1.jpg       (Our Story image 1 — portrait recommended)
│       ├── story2.jpg       (Our Story image 2 — portrait recommended)
│       ├── story3.jpg       (Our Story image 3 — portrait recommended)
│       ├── photo1.jpg       (Gallery image 1)
│       ├── photo2.jpg       (Gallery image 2)
│       ├── photo3.jpg       (Gallery image 3)
│       ├── photo4.jpg       (Gallery image 4)
│       ├── photo5.jpg       (Gallery image 5)
│       └── photo6.jpg       (Gallery image 6)
└── music/
    └── our-song.mp3   ← Optional background music
```

---

## ✏️ Customisation Guide

Open `index.html` and search for the following to edit:

### Essential Edits
| Find | Replace with |
|------|-------------|
| `28 June, 2025` | Your wedding date |
| `new Date('2025-06-28T16:00:00')` | Your actual date/time for countdown |
| `The Grand Estate & Gardens` | Your venue name |
| `123 Rosewood Lane, City, State` | Your venue address |
| `https://maps.google.com/?q=Your+Venue+Name` | Real Google Maps link |
| `May 15th` | Your RSVP deadline |

### Add Photos
In `index.html`, find the `<!-- Replace src -->` comments and swap in your image paths:

```html
<!-- Hero -->
<!-- Replace this line: -->
<div class="hero-placeholder"></div>
<!-- With: -->
<img src="/images/hero.jpg" class="hero-img" alt="Marlee and Cameron" />

<!-- Story images -->
<!-- Replace: <div class="story-img-placeholder">Add photo here</div> -->
<!-- With:    <img src="/images/story1.jpg" alt="How we met" /> -->
```

### Add Background Music
1. Place your MP3 in `/music/our-song.mp3`
2. In `index.html`, find the `<audio>` tag and uncomment:
   ```html
   <source src="/music/our-song.mp3" type="audio/mpeg" />
   ```

### Change Wedding Date (Countdown)
Find this line and update it:
```js
const weddingDate = new Date('2025-06-28T16:00:00');
```

### Add Your Story
Find the 3 story blocks and replace the placeholder text with your own.

### Edit the Schedule
Find the `#schedule` section and update times/events to match your day.

### Colors
All colors are defined as CSS variables at the top of the `<style>` block:
```css
:root {
  --cream:   #f5f0e8;   /* page background */
  --gold:    #b8955a;   /* accent color    */
  --dark:    #1a1611;   /* dark sections   */
  ...
}
```

---

## 💡 Tips
- Optimise images to JPEG, 80% quality — keeps the site fast
- Hero image: at least 1920 × 1080px landscape
- Gallery images: mix portrait + landscape for visual interest
- Music file: compress MP3 to ~128kbps to keep load fast
- RSVP form: for a real backend, connect to Netlify Forms or Formspree by adding `action="https://formspree.io/f/YOUR_ID"` to the form

---

Built with love ❤️
