# NexaCode — IT Solutions Website

> Official website for **NexaCode**, an IT solutions company based in Hafar Al-Batin, Eastern Province, Saudi Arabia.
> Services: Website Development · Mobile Apps · E-Commerce · Custom Software

---

## 🚀 Live Site

| Environment | URL |
|---|---|
| Production | https://nexacode.sa |
| Netlify Preview | https://nexacode.netlify.app |

---

## 📁 Project Structure

```
nexacode-site/
├── index.html        ← Main landing page (all-in-one)
├── netlify.toml      ← Netlify config: headers, redirects, caching
├── _redirects        ← Netlify redirect rules (fallback)
├── robots.txt        ← Search engine crawl rules
├── sitemap.xml       ← SEO sitemap
├── .gitignore        ← Files excluded from Git
└── README.md         ← This file
```

---

## ⚙️ Local Development

No build step needed — it's a pure HTML/CSS/JS site.

**Option 1 — Open directly:**
```bash
open index.html
```

**Option 2 — Local server (recommended, avoids CORS issues):**
```bash
# Using Python
python3 -m http.server 3000

# Using Node.js
npx serve .

# Then visit: http://localhost:3000
```

---

## 📦 Git Setup (First Time)

Run these commands in your terminal:

```bash
# 1. Clone this repo (replace with your GitHub username)
git clone https://github.com/YOUR_USERNAME/nexacode-site.git
cd nexacode-site

# ── OR if starting fresh ──

# 1. Initialize a new repo
git init
git branch -M main

# 2. Add all files
git add .

# 3. First commit
git commit -m "🚀 Initial launch: NexaCode website"

# 4. Connect to GitHub (replace with your repo URL)
git remote add origin https://github.com/YOUR_USERNAME/nexacode-site.git

# 5. Push to GitHub
git push -u origin main
```

---

## 🌐 Deploy on Netlify

### First-time setup:

1. Go to **[netlify.com](https://netlify.com)** → Log in → **"Add new site"**
2. Choose **"Import an existing project"**
3. Select **GitHub** → Authorize Netlify
4. Choose your repo: `nexacode-site`
5. Build settings:
   - **Build command:** *(leave empty)*
   - **Publish directory:** `.` (a single dot)
6. Click **"Deploy site"**

✅ Your site goes live in ~30 seconds at a Netlify URL (e.g. `nexacode.netlify.app`)

---

## 🔗 Connect Your Custom Domain (nexacode.sa)

1. In Netlify → **Site settings → Domain management → Add custom domain**
2. Type `nexacode.sa` → Confirm
3. Netlify shows you DNS records to add. Go to your domain registrar and add:

| Type | Name | Value |
|---|---|---|
| `A` | `@` | `75.2.60.5` |
| `CNAME` | `www` | `nexacode.netlify.app` |

4. Wait 10–60 minutes for DNS to propagate
5. In Netlify → **"Verify DNS"** → Then **"Enable HTTPS"** (free SSL via Let's Encrypt)

---

## ✏️ Updating the Website

```bash
# 1. Edit index.html (or any file)
# 2. Stage your changes
git add .

# 3. Commit with a message
git commit -m "✏️ Update: changed service pricing"

# 4. Push to GitHub
git push origin main
```

**Netlify auto-deploys every time you push to `main`.** ⚡
Your live site updates in ~15–30 seconds automatically.

---

## 🔒 Security Features

The website includes 16 client-side security layers:

| Layer | Protection |
|---|---|
| Content Security Policy | Blocks XSS & unauthorized scripts |
| X-Frame-Options: DENY | Prevents clickjacking |
| HSTS | Forces HTTPS for 1 year |
| Referrer Policy | Limits URL leakage |
| Permissions Policy | Disables camera/mic/GPS |
| XSS Sanitizer | Escapes all dynamic content |
| CSRF Token | Per-session token for API calls |
| Bot Detection | Flags headless browsers |
| Rate Limiter | Stops click/form spam |
| Link Hardener | Auto noopener noreferrer |
| Input Validator | Validates all form fields |
| DevTools Deterrence | Detects dev tools opening |
| Right-click Protection | Disables context menu |
| Keyboard Shortcut Block | Blocks F12, Ctrl+U, etc. |
| Session Timer | Flags long-open sessions |
| Secure Fetch Wrapper | Safe API call utility |

Server-level headers are also set in `netlify.toml` for full protection.

---

## 📋 Useful Git Commands

```bash
# Check status of changes
git status

# See commit history
git log --oneline

# Undo last commit (keep changes)
git reset --soft HEAD~1

# Pull latest changes from GitHub
git pull origin main

# Create a new branch for experiments
git checkout -b feature/new-section

# Merge branch back to main
git checkout main
git merge feature/new-section

# Tag a release version
git tag -a v1.0.0 -m "Version 1.0 — Launch"
git push origin --tags
```

---

## 📞 Contact

- **Email:** hello@nexacode.sa
- **WhatsApp:** +966 50 000 0000
- **Location:** Hafar Al-Batin, Eastern Province, KSA

---

*Built with ❤️ in Saudi Arabia — © 2026 NexaCode*
