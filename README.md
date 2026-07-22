# OpenStack Horizon Test Job Monitor - Web Dashboard

[![Live Demo](https://img.shields.io/badge/demo-live-brightgreen)](https://xtmprsqzntwlfb.github.io/openstack-horizon-test-job-monitor-web/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

Browser-based real-time monitoring dashboard for OpenStack Horizon test jobs running on Zuul CI.


## Quick Start

### Option 1: Use the Live Version

Simply visit: **https://xtmprsqzntwlfb.github.io/openstack-horizon-test-job-monitor-web/**

No installation needed!

### Option 2: Run Locally

```bash
# Clone the repository
git clone https://github.com/xtmprsqzntwlfb/openstack-horizon-test-job-monitor-web.git
cd openstack-horizon-test-job-monitor-web

# Open in browser
open index.html
# or
python3 -m http.server 8000
# Then visit http://localhost:8000
```

## How It Works

1. Fetches data directly from [Zuul CI API](https://zuul.opendev.org/openapi) for openstack/horizon builds
2. Processes build statistics in the browser: success/failure rates, trends, durations
3. Displays metrics in a sortable jobs table with sparklines, trend indicators, and expandable build history per job
4. Shows when jobs ran and on which Gerrit patches or branch commits:
   - check/gate pipelines: links to Gerrit reviews (e.g., `123456,7`)
   - post-merge pipelines: shows branch names (e.g., `stable/2025.1`)
   - periodic and experimental jobs: scheduled builds running on branch heads
5. Auto-refreshes at configurable intervals
6. Saves preferences to browser localStorage (theme, filters, time periods, refresh interval)

All processing happens client-side, no backend server required!


## Links

- [OpenStack Horizon](https://docs.openstack.org/horizon/) - Dashboard project
- [Zuul CI](https://zuul-ci.org/) - CI/CD system
- [OpenStack](https://www.openstack.org/) - Cloud infrastructure

---

**Note**: This is an independent monitoring tool and is not officially affiliated with the OpenStack project.
