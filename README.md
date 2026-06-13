# Tarun A — Personal Portfolio 🚀

A modern, responsive, single-page portfolio website built with plain **HTML, CSS & JavaScript** — no build step required. Ready to deploy to **GitHub Pages** at `tarunattuluri19.github.io`.

![Made with HTML](https://img.shields.io/badge/HTML5-E34F26?logo=html5&logoColor=white)
![Made with CSS](https://img.shields.io/badge/CSS3-1572B6?logo=css3&logoColor=white)
![Made with JS](https://img.shields.io/badge/JavaScript-F7DF1E?logo=javascript&logoColor=black)

## ✨ Features

- 🌗 **Dark / Light mode** with saved preference
- 📱 Fully **responsive** (mobile menu, fluid typography)
- ⌨️ Animated **typed text** + scroll-reveal animations
- 🧭 Sticky navbar with **active section highlighting**
- 🎨 Modern gradient theme, animated background blobs, 3D code card
- ⚡ Zero dependencies, zero build — just static files

## 📁 Structure

```
portfolio/
├── index.html      # The ENTIRE website (HTML + CSS + JS all in one file)
├── README.md       # This file — notes only, NOT the website
└── .nojekyll       # Tells GitHub Pages to serve files as-is
```

> ⚠️ The website is **`index.html`**. Open that in a browser. `README.md` is just documentation — never paste website code into it.

## 🖥️ Run locally

Just open `index.html` in your browser. For a local server (recommended so everything works):

```powershell
# From inside the portfolio folder
python -m http.server 5500
# then visit http://localhost:5500
```

Or use the **VS Code "Live Server"** extension → right-click `index.html` → *Open with Live Server*.

## 🚀 Deploy to GitHub Pages (username.github.io)

To make this your main profile site at **https://tarunattuluri19.github.io**:

1. **Create a new repo** on GitHub named **exactly**:
   ```
   tarunattuluri19.github.io
   ```
2. **Push these files to the repo root** (note: the site files must be at the root, not inside a `portfolio/` subfolder):
   ```powershell
   # From inside the portfolio folder
   git init
   git add .
   git commit -m "Initial portfolio site"
   git branch -M main
   git remote add origin https://github.com/tarunattuluri19/tarunattuluri19.github.io.git
   git push -u origin main
   ```
3. In the repo, go to **Settings → Pages** → set **Source** to `Deploy from a branch`, **Branch** = `main` / `root`, then **Save**.
4. Wait ~1 minute, then visit **https://tarunattuluri19.github.io** 🎉

> 💡 If you instead want this in a *project* repo (e.g. `my-portfolio`), it will be served at `https://tarunattuluri19.github.io/my-portfolio/` — in **Settings → Pages**, just point it at the branch the same way.

## 🎨 Customize

Everything lives in `index.html`:

| What | Where in `index.html` |
|------|-------|
| Name, bio, links | the HTML in the `<body>` |
| Email address | search `tarun@example.com` |
| Projects | the `projects__grid` section |
| Typed phrases | `phrases` array in the `<script>` block |
| Colors / theme | CSS variables in `:root` inside the `<style>` block |

---

Built with ☕ & ❤️ by **Tarun A** · [GitHub](https://github.com/tarunattuluri19) · [Blog](https://tarunattuluri.netlify.app/)
