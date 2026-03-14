# SubnetCalc

A modern, browser-based subnet calculator for both IPv4 and IPv6 networks. Zero dependencies — just static HTML, CSS, and vanilla JavaScript.

![HTML](https://img.shields.io/badge/HTML-single%20page-E34F26)
![JavaScript](https://img.shields.io/badge/JavaScript-vanilla-F7DF1E)
![License](https://img.shields.io/badge/license-MIT-blue)

## Features

### IPv4 Calculator (`index.htm`)
- **Subnet calculation** — enter an IP address with CIDR prefix, subnet mask, or desired host/network count
- **Bidirectional input** — change any field (CIDR, mask, hosts, networks) and all others update automatically
- **Subnet details** — network/broadcast addresses, usable host range, wildcard mask, class info, CIDR notation
- **Binary visualization** — color-coded network vs. host bits with a visual subnet map
- **Common subnet finder** — enter two IPs to find the smallest common subnet
- **CIDR reference table** — full /0–/32 table with masks, host counts, and subnet counts
- **Quick-select buttons** — one-click preset for common CIDR values
- **Query string support** — link directly with `?ip=10.0.0.1&cidr=16`

### IPv6 Calculator (`ipv6.htm`)
- **128-bit math via BigInt** — accurate calculation across the full IPv6 address space
- **Address expansion & compression** — full and compressed RFC 5952 notation
- **Address type detection** — Global Unicast, Link-Local, Unique Local, Multicast, Loopback, IPv4-Mapped, etc.
- **Binary visualization** — color-coded prefix vs. interface ID with a visual prefix map
- **Total addresses & /64 networks** — displayed in both 2^n notation and full decimal
- **Reference table** — common prefix lengths (/12–/128) with typical use cases

### Shared
- **Light / Dark mode** — toggle button with `localStorage` persistence and no flash-of-wrong-theme
- **Responsive design** — fully mobile-friendly, scales from phone to ultrawide
- **Shared theme system** — single `theme.css` drives both pages with page-specific accent colors (cyan for IPv4, purple for IPv6)

## Project Structure

```
subnet-calc/
├── index.htm    # IPv4 subnet calculator
├── ipv6.htm     # IPv6 subnet calculator
├── theme.css    # Shared light/dark theme & component styles
└── README.md
```

## Usage

Serve the directory with any static web server, or open `index.htm` directly in a browser.

```bash
# Python
python3 -m http.server 8080 -d /path/to/subnet-calc

# PHP
php -S localhost:8080 -t /path/to/subnet-calc

# Or just open the file
open index.htm
```

No build step, no bundler, no node_modules.

## Browser Support

Modern browsers with ES2020+ support (BigInt is required for the IPv6 calculator).

- Chrome 67+
- Firefox 68+
- Safari 14+
- Edge 79+

## License

MIT License

Copyright © 2009–2026 ZeroGlitchX
