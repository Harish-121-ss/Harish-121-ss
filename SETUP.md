# 🚀 Harish SS — GitHub Profile Setup

This package is designed for the special GitHub profile repository:

`Harish-121-ss/Harish-121-ss`

## 1. Create the profile repository

On GitHub, create a **public repository named exactly**:

`Harish-121-ss`

GitHub recognizes a repository with the same name as your username as your profile README repository.

## 2. Copy the files

Copy:

```text
README.md
.github/workflows/
profile/
```

into the root of the profile repository.

## 3. Add your custom opening message

The README currently contains:

```text
<!-- CUSTOM OPENING MESSAGE: Replace this line with your own message from Phase 3, option 81B. -->
```

Replace it with your exact message.

## 4. GitHub Actions permissions

Open:

`Repository → Settings → Actions → General`

Under **Workflow permissions**, allow the workflows to have:

`Read and write permissions`

The workflows also declare their required permissions.

## 5. Run the workflows manually first

Open:

`Actions`

Then run these workflows one at a time:

- `Generate GitHub Profile Assets`
- `WakaTime README`
- `Latest Blog Posts`

Manual execution is useful for checking failures before waiting for scheduled runs.

## 6. GitHub stats

The stats workflow generates local SVG files:

```text
profile/stats.svg
profile/top-langs.svg
```

The current stats action supports generating these cards inside GitHub Actions, which avoids relying on a public hosted stats endpoint for every README view.

## 7. Contribution animation

The snake workflow generates:

```text
profile/github-snake-dark.svg
```

It uses `Platane/snk@v3`.

## 8. WakaTime

Create a WakaTime account and install the WakaTime extension/plugin in the editors you use.

Then add this repository secret:

```text
WAKATIME_API_KEY
```

The workflow uses the maintained `athul/waka-readme` action.

Without the secret, the workflow will fail or the WakaTime section will remain unchanged. This is expected until WakaTime is configured.

## 9. Medium

You said you want Medium updates but did not provide a Medium username.

The workflow is intentionally configured with a placeholder feed:

```text
https://medium.com/feed/@YOUR_MEDIUM_USERNAME
```

Replace `YOUR_MEDIUM_USERNAME` in:

```text
.github/workflows/blog-posts.yml
```

with your actual Medium username.

If you do not have a Medium account, disable/remove that workflow until you create one.

## 10. Spotify

Spotify integration requires external credentials and additional setup. The README contains a safe placeholder until you configure it.

Do **not** put Spotify Client Secret or Refresh Token directly into README.md.

Use GitHub Secrets if you implement the Spotify integration.

The 2026 Spotify API changes may require a Premium account for live currently-playing information depending on the integration used.

## 11. Visitor counter

The profile-view counter is intentionally an external image badge. It does not require a GitHub token.

If you prefer not to use an external visitor-counter service later, remove the `komarev.com/ghpvc` image from README.md.

## 12. Project repository links

You currently did not provide GitHub URLs for:

- STORM
- Radar Detection
- Crop Disease Prediction

When those repositories are ready, replace the corresponding project text with links.

## 13. Git commands

From the profile repository:

```bash
git init
git branch -M main
git remote add origin https://github.com/Harish-121-ss/Harish-121-ss.git
git add .
git commit -m "Build production GitHub profile README"
git push -u origin main
```

If the remote already contains files:

```bash
git pull --rebase origin main
git push origin main
```

If you have local work that conflicts with the remote, stop and inspect the conflict instead of using a force push.

## 14. Validation checklist

Before considering the profile finished:

- [ ] Repository name is `Harish-121-ss`
- [ ] Repository is public
- [ ] README renders correctly
- [ ] All profile links open
- [ ] GitHub username is correct
- [ ] No email is exposed
- [ ] No API key/token is committed
- [ ] Stats workflow succeeds
- [ ] Snake workflow succeeds
- [ ] WakaTime secret is configured if WakaTime is enabled
- [ ] Medium username/feed is configured if Medium is enabled
- [ ] Spotify is configured only if you want the live feature
- [ ] Project repository URLs are added when available
- [ ] Mobile rendering is checked
- [ ] Images have useful alt text
- [ ] No fake statistics or skill percentages are shown

## ⚠️ Important

Do not run:

```bash
git push --force
```

on the profile repository unless you fully understand what history you are replacing.

Also, if a workflow modifies `README.md`, avoid editing the same generated section manually while the workflow is running.
