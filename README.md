# Academic Website — Ulrich Laitenberger

Custom Hugo site with the same editorial design (Newsreader + DM Sans typography, cream/ink color scheme) but fully editable via Markdown.

## Setup (one time)

### 1. Install Hugo

```bash
# Mac
brew install hugo

# Windows
choco install hugo-extended

# Linux
snap install hugo
```

### 2. Create GitHub repository

Create a new repository on GitHub (e.g., `ulrich-laitenberger.github.io`), clone it, and copy all files from this package into it.

### 3. Add your files

- Put your photo as `static/unnamed.jpg`
- Put your CV as `static/cv.pdf`
- (Optional) add a favicon as `static/favicon.ico`

### 4. Preview locally

```bash
hugo server
```

Open http://localhost:1313

### 5. Deploy

```bash
git add .
git commit -m "Initial site"
git push
```

Then go to GitHub → Settings → Pages → Source: **GitHub Actions**.

---

## Day-to-day workflow

```
1. Edit a .md file in content/
2. Preview: hugo server
3. Push: git add . && git commit -m "update" && git push
4. Done — GitHub builds and deploys automatically
```

---

## File structure

```
config.yml                ← Title, bio, social links, affiliations, nav menu
content/
  _index.md               ← Homepage (mostly empty, content comes from config + sections)
  publications.md          ← All publications (3 categories)
  research.md              ← Working papers, WIP, PhD supervision
  teaching.md              ← Courses by institution
  talks.md                 ← Talks by year
  expertises.md            ← Policy reports
layouts/                   ← HTML templates (you shouldn't need to touch these)
assets/css/style.css       ← Styling (edit to change colors/fonts)
static/
  unnamed.jpg              ← Your profile photo
  cv.pdf                   ← Your CV
.github/workflows/hugo.yml ← Auto-deploy config
```

## How to edit content

All content is in **plain Markdown** in the `content/` folder. Examples:

**Add a new publication:** open `content/publications.md`, add:
```markdown
---

**[Paper Title](https://doi.org/...)**
*Journal Name*, 2026. With Coauthor Name.
[[WP](https://link)] [[Slides](https://link)]
```

**Add a new talk:** open `content/talks.md`, add a bullet under the year:
```markdown
- June 5: [Conference Name](https://link), City
```

**Add a new working paper:** open `content/research.md`, add:
```markdown
---

**Paper Title**
With [Coauthor](https://link). Month 2026. Under Review.
```

**Update your bio:** edit the `bio` field in `config.yml`.

**Change colors:** edit `assets/css/style.css`, modify the `:root` variables.
