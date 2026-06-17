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

## Related repos

| Repo | Role |
|------|------|
| [`Trigv/trigv`](https://github.com/Trigv/trigv) | Shared examples & snippets (not the org profile) |
| [`Trigv/platform`](https://github.com/Trigv/platform) | Application code + internal `_docs/` |
