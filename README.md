# Project Travel Journal

<!-- PROJECT SHIELDS -->
<p align="center">
  <a href="[contributors-url]"><img src="[contributors-shield]" alt="Contributors"></a>
  <a href="[forks-url]"><img src="[forks-shield]" alt="Forks"></a>
  <a href="[stars-url]"><img src="[stars-shield]" alt="Stargazers"></a>
  <a href="[issues-url]"><img src="[issues-shield]" alt="Issues"></a>
  <a href="[demo-url]"><img src="[demo-shield]" alt="Demo Status"></a>
  <a href="[linkedin-url]"><img src="[linkedin-shield]" alt="LinkedIn"></a>
</p>

<p align="center">
  <a href="https://github.com/codingmaniac227/Project-Travel-Journal">
    <img src="logo.png" alt="Logo" width="90" height="90" style="border-radius:50%">
  </a>
</p>

<p align="center">
  A clean, responsive travel journal built with React + Vite.
  <br />
  <a href="https://github.com/codingmaniac227/Project-Travel-Journal"><strong>Explore the repo »</strong></a>
  <br />
  <br />
  <a href="https://travel-journal-demo.netlify.app">View Demo</a>
  ·
  <a href="https://github.com/codingmaniac227/Project-Travel-Journal/issues">Report Bug</a>
  ·
  <a href="https://github.com/codingmaniac227/Project-Travel-Journal/issues">Request Feature</a>
</p>

<p align="center">
  <a href="https://react.dev/"><img src="https://img.shields.io/badge/React-20232A?style=for-the-badge&logo=react&logoColor=61DAFB" alt="React"></a>
  <a href="https://vitejs.dev/"><img src="https://img.shields.io/badge/Vite-646CFF?style=for-the-badge&logo=vite&logoColor=FFD62E" alt="Vite"></a>
</p>

---

## 📸 Screenshot

![App Screenshot](screenshot.png)

---

## ✨ Features

- Three journal entries (Japan – Mount Fuji, Australia – Sydney Opera House, Norway – Geirangerfjord)
- Semantic, accessible markup (headings, links, and readable date formatting)
- Responsive layout with clean breakpoints for tablet/phone
- Image optimization via Vite asset handling
- Simple, minimal CSS with a focus on readability

---

## 🚀 Tech Stack

- **Frontend:** React 19 + Vite
- **Styling:** Plain CSS (mobile-friendly media queries)
- **Tooling:** ESLint (optional)

---

## 🗂 Project Structure

```
project-root/
├─ public/
│  └─ (static files if needed)
├─ src/
│  ├─ assets/
│  │  ├─ japan-img.png
│  │  ├─ australia-img.png
│  │  ├─ norway-img.png
│  │  └─ location-icon.svg
│  ├─ components/
│  │  ├─ Header.jsx
│  │  └─ Entry.jsx          ← renders the three cards
│  ├─ App.jsx
│  ├─ App.css               ← core styles & media queries
│  ├─ index.css
│  └─ main.jsx
├─ screenshot.png
├─ logo.png
└─ package.json
```

> **Note on assets:** images are imported from `src/assets` so that Vite can fingerprint/optimize them at build time.

**Example import:**

```jsx
import japanImg from '../assets/japan-img.png'
<img src={japanImg} alt="Mount Fuji" />
```

---

## 🧭 Live Demo

- **Netlify:** https://travel-journal-demo.netlify.app

---

## 🛠 Getting Started

### Prerequisites
- Node.js 18+ (recommended)

### Install & Run
```bash
# install
npm install

# start dev server
npm run dev

# build for production
npm run build

# preview production build locally
npm run preview
```

---

## 📐 Responsive Behavior

- **Desktop:** two-column card (image + content), capped text width for readability.
- **≤ 768px (tablet):** cards stack vertically; images shrink.
- **≤ 480px (phone):** tighter padding & font sizes, smaller images.

Media queries live in `App.css`.

---

## 🔜 What’s Next: Moving to Data‑Driven React

This project was intentionally completed **right before** a data‑driven refactor. Building the static version first helps you:

- **Lock in markup & styles** before adding abstractions.
- **Identify reusable patterns** (card layout, header row, dates, link styles).
- **Reduce complexity** when you introduce a reusable `<EntryCard />` and render from an array.

**Why it matters:** after the refactor, adding 300 entries becomes a data task, not a markup task.

**Sketch of the next step:**
```jsx
// entries.js
export const entries = [
  { country: 'JAPAN', title: 'Mount Fuji', start: '2023-01-12', end: '2023-01-24', ... },
  // ...
]

// Entry.jsx
{entries.map(e => <EntryCard key={e.title} {...e} />)}
```

---

## ♿ Accessibility Notes

- Meaningful `alt` text for photos; decorative icons use `alt=""`.
- Proper heading order (`h1` in the header, `h2` per entry).
- Links are descriptive (“View on Google Maps”).

---

## 🧹 Scripts

```json
{
  "dev": "vite",
  "build": "vite build",
  "preview": "vite preview",
  "lint": "eslint ."
}
```

---

## 🤝 Contributing

Open issues and PRs are welcome!  
https://github.com/codingmaniac227/Project-Travel-Journal/issues

---

## 📄 License

MIT — feel free to reuse with attribution.

<!-- MARKDOWN LINKS & IMAGES -->
[contributors-shield]: https://img.shields.io/github/contributors/codingmaniac227/Project-Travel-Journal?style=for-the-badge
[contributors-url]: https://github.com/codingmaniac227/Project-Travel-Journal/graphs/contributors
[forks-shield]: https://img.shields.io/github/forks/codingmaniac227/Project-Travel-Journal?style=for-the-badge
[forks-url]: https://github.com/codingmaniac227/Project-Travel-Journal/network/members
[stars-shield]: https://img.shields.io/github/stars/codingmaniac227/Project-Travel-Journal?style=for-the-badge
[stars-url]: https://github.com/codingmaniac227/Project-Travel-Journal/stargazers
[issues-shield]: https://img.shields.io/github/issues/codingmaniac227/Project-Travel-Journal?style=for-the-badge
[issues-url]: https://github.com/codingmaniac227/Project-Travel-Journal/issues
[demo-shield]: https://img.shields.io/website?url=https%3A%2F%2Ftravel-journal-demo.netlify.app&label=demo&up_color=brightgreen&up_message=online&down_message=offline&style=for-the-badge
[demo-url]: https://travel-journal-demo.netlify.app
[linkedin-shield]: https://img.shields.io/badge/-LinkedIn-black.svg?style=for-the-badge&logo=linkedin&colorB=555
[linkedin-url]: https://www.linkedin.com/in/marquise-davis/
