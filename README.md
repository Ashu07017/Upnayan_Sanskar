# Upanayan Sanskar Mahotsav — Digital Invitation & Memories

A premium static website built as a digital invitation and cinematic memory gallery for an Upanayan Sanskar ceremony. Designed to feel personal, elegant, and celebration-worthy — no backend, no frameworks, just clean HTML, CSS, and JavaScript.

**🔗 Live Site:** [upnayan-sanskar.netlify.app](https://upnayan-sanskar.netlify.app/)

---

## ✨ Features

- **Digital Invitation Page** — Event details presented in a warm, festive layout
- **Cinematic Memories Gallery** — Photo timeline organized by day with smooth reveal animations
- **Scroll Animations** — Subtle, fluid transitions as content enters the viewport
- **Lightbox Viewer** — Full-screen image viewing with keyboard and touch support
- **Lazy Loading** — Images load only when needed, keeping the page fast
- **Background Music System** — Ambient music that respects browser autoplay policies (see [Music Behavior](#-music-behavior))
- **Fully Responsive** — Optimized for mobile, tablet, and desktop
- **Manual Photo Control** — Photos are managed directly via `<img>` tags; no upload system or CMS required

---

## 📁 Project Structure

```
upnayan-site/
│── index.html          # Digital invitation page
│── photos.html         # Memories / photo gallery page
│
├── images/
│   ├── day-1/          # Photos from Day 1
│   ├── day-2/          # Photos from Day 2
│   └── day-3/          # Photos from Day 3
│
└── audio/
    └── music.mp3       # Background music track
```

---

## 🎵 Music Behavior

The background music **does not autoplay** when the page loads.

This is intentional — modern browsers block audio from playing before a user has interacted with the page. To respect this policy and avoid silent failures or console errors, music is designed to begin only after the first user interaction (a click, scroll, or touch event).

- A **play/pause toggle button** is available on the page
- Music starts automatically on first interaction if the toggle is enabled
- No audio plays without user consent

> This is standard browser behavior, not a limitation of the site.

---

## 🖼️ How to Add Photos

There is no upload system. Photos are managed manually by editing `photos.html` directly.

**To add a photo:**

1. Place the image file inside the appropriate day folder (e.g., `images/day-2/`)
2. Open `photos.html` and add an `<img>` block in the correct section:

```html
<img
  src="images/day-2/photo-name.jpg"
  alt="Brief description"
  loading="lazy"
  class="gallery-img"
/>
```

3. To remove a photo, delete or comment out its `<img>` tag

This approach keeps everything simple, static, and fully under your control.

---

## ⚡ Performance Notes

- Images are manually optimized before being added to the project
- Lazy loading (`loading="lazy"`) is applied to all gallery images
- Videos are **not included** in the repository to keep the project size manageable
- No external JavaScript frameworks or UI libraries are used

---

## 🚀 Deployment

The site is hosted on **Netlify** via direct folder deployment (drag-and-drop or Git integration).

No build step required — the project is fully static and deploys as-is.

---

## 👤 Author

**Ashok Chaturvedi**

---

*Built with care for a meaningful family occasion.*