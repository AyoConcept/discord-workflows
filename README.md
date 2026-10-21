# discord-workflows

GitHub → Discord workflows and daily task automation.

## Setup
1. In Discord, go to your channel: Settings → Integrations → Webhooks → New Webhook, copy the URL.
2. In this repo: Settings → Secrets and variables → Actions → New repository secret.
   Name it `DISCORD_WEBHOOK`, paste the webhook URL as the value.
3. Move the workflow files from `workflows/` to `.github/workflows/`
   (GitHub does not let apps write directly to `.github/workflows/`, so this last step is manual —
   you can do it in the GitHub web UI by opening each file and using “Move”).
4. Workflows will post automatically. The webhook URL lives only in the repo secret, never in the code.

## Workflows
- `discord-notify.yml` – posts pushes, PRs, issues, and releases to Discord
- `daily-digest.yml` – weekday morning digest of open issues/PRs at 8am ET (plus manual trigger)
