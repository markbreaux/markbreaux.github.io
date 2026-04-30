# Portfolio Site — Setup Guide

A personal portfolio site built with [Hugo](https://gohugo.io/) and deployed to GitHub Pages.

---

## Prerequisites

Install Hugo (Extended version) on Windows:

```powershell
winget install Hugo.Hugo.Extended
```

Verify the install:

```powershell
hugo version
```

---

## Local Development

Run the site locally with live reload:

```powershell
hugo server -D
```

Open your browser to `http://localhost:1313`

The `-D` flag includes draft content. Remove it to preview only published content.

---

## Install the Theme

This site uses [hugo-profile](https://github.com/gurusabarish/hugo-profile). Install it as a Git submodule:

```powershell
git init
git submodule add https://github.com/gurusabarish/hugo-profile themes/hugo-profile
```

If you clone this repo on a new machine, restore the submodule with:

```powershell
git submodule update --init --recursive
```

---

## File Structure

```
portfolio-site/
├── .github/
│   └── workflows/
│       └── hugo.yml          # GitHub Actions — auto-deploys on push to main
├── content/
│   ├── resume.md             # Resume page
│   └── portfolio/
│       └── _index.md         # Portfolio/case studies landing page
├── static/
│   └── images/               # Add headshot.jpg or other images here
├── themes/
│   └── hugo-profile/         # Theme (installed as git submodule)
└── hugo.toml                 # Site configuration — start here for customizations
```

---

## Deploying to GitHub Pages

### First-time setup

1. Create a new GitHub repository named `mbreaux622.github.io`
2. Push this project to the `main` branch of that repo
3. In GitHub: go to **Settings → Pages → Source** and select **GitHub Actions**

That's it. Every push to `main` triggers the workflow and deploys the site automatically.

### Custom domain (optional)

1. Add a `CNAME` file to the `/static/` folder containing your domain, e.g.: `markbreaux.com`
2. Configure your DNS provider to point to `mbreaux622.github.io`
3. Enable HTTPS in **Settings → Pages**

---

## Customization Checklist

Before going live, update the following in `hugo.toml`:

- [ ] `baseURL` — replace with your actual GitHub Pages URL or custom domain
- [ ] `[YOUR-GITHUB-USERNAME]` — in baseURL and social links
- [ ] `[YOUR-LINKEDIN-HANDLE]` — LinkedIn profile URL
- [ ] `[YOUR-EMAIL]` — contact email
- [ ] Headshot — add `headshot.jpg` to `/static/images/` and uncomment the image lines in `hugo.toml`

And in `content/resume.md`:

- [ ] City, State
- [ ] Phone, Email, LinkedIn URL
- [ ] Education section

---

## Adding a Case Study

1. Create a new file: `content/portfolio/case-study-name.md`
2. Use this front matter:

```markdown
---
title: "Your Case Study Title"
date: 2026-04-29
draft: false
summary: "One sentence description for the portfolio listing."
---

Your case study content here.
```

3. In `hugo.toml`, uncomment the `url` line for the matching project card and update it to match your filename.

---

## Useful Hugo Commands

| Command | What it does |
|---|---|
| `hugo server -D` | Run locally with drafts |
| `hugo` | Build the site into `/public` |
| `hugo new content/portfolio/my-case-study.md` | Create a new content file |
