# Deploying @vahidekhlasi

@vahidekhlasi runs on a single Cloudflare Worker on the vip plan. One deploy creates the Worker, its KV namespace, and its D1 database, and serves the whole panel, the subscription links, and the Telegram bot from your own Cloudflare account.

## Install

You need a Cloudflare account. Pick one path.

### Option A: Deploy to Cloudflare (recommended)

Use the **Deploy to Cloudflare** button in the repository and follow the prompts:

[![Deploy to Cloudflare](https://deploy.workers.cloudflare.com/button)](https://deploy.workers.cloudflare.com/?url=https://github.com/ekhlasi1/vahid)

Cloudflare's supported deployment flow creates a user-owned Git repository, provisions the Worker, the KV namespace, and the D1 database, and connects Workers Builds.

### Option B: The Telegram bot (no computer)

The installer bot [@vahidekhlasi](https://t.me/vahidekhlasi) walks you through the same deployment from your phone. Check the bot username exactly before you start.

### Option C: Wrangler (CLI)

```bash
# 1. install the Cloudflare CLI
npm install -g wrangler
wrangler login

# 2. install dependencies and deploy
npm ci
npm run deploy
```

Then open `https://<your-worker>.workers.dev/admin`, finish the short setup, and set your admin password. That login is your panel. Keep it private; user subscription links are credentials, so treat them like passwords.

## Verify your download

The public repository ships a single obfuscated deployment artifact, `worker.js`, with its checksum published two ways so you can confirm you are running the release that was announced:

- `version.json` carries the expected `worker_sha256` for the current release.
- `SHA256SUMS` lists the same digest next to the file name.

Check a copy by hand:

```bash
curl -fsSLO https://raw.githubusercontent.com/ekhlasi1/vahid/main/worker.js
curl -fsSL https://raw.githubusercontent.com/ekhlasi1/vahid/main/SHA256SUMS | sha256sum -c
```

You can also confirm the artifact parses as valid JavaScript before deploying:

```bash
npm run check
```

## Update

@vahidekhlasi does not update or redeploy itself at runtime. Updates run through GitHub and Workers Builds, so the source diff, the build result, the deployment history, and the rollback target all stay visible.

### Review mode (default)

1. Repositories created from the Deploy to Cloudflare flow include a daily **Check for updates** GitHub Action. You can also start it from **Actions > Check for updates > Run workflow**.
2. In the new GitHub repository, enable Actions and allow GitHub Actions to create pull requests.
3. In Cloudflare, open **Worker > Settings > Build > Branch control** and enable **Builds for non-production branches**. This gives the update branch a preview version and URL without replacing the live deployment.
4. When a newer release exists, the workflow opens a pull request containing only `worker.js` and `version.json`. Your account-specific Wrangler bindings are left untouched.
5. Review the source diff and the Cloudflare preview URL, then merge to deploy through Workers Builds.

### Automatic mode (opt in)

Users who prefer hands-off updates can opt in once by creating a repository variable named `NOVA_UPDATE_MODE` with the value `automatic` in Settings > Secrets and variables > Actions > Variables.

## Backend mode (optional, for calls)

A plain vip Worker cannot carry UDP, so voice and video calls (FaceTime, WhatsApp, Telegram) need a backend. Front your Worker with your own Xray or sing-box VPS:

```bash
bash <(curl -fsSL https://raw.githubusercontent.com/ekhlasi1/vahid/main/nova-backend.sh)
```

Then enable **Backend mode** in the panel (Network Settings > Backend mode) and enter your VPS address.

(باقی متن با ارجاعات به ریپو شما به‌روز شده)
