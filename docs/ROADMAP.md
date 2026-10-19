<h1 align="center">🗺️ Roadmap</h1>

<p align="center">
  <em>The Cronsole front door is live; what's left is tidying its public record.</em>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/now-public_release-F59E0B?style=for-the-badge" alt="Now: public release">
  <img src="https://img.shields.io/badge/stage-live_since_2026--07--14-2ea44f?style=for-the-badge" alt="Stage: live since 2026-07-14">
  <a href="../README.md"><img src="https://img.shields.io/badge/↩-repository_root-6B7280?style=for-the-badge" alt="Back to the repository root"></a>
</p>

---

Worked by hand. The page itself is not edited here: `index.html` is published from `registry-site/` in [ai-automation-tools/cronsole](https://github.com/ai-automation-tools/cronsole) by its "Publish front door" workflow, so page work belongs on that repo's roadmap. This file covers the repo and the site's hosting. **Every item above `## After public release` is a release gate.** Ticking an item adds its line to the [changelog](CHANGELOG.md) and updates any doc it made stale, in the same commit.

Markers: `- [ ]` open, `- [-]` claimed by a run in progress, `- [x]` done, `- [!]` blocked (the reason follows on the line). `small` marks an item a check verifies; `🔒 Needs Mike` marks one only Mike can do.

## 🧱 Phase 1: Landing page on Pages (done 2026-07-14)

- [x] Single self-contained `index.html` (inline CSS and vanilla JS, no build step) published to GitHub Pages — done 2026-07-14: "Add TaskHub landing page"
- [x] `.nojekyll`, so Pages serves the files raw — done 2026-07-14
- [x] House-style README front page — done 2026-07-14

## 🔁 Phase 2: The front door mirrors the gallery (done 2026-08-19)

- [x] The standalone landing page retired; the template gallery absorbed its pitch, quick start and project links, and this repo serves the same page — done 2026-07-28
- [x] Moved to `cronsole.mikesailab.com` and renamed from TaskHub to Cronsole — done 2026-07-31
- [x] Publishing automated: the cronsole repo's "Publish front door" workflow mirrors the page on every merge that touches `registry-site/`, and "Front door drift" checks both hosts daily — done 2026-08-19: per `scripts/publish-frontdoor.ps1` in the cronsole repo

## 🚦 Public release

- [x] Site live at <https://cronsole.mikesailab.com> (GitHub Pages, HTTPS enforced) — done 2026-07-14: first publish; the custom domain moved on 2026-07-31. Checked 2026-10-19: `200`, `Server: GitHub.com`
- [x] Repo public on GitHub — done by 2026-10-19 (the date it went public isn't recorded in git)
- [x] Full-history secret scan comes back clean — done 2026-10-19: `gitleaks git .`, 28 commits, no leaks
- [ ] small `LICENSE` file added: the README's badge and footer say Apache-2.0, but the repo has no licence file
- [ ] No personal email in public commit metadata: 37 author/committer entries use a personal address rather than the GitHub noreply one. Fixing it means rewriting public history 🔒 Needs Mike

## After public release

Nothing below blocks go-live.

### 📝 README accuracy

- [ ] small Point the README's Cronsole app links at `ai-automation-tools/cronsole` (it still links `michaelschecht/cronsole`, which only redirects) and drop "Private during build; public at launch": the app is public
- [ ] small Say in the README that the same workflow also publishes to the org copy, `ai-automation-tools/cronsole-site` at `cronsole.ai-automation-tools.dev`

---

<p align="center">
  <a href="../README.md">← Repository home</a> ·
  <a href="CHANGELOG.md">Changelog →</a>
</p>
