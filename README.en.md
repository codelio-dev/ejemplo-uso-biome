# Waku Starter with Biome

A minimal [Waku](https://waku.gg) starter template that demonstrates the integration of [Biome](https://biomejs.dev) as an all-in-one toolchain for linting, formatting, and import organization. This repository is the companion for the article [Biome: la navaja suiza de los toolchain para JavaScript/TypeScript](https://codel.io/articulos/biome-la-navaja-suiza-de-los-toolchain-para-javascript-typescript/).

> [Leer en español](README.md)

## Tech Stack

- **[Waku](https://waku.gg)** — Minimal React framework with file-based routing and static site generation
- **[React 19](https://react.dev)** — UI library with server and client components
- **[TypeScript](https://www.typescriptlang.org)** — Strict type-safe development
- **[Tailwind CSS 4](https://tailwindcss.com)** — Utility-first CSS framework
- **[Biome](https://biomejs.dev)** — Fast linter and formatter for JavaScript/TypeScript
- **[Vite](https://vite.dev)** — Build tool and dev server

## Project Structure

```
src/
├── components/
│   ├── counter.tsx      # Interactive client component (useState)
│   ├── header.tsx       # Navigation header
│   └── footer.tsx       # Footer with link to Waku docs
├── pages/
│   ├── _layout.tsx      # Root layout (header, footer, styles)
│   ├── index.tsx        # Home page (static render)
│   └── about.tsx        # About page (static render)
└── styles.css           # Tailwind CSS entry point

public/
├── images/
│   └── favicon.png
└── robots.txt

biome.json               # Biome configuration
tsconfig.json             # TypeScript configuration
waku.config.ts            # Waku/Vite plugins configuration
package.json
```

## Getting Started

### Prerequisites

- [Node.js](https://nodejs.org) (v18 or higher recommended) or [Bun](https://bun.sh)

### Installation

1. Clone the repository:

```bash
git clone https://github.com/codel-io/ejemplo-uso-biome.git
cd ejemplo-uso-biome
```

2. Install dependencies:

```bash
# npm
npm install

# pnpm
pnpm install

# yarn
yarn install

# bun
bun install
```

### Development

Start the development server:

```bash
# npm
npm run dev

# pnpm
pnpm run dev

# yarn
yarn run dev

# bun
bun run dev
```

## Available Scripts

| Script | Command | Description |
|--------|---------|-------------|
| `dev` | `waku dev` | Start the development server |
| `build` | `waku build` | Build for production |
| `start` | `waku start` | Start the production server |
| `format` | `biome format --write` | Format all files with Biome |
| `lint` | `biome lint --write` | Lint and auto-fix issues with Biome |
| `check` | `biome check --write` | Run all Biome checks (format + lint + imports) |

## See Results
Before running any Biome command, inspect the .ts/.tsx files in the project to see their default formatting. Then run the `check` command found below and review the files again — you will notice the formatting has changed. Additionally, it will show an error in the file src/components/counter.tsx indicating that the `<button>` element is missing the *type* prop, this is due to the rules that come configured by default. If you add the prop and run the command again, the error will disappear.

## Biome Configuration

Biome is configured in `biome.json` with the following settings:

- **Formatter** — Enabled with tab indentation and double quotes for JavaScript/TypeScript
- **Linter** — Enabled with recommended rules
- **Import Organization** — Automatically sorts and organizes imports
- **VCS Integration** — Git-aware, respects `.gitignore`

Run a full check across the project:

```bash
# npm
npm run check

# pnpm
pnpm run check

# yarn
yarn run check

# bun
bun run check
```

## License

[Unlicense](https://unlicense.org)

## Author

Sergio Gallardo - [codelio](https://codel.io)
