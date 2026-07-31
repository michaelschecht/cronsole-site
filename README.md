<a id="readme-top"></a>

<h1 align="center">Cronsole — Landing Site</h1>

<p align="center">
  <em>The public front door for Cronsole — one pane of glass for every scheduled task.<br>A single, self-contained static page served on GitHub Pages.</em>
</p>

<p align="center">
  <a href="https://cronsole.mikesailab.com"><strong>Visit the site »</strong></a>
</p>

<p align="center">
  <a href="https://cronsole.mikesailab.com">Live Site</a>
  ·
  <a href="https://github.com/michaelschecht/cronsole-site/issues">Report Bug</a>
  ·
  <a href="https://github.com/michaelschecht/cronsole-site/issues">Request Feature</a>
</p>

<p align="center">
  <a href="https://cronsole.mikesailab.com"><img src="https://img.shields.io/badge/Live_Site-cronsole.mikesailab.com-2ea44f?style=for-the-badge&logo=githubpages&logoColor=white" alt="Live at cronsole.mikesailab.com"></a>
  <img src="https://img.shields.io/badge/status-Live-2ea44f?style=for-the-badge" alt="Status: Live">
  <a href="https://mikesailab.com/cronsole-registry/"><img src="https://img.shields.io/badge/browse-TEMPLATES-8B5CF6?style=for-the-badge" alt="Browse templates"></a>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/HTML5-static-E34F26?style=flat-square&logo=html5&logoColor=white" alt="HTML5">
  <img src="https://img.shields.io/badge/no_build-vanilla_JS-F7DF1E?style=flat-square&logo=javascript&logoColor=black" alt="Vanilla JS, no build step">
  <img src="https://img.shields.io/badge/GitHub_Pages-served-222?style=flat-square&logo=githubpages&logoColor=white" alt="Served via GitHub Pages">
  <img src="https://img.shields.io/badge/license-Apache_2.0-6B7280?style=flat-square" alt="Apache-2.0">
</p>

---

## 🧩 What this is

This repository serves Cronsole's **public front door** — the site for
[Cronsole](https://github.com/michaelschecht/cronsole), a local-first control plane for scheduled
tasks across Windows Task Scheduler, Claude Code / Codex routines, AI-agent jobs, and more.
It doubles as the **template gallery** (see the maintenance note below).

It is a **single self-contained `index.html`** (inline CSS + vanilla JS — no build step, no
external CDN or fonts), served as static files over **GitHub Pages** at:

> **`https://cronsole.mikesailab.com`**

The page pitches Cronsole and points visitors to the three public pieces of the project (below).

## 🚀 The Cronsole project

| Piece | What it is |
|:---|:---|
| [**🧠 Cronsole app**](https://github.com/michaelschecht/cronsole) | The full stack — React dashboard, Node/Postgres backend, the .NET Windows agent, and the MCP server. *(Private during build; public at launch.)* |
| [**🗃️ Template registry**](https://github.com/michaelschecht/cronsole-registry) | The public, versioned catalog — `index.json` + one JSON file per template, content-addressed with sha256 and served over a CDN. |
| [**🖼️ Template gallery**](https://mikesailab.com/cronsole-registry/) | Browse, filter, and import the whole template catalog into your local Cronsole. |

## 📦 What's inside

| File | What it holds |
|:---|:---|
| [**`index.html`**](index.html) | The entire page — markup, inline styles, and the theme-toggle script. Self-contained and offline-capable. |
| `CNAME` | The custom domain (`cronsole.mikesailab.com`). GitHub Pages reads this on build. |
| `.nojekyll` | Tells GitHub Pages to serve the files raw (no Jekyll processing). |

## 🛠️ How this repo is maintained

This repo is a **published mirror**. The source of truth is `registry-site/index.html` in the
Cronsole app repo; a publish script (`scripts/publish-frontdoor.ps1`) copies the page here and
pushes, and GitHub Pages rebuilds within about a minute.

> [!IMPORTANT]
> **This is the same page as the template gallery, published to a second host.** The standalone
> marketing landing page was retired on 2026-07-28 and the gallery absorbed its product pitch,
> quick start, and project links into its Home view. `publish-frontdoor.ps1` copies
> `registry-site/index.html` here; `publish-registry.ps1` copies the identical file to
> [`cronsole-registry`](https://github.com/michaelschecht/cronsole-registry). Run **both**, or the
> two hosts silently drift.

> [!NOTE]
> Content here is generated from the source folder — an edit to `index.html` in this repo would
> be overwritten on the next publish. This repo *does* own its own `README.md`, so this file is
> safe from the publish step. To change the page, edit it at the source and re-publish.

> [!TIP]
> The page uses only **relative** asset references and links out to absolute URLs, so it renders
> identically whether it's served from the custom domain or a local static server.

## 🔗 Links

| | |
|:---|:---|
| [**Live site**](https://cronsole.mikesailab.com) | The front door this repo serves. |
| [**Cronsole app**](https://github.com/michaelschecht/cronsole) | The application the site is about. |
| [**Template gallery**](https://mikesailab.com/cronsole-registry/) | Browse and import automation templates. |
| [**Issues**](https://github.com/michaelschecht/cronsole-site/issues) | Report a problem with the site. |

---

<p align="center">
  <sub>Landing site for <a href="https://github.com/michaelschecht/cronsole">Cronsole</a> · served via GitHub Pages · Apache-2.0</sub>
</p>

<p align="right">(<a href="#readme-top">back to top</a>)</p>
