# discord-workflows

GitHub → Discord workflows and daily task automation.

## Setup
1. Create a Discord webhook in your channel: Channel Settings → Integrations → Webhooks → New Webhook
2. Add it as a GitHub secret named `DISCORD_WEBHOOK_URL` in this repo: Settings → Secrets and variables → Actions → New repository secret
3. Workflows will post automatically — the webhook URL is never stored in the repo.

## Workflows
- `discord-notifications.yml` – posts pushes, PRs, and issues to Discord
- `daily-digest.yml` – weekday morning digest at 9am ET (manual trigger also available)
