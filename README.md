# Axxit Technology Radar

Built with [AOE Technology Radar](https://github.com/AOEpeople/aoe_technology_radar).
Published at https://michiel-vanherreweghe-axxit.github.io/techradar on every merge to `main`.

## Run locally

```sh
npm install
npm run serve   # http://localhost:3000/techradar
```

## Add or move an item

Items live in `radar/<release-date>/<id>.md`. The filename is the item's id.

```markdown
---
title: "OpenTelemetry"
ring: adopt                 # adopt | trial | assess | hold
quadrant: methods-and-patterns  # languages-and-frameworks | methods-and-patterns | platforms-and-operations | tools
tags: [monitoring]          # purpose, used by the filter below the radar
---

Why it is in this ring.
```

- **New item:** add a file to the latest release folder.
- **Move an item:** copy it into a new release folder (`radar/YYYY-MM-DD/`) with the new ring and
  explain why. Earlier releases stay as the item's history.

Reuse an existing purpose tag where one fits: `programming-languages`, `frontend`, `backend`,
`data`, `development-tooling`, `testing`, `infrastructure-as-code`, `cloud`, `identity`,
`security`, `ci-cd`, `monitoring`, `ai`.

`npm run build` fails on invalid items, and so does the pull request check.
