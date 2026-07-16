# LeadWell Company Website

Static site — plain HTML/CSS/JS, no build step required.

## File structure
```
index.html          Home
about.html           About
services.html        Services
blog.html             Blog
contact.html          Contact (working Netlify form)
assets/style.css       Shared styles
assets/script.js        Shared behavior (nav, animations, form)
assets/images/          Photos
```

## 1. Push to GitHub

From inside this folder:

```bash
git init
git add .
git commit -m "Initial site"
gh repo create leadwell-company-site --private --source=. --push
```

(No GitHub CLI? Create an empty repo at github.com/new first, then:)

```bash
git init
git add .
git commit -m "Initial site"
git branch -M main
git remote add origin https://github.com/YOUR-USERNAME/leadwell-company-site.git
git push -u origin main
```

## 2. Deploy on Netlify

1. Go to app.netlify.com → **Add new site → Import an existing project**
2. Connect your GitHub account, pick this repo
3. Build settings: leave blank (no build command, publish directory = `/`)
4. Click **Deploy**

Your site goes live at a random `*.netlify.app` URL immediately.

## 3. Point your domain

In Netlify: **Site settings → Domain management → Add a custom domain** → enter `leadwellcompany.com`.
Netlify will show you the exact DNS records to add. You'll update these wherever leadwellcompany.com is currently managed (likely inside Lovable's domain settings, or your registrar if you bought it elsewhere).

## 4. The contact form

`contact.html` is already wired for **Netlify Forms** — no backend needed. Once deployed, submissions will appear in Netlify under **Forms**, and you can set up email notifications there.

## Still needs you
- Swap the 3 placeholder Blog story cards for real titles/excerpts/Substack links
- Add your real Substack URL to the "Subscribe to The Career Reset" buttons (currently `#`)
- Confirm ICF-PCC vs ACC coaching credential (see chat)
- Confirm Newsweek vs Choice Coaching Magazine in publications (see chat)
