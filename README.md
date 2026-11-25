# Unraid templates

Docker templates for [Unraid Community Applications](https://ca.unraid.net), one XML file per app.

| App | Template | What it is |
| --- | --- | --- |
| [Agent Cairn](https://github.com/itsmemac/AgentCairn) | [`templates/cairn.xml`](templates/cairn.xml) | Shared, persistent project memory for AI coding agents, backed by Neo4j |
| [Packwright](https://github.com/itsmemac/Packwright) | [`templates/packwright.xml`](templates/packwright.xml) | Manage PS5 dump, image and package collections from a browser |

## Use it before it is listed

On Unraid: **Settings → Docker → Advanced View → Template repositories**, add `https://github.com/itsmemac/unraid-template`, save, then **Docker → Add Container** and pick the template.

## Layout

```
ca_profile.xml        repository profile shown in Community Applications
templates/<app>.xml   one Docker template per app
icons/<app>.png       square PNG icon per app (256-512 px)
```

Every template's `TemplateURL` and `Icon` point at the raw files on `main`. Check a template with Unraid's [validator](https://github.com/unraid-apps/template/blob/main/scripts/validate-template.py): `python3 validate-template.py --check-urls ca_profile.xml templates/*.xml`.

## Adding an app

1. Copy an existing template to `templates/<app>.xml` and change every field, including `TemplateURL` and `Icon`.
2. Add `icons/<app>.png`.
3. Add a row to the table above and validate.

MIT licensed. App bugs go to each app's own repository.
