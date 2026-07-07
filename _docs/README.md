# `_docs`

Internal notes for **`Trigv/.github`**.

## Purpose

This repo powers the **public organization profile** on [github.com/Trigv](https://github.com/Trigv).

Per [GitHub’s org profile docs](https://docs.github.com/en/organizations/collaborating-with-groups-in-organizations/customizing-your-organizations-profile):

| File | Renders on |
|------|------------|
| `profile/README.md` | Org **Overview** tab (public view) |

This is **not** the same mechanism as a personal profile README (`username/username` repo). Orgs use **`.github/profile/README.md`**.

## Optional later

| Repo | Use |
|------|-----|
| `Trigv/.github-private` + `profile/README.md` | Member-only org profile view |

## Assets

Logos in `assets/` are referenced from `profile/README.md` via `raw.githubusercontent.com` URLs (required for org profile rendering).

## Public profile content

Do **not** list private application repos on `profile/README.md`. Link to [trigv.com/docs](https://trigv.com/docs) instead.

Future public example repos (e.g. `Trigv/examples`) can be linked from the **Examples** section when they exist. SDK repos are listed on `profile/README.md` under **SDKs & developer tools**.

## Recommended GitHub organisation topics

Set these on the **Trigv** organisation profile in GitHub (Settings → Profile). Not shown on the public README.

`push-notifications` · `developer-tools` · `webhooks` · `ci-cd` · `monitoring` · `alerts` · `devops` · `api` · `mcp` · `ai-agents`

## Related repos (internal)

| Repo | Role |
|------|------|
| [`Trigv/platform`](https://github.com/Trigv/platform) | Application code + internal `_docs/` |
| [`Trigv/mobile`](https://github.com/Trigv/mobile) | Flutter apps (private) |
| [`Trigv/trig-html`](https://github.com/Trigv/trig-html) | Marketing + public docs (private) |
| [`Trigv/trigv-node`](https://github.com/Trigv/trigv-node) | Node.js / TypeScript SDK (`@trigv/sdk`) |
| [`Trigv/trigv-python`](https://github.com/Trigv/trigv-python) | Python SDK |
| [`Trigv/trigv-php`](https://github.com/Trigv/trigv-php) | PHP SDK |
| [`Trigv/trigv-go`](https://github.com/Trigv/trigv-go) | Go SDK |
| [`Trigv/trigv-ruby`](https://github.com/Trigv/trigv-ruby) | Ruby SDK |
| [`Trigv/trigv-cli`](https://github.com/Trigv/trigv-cli) | CLI (`@trigv/cli`) |
| [`Trigv/trigv-mcp`](https://github.com/Trigv/trigv-mcp) | MCP server (`@trigv/mcp`) |
| [`Trigv/trigv-github-action`](https://github.com/Trigv/trigv-github-action) | GitHub Action |
