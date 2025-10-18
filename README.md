# ua-collector ![version](https://img.shields.io/npm/v/ua-collector) ![types](https://img.shields.io/npm/types/ua-collector) ![ci](https://github.com/ua-tools/collector/workflows/CI/badge.svg)

Collect and analyze user agent strings from real-world traffic data

## Quick Start

```bash
yarn add ua-collector
```

## API Usage

```javascript
const { fetchUserAgents } = require('ua-collector');

// Get current top user agents
fetchUserAgents()
  .then(data => {
    data.forEach(entry => {
      console.log(`${entry.frequency}: ${entry.browser} on ${entry.os}`);
      // "8.3%: Chrome 94 on Windows 11"
    });
  });
```

Data is fetched from live sources. Implement caching for production use.

## Features

- Real-time user agent statistics
- Browser and OS breakdown
- Mobile and desktop coverage
- TypeScript definitions included

## License
ISC Licensed - full terms in [LICENSE](LICENSE) file.
