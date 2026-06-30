# OpenStack Horizon Test Job Monitor - Web Dashboard

[![Live Demo](https://img.shields.io/badge/demo-live-brightgreen)](https://xtmprsqzntwlfb.github.io/openstack-horizon-test-job-monitor-web/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

Browser-based real-time monitoring dashboard for OpenStack Horizon test jobs running on Zuul CI.

🔗 **Live Demo**: https://xtmprsqzntwlfb.github.io/openstack-horizon-test-job-monitor-web/


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

1. Fetches data directly from [Zuul CI API](https://zuul.opendev.org/api)
2. Processes build statistics in the browser
3. Displays real-time metrics with color-coded indicators
4. Auto-refreshes at configurable intervals (default: 5 minutes)
5. Saves all preferences to browser localStorage

All processing happens client-side - no backend server required!


## License

MIT License - see [LICENSE](LICENSE) file for details.

## Author

Tatiana Ovchinnikova

## Acknowledgments

- [OpenStack Horizon](https://docs.openstack.org/horizon/) - Dashboard project
- [Zuul CI](https://zuul-ci.org/) - CI/CD system
- [OpenStack](https://www.openstack.org/) - Cloud infrastructure

---

**Note**: This is an independent monitoring tool and is not officially affiliated with the OpenStack project.
