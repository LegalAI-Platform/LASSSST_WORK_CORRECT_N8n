# n8n workflow exports

Seven workflows exported from the n8n workspace on 2026-10-09. Each JSON file preserves the workflow nodes, connections, settings, activation state, tags, and available node-group metadata.

## Workflows

- `LAsST_IMAGE_PIPELINE_V1.json`
- `LAsST_RESEARCH_PIPELINE_V1.json`
- `LAsST_TELEGRAM_REVIEW_V1.json`
- `LAsST_WORDPRESS_DRAFT_V1.json`
- `LAsST_WRITING_REVIEW_V1.json`
- `UPDATES_DISPATCHER_WATCHDOG.json`
- `UPDATES_ONE_ARTICLE.json`

## Import notes

- n8n credential secrets are not included. Credential references may need to be reconnected after import.
- Static Telegram chat IDs were replaced in the public exports with the n8n expression `={{ $vars.TELEGRAM_CHAT_ID }}`. Create a string variable named `TELEGRAM_CHAT_ID` in the target n8n workspace before running the affected notifications.
- Workflows that call another workflow have an allow-list in `settings.callerIds`; update those IDs if importing them into a different n8n workspace.
- The two source workflows that were inactive remain inactive in these exports.

