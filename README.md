# Tools Hub

Deployment and release instructions for [https://fastshoes.co.za/jithin/tools/](https://fastshoes.co.za/jithin/tools/).

---

## 🚀 Deployment Overview

- **CI**: Runs Prettier formatting + internal link check (non-blocking).
- **Deploy**: Runs after CI succeeds and uploads via FTP to `/public_html/jithin/tools/`.
- **Secrets** (set under **Repo → Settings → Secrets and variables → Actions**):
  - `FTP_SERVER = fastshoes.co.za`
  - `FTP_USERNAME`
  - `FTP_PASSWORD`
  - `FTP_REMOTE_DIR = public_html/jithin/tools/` _(must end with `/`)_

🔒 Upload excludes: `.github`, `.git*`, `node_modules`, `README.md`, `CHANGELOG.md`, `LICENSE`.

---

## 🛠 Adding a New Tool/Page

### 1. Create the HTML page

- Add a file like `your-tool-name.html`.

Include a back button at the bottom:

```html
<a href="index.html" class="cta-btn">Go Back to Home</a>
```

Keep heading/title consistent:

```html
<title>Your Tool Name</title>
<h1>Your Tool Name</h1>
```

---

### 2. Link it on the home page

Open `index.html` and add a link:

```html
<li><a href="your-tool-name.html">Your Tool Name</a></li>
```

---

## 📦 Deploying

## 🚀 Deploying

1. Format your changes with Prettier:

```bash
npx prettier --write .
```

2. Commit your changes:

```bash
git add .
git commit -m "feat: add your-tool-name"
git push origin main
```

3. GitHub Actions will:

   - Run CI checks.
   - Deploy to the FTP server if checks pass.

4. Verify live at: [https://fastshoes.co.za/jithin/tools/](https://fastshoes.co.za/jithin/tools/).

---

## 📝 Notes

- CI must pass before deployment triggers.
- If you only want to test the pipeline, enable:
  ```yaml
  dry-run: true
  ```
  in `.github/workflows/deploy-ftp.yml`.

---

✅ That’s it — just push to `main`, and your tool will be live!
