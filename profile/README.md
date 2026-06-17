<div align="center">

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/Trigv/.github/main/assets/logo-trigv-dark.svg">
  <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/Trigv/.github/main/assets/logo-trigv-light.svg">
  <img alt="Trigv" src="https://raw.githubusercontent.com/Trigv/.github/main/assets/logo-trigv-dark.svg" width="320">
</picture>

### Realtime events. Instant alerts.

Capture events from your code, cron jobs, and agents — get push notifications on your phone in seconds.

**Your notification history lives on your device. We never see it.**

<br>

[![Website](https://img.shields.io/badge/website-trigv.com-FF3253?style=for-the-badge)](https://trigv.com)
[![Docs](https://img.shields.io/badge/docs-read%20the%20API-0B0D10?style=for-the-badge)](https://trigv.com/docs)
[![Dashboard](https://img.shields.io/badge/app-dashboard-FBFBFA?style=for-the-badge&labelColor=0B0D10&color=FF3253)](https://app.trigv.com)

</div>

---

## What is Trigv?

Trigv is a **notification-first** event platform for developers. Send a JSON payload (or a curl one-liner) from your backend, CI, or automation — subscribers on a channel get an instant mobile push. Event **content** stays on-device; the server stores **metadata only**.

| | |
|---|---|
| **Sweet spot** | Between Pushover (alerts, no feed) and LogSnag (dashboard-heavy) |
| **Setup goal** | Register → API key → curl → notification in **under 5 minutes** |
| **Privacy** | Title, body, and feed history are **on your phone** — not on our servers |

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
    "level": "success"
  }'
```

[Create a free account](https://app.trigv.com/register) · [API reference](https://trigv.com/docs/events) · [Examples](https://github.com/Trigv/trigv/tree/main/examples)

---

## Repositories

| Repo | What it is |
|------|------------|
| [**platform**](https://github.com/Trigv/platform) | Laravel API, billing, dashboard (`api.trigv.com` + `app.trigv.com`) |
| [**mobile**](https://github.com/Trigv/mobile) | Flutter app — iOS & Android push feed |
| [**trig-html**](https://github.com/Trigv/trig-html) | Marketing site + public docs ([trigv.com](https://trigv.com)) |
| [**trigv**](https://github.com/Trigv/trigv) | Shared examples, curl snippets, integration samples |

---

## Use cases

- **Deploy & CI** — `deploy.completed`, `build.failed`
- **Payments** — `sale.completed`, `subscription.cancelled`
- **Cron & scripts** — backup finished, job stalled
- **AI agents** — workflow step done, human approval needed
- **Security** — login from new IP, rate limit hit

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
