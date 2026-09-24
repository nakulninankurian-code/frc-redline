# 🏍️ FRC RedLine — Website

**Engineering The Impossible**

A high-energy, 3D racing team website built with GSAP, Lenis smooth scroll, and pure CSS.

---

## 📁 File Structure

```
website/
├── index.html              ← Main page (open this in browser)
├── css/
│   ├── main.css            ← Design system, nav, cursor, footer
│   ├── hero.css            ← Hero + ticker
│   ├── countdown.css       ← Countdown timer
│   ├── about.css           ← Build story horizontal scroll
│   ├── team.css            ← Cinematic team section
│   └── merch.css           ← Merchandise grid
├── js/
│   ├── main.js             ← Lenis, GSAP setup, nav, cursor, hero entry
│   ├── hero.js             ← Mouse parallax tilt
│   ├── ticker.js           ← F1 ticker reveal
│   ├── countdown.js        ← Live countdown timer
│   ├── about.js            ← Horizontal scroll + stat counters
│   ├── team.js             ← Team member reveal animations
│   └── merch.js            ← Product filter + reveals
└── assets/
    └── images/             ← All your team photos go here
```

---

## 🚀 How to Run

### Option 1 — Open directly (simplest)
1. Copy the entire `website/` folder to your Desktop or anywhere
2. Open `index.html` in **Google Chrome** or **Firefox**
3. Done!

> ⚠️ Some browsers block local file GSAP requests. If animations don't work, use Option 2.

### Option 2 — Live Server (recommended for development)
1. Install [VS Code](https://code.visualstudio.com/) + **Live Server** extension
2. Open the `website/` folder in VS Code
3. Right-click `index.html` → **"Open with Live Server"**
4. Browser opens at `http://127.0.0.1:5500`

### Option 3 — Deploy Free (share with the world)
- **Netlify**: Drag and drop the `website/` folder at [netlify.com/drop](https://netlify.com/drop)
- **GitHub Pages**: Push to a repo, enable GitHub Pages
- **Vercel**: Import repo at [vercel.com](https://vercel.com)

---

## ✏️ How to Customize

### Update the Race Date (Countdown)
Open `js/countdown.js` and change line 10:
```js
const TARGET_DATE = '2027-06-01T09:00:00'; // ← Change this
```

### Add Real Team Photos
Replace placeholder SVGs with real photos:
1. Add your photos to `assets/images/`
2. In `index.html`, find each `.team-member` block
3. Replace the `<div class="team-member-placeholder">...</div>` with:
```html
<img src="assets/images/your-photo.jpg" alt="Name" class="team-member-img" />
```

### Add Real Team Names
In `index.html`, find each `.team-member-info` block and replace:
- `TEAM LEAD` with the actual name
- `CAPTAIN · MECHANICAL ENGINEERING` with the real role
- Update the bio text

### Update Social Links
In `index.html`, find the footer social links:
```html
<a href="#" class="footer-social-link" ...>  ← Replace # with your URL
```

### Update Merch Prices / Items
In `index.html`, find `.merch-card` blocks to update names and prices.

### Update Stat Numbers (About section)
In `index.html`, find `.about-stat-val` elements with `data-target`:
```html
<span class="about-stat-val" data-target="600">  ← Change the target number
```

---

## 🎨 Changing Colors

All colors are CSS variables in `css/main.css`:
```css
:root {
  --red:     #CC0000;  /* Primary red */
  --red-hot: #FF2020;  /* Hover/active red */
  --chrome:  #C0C0C0;  /* Metallic silver */
  --bg:      #080808;  /* Background */
}
```

---

## 📱 Responsive
- Desktop: Full 3D parallax + horizontal scroll experience
- Tablet: Graceful layout adjustments
- Mobile: Vertical stack, no parallax (optimized for performance)

---

## 🛠️ Tech Stack

| Tool | Purpose |
|---|---|
| GSAP 3 | All animations |
| ScrollTrigger | Scroll-based animations |
| Lenis | Buttery smooth scrolling |
| Google Fonts | Barlow Condensed, Inter, DM Mono |
| Vanilla JS | No frameworks needed |

All libraries loaded from CDN — no build step required.

---

*Built for FRC RedLine Engineering Team · 2026*
