# charly-coder

The `charly-coder` family — the coder/dev-image command skills.

The `charly-coder` candy is a **concept candy**: it ships no install content and
owns the `coder` family of `skill:` entities whose names have no namesake candy
(the coder/dev image skills). It currently carries the `kubernetes-layer` skill
(kubectl and Helm client tools). `candy/plugin-marketplace` regenerates the
standalone [opencharly/marketplace](https://github.com/opencharly/marketplace)
corpus from these entities, so the skills are authored here and projected there.

## What it provides

| Property | Value |
|---|---|
| Layer / candy | `charly-coder` (concept candy) |
| Install content | none — a `true` no-op `plan:` |
| Owns | 1 `skill:` entity: `kubernetes-layer` |
| Projected to | `marketplace/coder/skills/` |
| Service / port | none |

## How to use it

This repo is consumed as a **skill source**, not as an image layer. Edit the
`skill:` entities in `charly.yml`; the marketplace regeneration projects them
into `/charly-coder:*` pages. To reference the repo directly:

```yaml
my-box:
  candy:
    base: fedora
    candy:
      - '@github.com/opencharly/layer-charly-coder:v2026.265.2127'
```

## Layout

- `charly.yml` — the `charly-coder:` concept candy entity plus the
  `kubernetes-layer-skill:` entity.
- `.github/workflows/tag-on-merge.yml` — CalVer tag + `CHANGELOG/` on merge.
- `README.md` — this user overview.

## Related

- Owning skill: `/charly-coder:kubernetes-layer`
- Authoring reference: `/charly-image:layer`
- [`opencharly/marketplace`](https://github.com/opencharly/marketplace) — the projected corpus
- [`opencharly/charly`](https://github.com/opencharly/charly) — the charly CLI and image builder
- [`opencharly/opencharly`](https://github.com/opencharly/opencharly) — the umbrella
