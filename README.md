# Bloom and Butter — GHL AI Studio package

This is a repository-ready Vite static site. The full page is contained in `index.html`; there are no local image assets or secrets to configure.

## Upload to the repository created by AI Studio

1. In HighLevel AI Studio, create a **Landing Page** project.
2. Open **More → Git → GitHub**, connect GitHub, and let AI Studio create its private repository on the `main` branch.
3. Clone that new repository to your computer.
4. Make a backup branch before replacing the generated starter:

   ```bash
   git switch -c ai-studio-original
   git push -u origin ai-studio-original
   git switch main
   ```

5. Delete the generated project files from the local checkout, but keep the `.git` directory.
6. Copy the **contents** of this folder into the repository root. `package.json` and `index.html` must sit at the top level, not inside an extra folder.
7. Commit and push:

   ```bash
   git add -A
   git commit -m "Import Bloom and Butter landing page"
   git push origin main
   ```

8. Return to **More → Git** in AI Studio. With Automatic Pull enabled, wait for the commit to appear; otherwise click **Pull now**.
9. When the preview finishes building, click **Refresh preview**, review it, then publish when ready.

## Local check (optional)

With Node.js installed:

```bash
npm install
npm run dev
```

For a production build:

```bash
npm run build
```

The generated site will be in `dist/`.

## Before publishing for a real business

The page is still a template and contains placeholders such as `[phone]`, `[email]`, `[street]`, order/map links, social links, and `yourdomain.com`. Replace them in `index.html` or ask AI Studio to update them after import.

Do not paste API keys or credentials into `index.html`. Use AI Studio Secrets for any future server-side integrations.
