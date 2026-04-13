# Complimetric Status

This repository powers the [Complimetric status page](https://status.complimetric.com).

Built with [Upptime](https://upptime.js.org) — open-source uptime monitoring via GitHub Actions.

## Services monitored

| Service         | URL                                          | Max response time |
| --------------- | -------------------------------------------- | ----------------- |
| API             | `https://api.complimetric.com/health`        | 3000ms            |
| Web Application | `https://complimetric.com`                   | 5000ms            |
| Integrations    | `https://mcp.complimetric.com/health`        | 3000ms            |
| Scan Engine     | `https://api.complimetric.com/api/v2/health` | 5000ms            |

## How it works

- GitHub Actions checks each service **every hour**
- On downtime: creates a GitHub Issue, updates the status page automatically
- On recovery: closes the Issue, restores green status
- 90-day uptime history visible at [status.complimetric.com](https://status.complimetric.com)

## Setup

### Prerequisites

1. Create a GitHub Personal Access Token (PAT) with `repo` and `workflow` scopes
2. Add it as a repository secret named `GH_PAT`
3. Enable GitHub Pages on the `gh-pages` branch

### DNS

Add a CNAME record in your DNS provider:

```
status.complimetric.com → complimetric.github.io
```

## Incident response

Contact [support@complimetric.com](mailto:support@complimetric.com) or visit [status.complimetric.com](https://status.complimetric.com) for current status.
