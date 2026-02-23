# Academic Website — Ulrich Laitenberger

Built with [Hugo](https://gohugo.io/) using Pascal Michaillat's [minimalist academic template](https://github.com/pmichaillat/hugo-website) (PaperMod theme).

## Quick Start (one-time setup)

### 1. Install Hugo

**Mac:**
```bash
brew install hugo
```

**Windows:**
```bash
choco install hugo-extended
```

**Linux:**
```bash
snap install hugo
```

Verify: `hugo version` (needs v0.147+)

### 2. Create your repository

1. Go to https://github.com/pmichaillat/hugo-website
2. Click **"Use this template" → "Create a new repository"**
3. Name it `ulrich-laitenberger.github.io` (or any name)
4. Clone it to your machine:
   ```bash
   git clone https://github.com/YOUR_USERNAME/YOUR_REPO.git
   cd YOUR_REPO
   ```

### 3. Replace content with your files

Copy the files from this package into your cloned repo, replacing the template's defaults:

```
config.yml              → replace the template's config.yml
content/papers/_index.md    → replace content/papers/_index.md  
content/research.md         → add to content/
content/teaching/_index.md  → replace or create content/teaching/_index.md
content/talks/_index.md     → replace or create content/talks/_index.md
content/expertises/_index.md → replace or create content/expertises/_index.md
```

Also:
- Put your photo as `static/picture.jpeg`
- Put your CV as `static/cv.pdf`

### 4. Preview locally

```bash
hugo server
```

Open http://localhost:1313 — the site auto-refreshes as you edit.

### 5. Deploy

```bash
git add .
git commit -m "Initial site"
git push
```

Go to GitHub → Settings → Pages → Source: **GitHub Actions**.
GitHub will auto-build and deploy your site.

### 6. Custom domain (optional)

In GitHub: Settings → Pages → Custom domain → `ulrich-laitenberger.com`

At your domain registrar, create DNS records:
- **A records:** `185.199.108.153`, `185.199.109.153`, `185.199.110.153`, `185.199.111.153`
- **CNAME:** `www` → `YOUR_USERNAME.github.io`

---

## Day-to-day workflow

Your entire workflow for updating the site:

1. **Edit a Markdown file** (e.g., `content/papers/_index.md`)
2. **Preview:** `hugo server` → check at localhost:1313
3. **Push:** `git add . && git commit -m "update" && git push`
4. **Done.** GitHub Actions builds and deploys automatically.

No HTML editing. No build tools. Just Markdown + git push.

---

## File structure

```
config.yml                   ← Site configuration (title, menu, social links)
content/
  papers/_index.md           ← Publications (all 3 categories)
  research.md                ← Working papers, WIP, PhD supervision
  teaching/_index.md         ← All teaching across institutions
  talks/_index.md            ← Conference talks by year
  expertises/_index.md       ← Policy reports
static/
  picture.jpeg               ← Your profile photo
  cv.pdf                     ← Your CV (linked from homepage)
```

## Adding new content

**New publication?** Edit `content/papers/_index.md`, add a new entry in the relevant section.

**New talk?** Edit `content/talks/_index.md`, add a bullet point under the right year.

**New working paper?** Edit `content/research.md`, add under "Working Papers Under Review."

**New course?** Edit `content/teaching/_index.md`, add a row to the relevant table.

Everything is plain Markdown — no templates, no front-matter juggling, no YAML arrays.
