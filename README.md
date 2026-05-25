# Personal Website — Björn Robert Holmgren

## 1. Filling in Your URLs

Open `config.js` and paste your real URLs as string values:

```js
window.SITE_CONFIG = {
  links: {
    linkedin: "https://linkedin.com/in/your-handle",  // your LinkedIn profile
    github:   "https://github.com/your-handle",       // your GitHub profile
  },
  projects: {
    bucketlist: {
      liveUrl: "https://your-bucketlist-app.com"      // live BucketList URL
    },
    tennisai: {
      githubUrl: "https://github.com/your-handle/tennisai"  // TennisAI repo
    }
  }
}
```

Leaving a value as an empty string `""` hides that button automatically — no broken links.

## 2. Running Locally

**Option A** (usually works): Open `index.html` directly in your browser.

**Option B** (if you see script loading issues): Run a local server from the project folder:

```bash
python3 -m http.server 8080
```

Then open `http://localhost:8080` in your browser.

## 3. Deploying to GitHub Pages

1. Create a GitHub repository (name it `your-username.github.io` for a root URL, or any name for a project-page URL like `your-username.github.io/repo-name`)
2. Push all four files to the `main` branch:
   ```bash
   git init
   git add .
   git commit -m "Initial site"
   git remote add origin https://github.com/your-username/your-repo.git
   git push -u origin main
   ```
3. In the repo on GitHub, go to **Settings → Pages**
4. Under **Source**, select **Deploy from a branch**, choose `main`, folder `/` (root), and click **Save**
5. Your site will be live at `https://your-username.github.io` (or the project-page URL) within 60–90 seconds
6. GitHub Pages provides HTTPS automatically — no extra configuration needed
