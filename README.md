# OpenStack Horizon Test Job Monitor - Web Dashboard

[![Live Demo](https://img.shields.io/badge/demo-live-brightgreen)](https://xtmprsqzntwlfb.github.io/openstack-horizon-test-job-monitor-web/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

Browser-based real-time monitoring dashboard for OpenStack Horizon test jobs running on Zuul CI.

🔗 **Live Demo**: https://xtmprsqzntwlfb.github.io/openstack-horizon-test-job-monitor-web/

## Features

- ✨ **Zero setup** - Just open the page in your browser
- 🔄 **Auto-refresh** - Updates every 30 seconds
- 🎨 **Modern UI** - Dark theme with color-coded health indicators
- 📱 **Responsive** - Works on desktop, tablet, and mobile
- 🌐 **Client-side** - No backend server needed
- 🆓 **Free hosting** - Deployed on GitHub Pages

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

## Dashboard Overview

### Summary Cards
- **Total Jobs** - Number of unique test jobs
- **Total Runs** - Total build executions
- **Success** - Successful builds with percentage
- **Failure** - Failed builds
- **Running** - Currently executing builds

### Job Details Table
- **Job Name** - Test job identifier
- **Total** - Total runs for this job
- **✓** - Success count
- **✗** - Failure count  
- **▶** - Running count
- **Success %** - Success rate with color coding
- **Avg Time** - Average execution duration

### Color Coding
- 🟢 **Green**: ≥90% success rate (healthy)
- 🟡 **Yellow**: 70-89% success rate (watch)
- 🔴 **Red**: <70% success rate (needs attention)

## How It Works

1. Fetches data directly from [Zuul CI API](https://zuul.opendev.org/api)
2. Processes build statistics in the browser
3. Displays real-time metrics with color-coded indicators
4. Auto-refreshes every 30 seconds

All processing happens client-side - no backend server required!

## Customization

Edit `index.html` to customize:

**Change refresh interval:**
```javascript
const REFRESH_INTERVAL = 60000; // 60 seconds
```

**Change data limit:**
```javascript
const builds = await fetchBuilds(500); // Fetch 500 builds
```

**Adjust color thresholds:**
```javascript
function getSuccessRateClass(rate) {
    if (rate >= 95) return 'rate-high';    // Green at 95%+
    if (rate >= 80) return 'rate-medium';  // Yellow at 80%+
    return 'rate-low';                     // Red below 80%
}
```

## Deploy Your Own

### GitHub Pages (Recommended)

1. Fork this repository
2. Go to **Settings → Pages**
3. Select **Source**: `main` branch, `/` (root)
4. Your dashboard will be live at: `https://yourusername.github.io/openstack-horizon-test-job-monitor-web/`

### Other Static Hosting

Deploy to any static host:
- **Netlify**: Drag & drop the `index.html` file
- **Vercel**: Connect your GitHub repo
- **Cloudflare Pages**: Push to repo and deploy
- **AWS S3**: Upload as static website

## Browser Compatibility

Works on all modern browsers:
- ✅ Chrome/Edge 90+
- ✅ Firefox 88+
- ✅ Safari 14+
- ✅ Mobile browsers (iOS Safari, Chrome Mobile)

## Related Projects

- [CLI Monitor](https://github.com/xtmprsqzntwlfb/openstack-horizon-test-job-monitor) - Terminal-based Python version with demo mode

## Tech Stack

- **Pure HTML/CSS/JavaScript** - No frameworks needed
- **Zuul API** - Real-time CI/CD data
- **GitHub Pages** - Free hosting

## Data Source

- **API**: `https://zuul.opendev.org/api`
- **Project**: `openstack/horizon`
- **Fetch limit**: 200 most recent builds
- **Update frequency**: Every 30 seconds

## Privacy & Security

- ✅ All data is public (Zuul API is public)
- ✅ No cookies or tracking
- ✅ No data storage
- ✅ All processing happens in your browser
- ✅ No authentication required

## Contributing

Contributions welcome! Feel free to:
- Report bugs via GitHub issues
- Suggest features
- Submit pull requests

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
