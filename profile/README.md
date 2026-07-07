<div align="center">

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/Trigv/.github/main/assets/logo-trigv-dark.svg">
  <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/Trigv/.github/main/assets/logo-trigv-light.svg">
  <img alt="Trigv" src="https://raw.githubusercontent.com/Trigv/.github/main/assets/logo-trigv-dark.svg" width="320">
</picture>

### Realtime events. Instant alerts.

Send real-time push notifications from your backend, scripts, cron jobs, CI/CD workflows, webhooks, and AI agents to iPhone and Android.

**Your notification history lives on your device. We never see it.**

<br>

[![Website](https://img.shields.io/badge/website-trigv.com-FF3253?style=for-the-badge)](https://trigv.com)
[![Docs](https://img.shields.io/badge/docs-read%20the%20API-0B0D10?style=for-the-badge)](https://trigv.com/docs)
[![Dashboard](https://img.shields.io/badge/app-dashboard-FBFBFA?style=for-the-badge&labelColor=0B0D10&color=FF3253)](https://app.trigv.com)
[![GitHub Action](https://img.shields.io/badge/GitHub%20Action-marketplace-0B0D10?style=for-the-badge)](https://github.com/marketplace/actions/trigv)

</div>

---

## What is Trigv?

Trigv is a **developer notification platform** for sending real-time push alerts from backend applications, scripts, cron jobs, CI/CD pipelines, webhooks, and AI agents to iPhone and Android. Send a JSON payload (or a curl one-liner) from your stack; subscribers on a channel get an instant mobile push. Event **content** stays on-device; the server stores **metadata only**.

| | |
|---|---|
| **Sweet spot** | Backend alerts and monitoring from scripts, cron, CI/CD, and webhooks. Metadata on the server, content on your phone |
| **Setup goal** | Register → API key → curl → notification in **under 5 minutes** |
| **Privacy** | Title, body, and feed history are **on your phone**, not on our servers |

---

## Quick start

```bash
curl -sS -X POST "https://api.trigv.com/api/v1/events" \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer trgv_YOUR_KEY" \
  -d '{
    "channel": "general",
    "title": "Deploy finished",
    "description": "Build #42 succeeded in 38s",
    "level": "success",
    "url": "https://example.com/deployments/42"
  }'
```

[Start your 7-day trial](https://trigv.com) · [API reference](https://trigv.com/docs/events) · [Integration guides](https://trigv.com/docs/learn)

### GitHub Actions

Add [`TRIGV_API_KEY`](https://trigv.com/docs/learn/api-keys) as a repository secret, then notify on failure:

```yaml
- name: Notify Trigv on failure
  if: failure()
  uses: Trigv/trigv-github-action@v1.1.0
  with:
    api-key: ${{ secrets.TRIGV_API_KEY }}
    title: Workflow failed
    level: error
    event-type: ci.failed
```

[GitHub Marketplace](https://github.com/marketplace/actions/trigv) · [Actions guide](https://trigv.com/docs/learn/github-actions) · [trigv-github-action](https://github.com/Trigv/trigv-github-action)

---

## Webhooks

Connect external services without changing your application code. Create an inbound webhook in the [Trigv dashboard](https://app.trigv.com), copy the generated URL, paste it into your provider, and choose which events to send. Trigv verifies signatures where supported and delivers them as mobile push notifications.

Supported providers include **GitHub**, **Stripe**, **Vercel**, **Railway**, **Creem**, **Supabase**, **Sentry**, **Laravel Cloud**, **Freemius**, and **Generic JSON** (plus others in the dashboard).

1. Create a webhook in Trigv and pick a provider
2. Copy the webhook URL
3. Paste it into the provider's webhook settings
4. Select the events you care about in the provider
5. Receive push notifications on iPhone and Android

---

## SDKs & developer tools

Official clients for [`POST /v1/events`](https://trigv.com/docs/events). All packages are published on public registries (SDKs **1.0.0**, CLI and MCP **0.1.0**). Each repo includes README, examples, and tests.

| Language / tool | Repository | Install |
|-----------------|------------|---------|
| Node.js / TypeScript | [trigv-node](https://github.com/Trigv/trigv-node) | [`npm install @trigv/sdk`](https://www.npmjs.com/package/@trigv/sdk) |
| Python | [trigv-python](https://github.com/Trigv/trigv-python) | [`pip install trigv`](https://pypi.org/project/trigv/) |
| PHP | [trigv-php](https://github.com/Trigv/trigv-php) | [`composer require trigv/trigv`](https://packagist.org/packages/trigv/trigv) |
| Go | [trigv-go](https://github.com/Trigv/trigv-go) | [`go get github.com/trigv/trigv-go@v1.0.0`](https://pkg.go.dev/github.com/trigv/trigv-go@v1.0.0) |
| Ruby | [trigv-ruby](https://github.com/Trigv/trigv-ruby) | [`gem install trigv`](https://rubygems.org/gems/trigv) |
| CLI | [trigv-cli](https://github.com/Trigv/trigv-cli) | [`npm install -g @trigv/cli`](https://www.npmjs.com/package/@trigv/cli) |
| MCP (AI agents) | [trigv-mcp](https://github.com/Trigv/trigv-mcp) | [`npm install -g @trigv/mcp`](https://www.npmjs.com/package/@trigv/mcp) |
| GitHub Actions | [trigv-github-action](https://github.com/Trigv/trigv-github-action) | `uses: Trigv/trigv-github-action@v1.1.0` |

[Integration guides](https://trigv.com/docs/learn) · [OpenAPI spec](https://api.trigv.com/openapi.yaml)

---

## Examples

| Example | Link |
|---------|------|
| curl | [Docs](https://trigv.com/docs/learn/curl) |
| Webhooks | [Dashboard](https://app.trigv.com) |
| GitHub Actions | [Marketplace](https://github.com/marketplace/actions/trigv) · [Repo](https://github.com/Trigv/trigv-github-action) |
| SDKs (above) | See **SDKs & developer tools** |

---

## Use cases

- **Deploy & CI**: `deploy.completed`, `build.failed`
- **Payments**: `sale.completed`, `subscription.cancelled`
- **Cron & scripts**: backup finished, job stalled
- **Webhooks & monitoring**: Stripe charges, Sentry issues, uptime alerts
- **AI agents**: workflow step done, human approval needed
- **Security**: login from new IP, rate limit hit

---

## Status & support

| | |
|---|---|
| **Status** | [status.trigv.com](https://status.trigv.com) |
| **Support** | [trigv.com/support](https://trigv.com/support) · support@trigv.com |
| **Legal** | [Privacy](https://trigv.com/legal/privacy-policy) · [Terms](https://trigv.com/terms) |

---

<div align="center">

<sub>Built by <a href="https://webtions.com">Webtions OU</a> · Trigv is trigger + <em>v</em> (velocity, vector, version)</sub>

</div>
