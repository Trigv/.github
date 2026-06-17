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

Future public example repos (e.g. `Trigv/examples`) can be linked from the **Examples** section when they exist.

## Related repos (internal)

| Repo | Role |
|------|------|
| [`Trigv/platform`](https://github.com/Trigv/platform) | Application code + internal `_docs/` |
| [`Trigv/mobile`](https://github.com/Trigv/mobile) | Flutter apps (private) |
| [`Trigv/trig-html`](https://github.com/Trigv/trig-html) | Marketing + public docs (private) |
