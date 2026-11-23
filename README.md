# Dark Docs 2.0

Enhanced dark theme for Google Docs with customizable accent colors, plus a beautiful website.

[![Build and Release](https://github.com/ameyalambat/dark-docs-2.0/actions/workflows/release.yml/badge.svg)](https://github.com/ameyalambat/dark-docs-2.0/actions/workflows/release.yml)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Chrome Web Store](https://img.shields.io/badge/Chrome%20Web%20Store-Dark%20Docs%202.0-blue)](https://chromewebstore.google.com/detail/docs-dark-20/djmmkojigpkdagglmjjdjiddopgdchcn)
[![Website](https://img.shields.io/badge/Website-darkdocs.ameyalambat.com-green)](https://darkdocs.ameyalambat.com)

## 🌟 Features

### Chrome Extension
- 🌙 **Dark Mode**: Modern dark theme for Google Docs
- 🎨 **Customizable Colors**: Adjustable accent colors
- ⚡ **Fast Performance**: Lightweight and efficient
- 🔧 **Easy Configuration**: User-friendly popup interface
- 🌐 **Multi-Browser**: Support for Chrome, Firefox, Edge, and Opera

### Website
- 🎯 **Minimalist Design**: Clean, professional aesthetic
- 📱 **Responsive**: Works on all devices
- ⚡ **Fast**: Built with Next.js 15
- 🎨 **Animated**: Smooth Framer Motion animations

## 🚀 Quick Start

### For Users
1. **Install the extension** from the [Chrome Web Store](https://chromewebstore.google.com/detail/docs-dark-20/djmmkojigpkdagglmjjdjiddopgdchcn)
2. **Visit Google Docs** and enjoy the dark theme
3. **Customize colors** using the extension popup

### For Developers
```bash
# Clone the repository
git clone https://github.com/ameyalambat/dark-docs-2.0.git
cd dark-docs-2.0

# Install dependencies
pnpm install

# Start development
pnpm dev
```

## 🏗️ Monorepo Structure

This project uses **Turborepo** with **pnpm** for optimal performance and developer experience.

```
docs-dark-chrome/
├── apps/
│   ├── extension/          # Chrome Extension
│   │   ├── src/           # Extension source files
│   │   ├── build_config.json
│   │   ├── package.js     # Build script
│   │   └── releases/      # Built ZIP packages
│   └── www/               # Next.js Website
│       ├── src/           # Website source
│       └── public/        # Static assets
├── packages/
│   ├── shared/            # Shared constants & utilities
│   └── ui/                # Shared UI components
├── turbo.json             # Turborepo configuration
├── pnpm-workspace.yaml    # pnpm workspace config
└── package.json           # Root dependencies
```

## 🛠️ Development

### Prerequisites

- **Node.js** >= 18.0.0
- **pnpm** (recommended) or npm

### Setup

1. **Clone the repository:**

```bash
git clone https://github.com/ameyalambat/dark-docs-2.0.git
cd dark-docs-2.0
```

2. **Install dependencies:**

```bash
pnpm install
```

### Build Commands

#### All Projects

```bash
pnpm turbo build        # Build all apps
pnpm turbo dev          # Run all apps in dev mode
pnpm turbo lint         # Lint all apps
pnpm turbo clean        # Clean all build artifacts
```

#### Chrome Extension Only

```bash
pnpm build:extension    # Build extension
pnpm dev:extension      # Build extension (same as build)
```

#### Website Only

```bash
pnpm build:www          # Build website
pnpm dev:www            # Run website dev server
```

### Development Workflow

1. **Start development servers:**

```bash
pnpm turbo dev
```

2. **For extension development:**
   - Make changes in `apps/extension/src/`
   - Run `pnpm build:extension`
   - Load `apps/extension/dist/chrome/` in Chrome developer mode

3. **For website development:**
   - Make changes in `apps/www/src/`
   - Visit `http://localhost:3000` (auto-reloads)

## 🌐 Multi-Browser Support

The extension build system creates browser-specific packages:

- **Chrome**: Manifest V3 with separate host permissions
- **Firefox**: Manifest V2 with combined permissions
- **Edge**: Manifest V3 (same as Chrome)
- **Opera**: Manifest V3 (same as Chrome)

Built packages are available in `apps/extension/releases/`:

- `dark-docs-2.0-chrome-v2.0.2.zip`
- `dark-docs-2.0-firefox-v2.0.2.zip`
- `dark-docs-2.0-edge-v2.0.2.zip`
- `dark-docs-2.0-opera-v2.0.2.zip`

## 🚀 Deployment

### Chrome Extension

```bash
pnpm build:extension
```

Upload the appropriate ZIP from `apps/extension/releases/` to browser stores.

### Website

```bash
pnpm build:www
```

Deploy `apps/www/.next/` to your hosting provider (Vercel, Netlify, etc.).

## 📦 Packages

- **@dark-docs/shared**: Shared constants, utilities, and brand colors
- **@dark-docs/ui**: Shared UI components (BackgroundLines, etc.)

## 🔧 Tech Stack

- **Monorepo**: Turborepo + pnpm
- **Extension**: Vanilla JS + CSS
- **Website**: Next.js 15 + TypeScript + Tailwind CSS + Framer Motion
- **Shared**: TypeScript + React

## 🤝 Contributing

We welcome contributions! Please see our [Contributing Guide](.github/CONTRIBUTING.md) for details.

### Quick Contribution Steps

1. **Fork** the repository
2. **Create** a feature branch: `git checkout -b feature/amazing-feature`
3. **Make** your changes
4. **Test** your changes: `pnpm build && pnpm lint`
5. **Commit** your changes: `git commit -m 'Add amazing feature'`
6. **Push** to your fork: `git push origin feature/amazing-feature`
7. **Create** a Pull Request

## 📋 Roadmap

- [ ] Additional theme variants
- [ ] Advanced customization options
- [ ] Performance optimizations
- [ ] Enhanced accessibility features
- [ ] Mobile app companion

## 🐛 Bug Reports & Feature Requests

- **Bug Reports**: Use the [Bug Report Template](.github/ISSUE_TEMPLATE/bug_report.md)
- **Feature Requests**: Use the [Feature Request Template](.github/ISSUE_TEMPLATE/feature_request.md)
- **General Questions**: [Open an issue](https://github.com/ameyalambat/dark-docs-2.0/issues)

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

- **Google Docs** for the amazing platform
- **Turborepo** for the excellent monorepo tooling
- **Next.js** for the powerful React framework
- **All contributors** who help make Dark Docs 2.0 better!

## 📊 Project Stats

![GitHub stars](https://img.shields.io/github/stars/ameyalambat/dark-docs-2.0)
![GitHub forks](https://img.shields.io/github/forks/ameyalambat/dark-docs-2.0)
![GitHub issues](https://img.shields.io/github/issues/ameyalambat/dark-docs-2.0)
![GitHub pull requests](https://img.shields.io/github/issues-pr/ameyalambat/dark-docs-2.0)

---

**Made with ❤️ by [Ameya Lambat](https://github.com/ameyalambat)**
