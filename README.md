# Waku Starter con Biome

Una plantilla inicial de [Waku](https://waku.gg) minimalista que demuestra la integración de [Biome](https://biomejs.dev) como herramienta todo-en-uno para linting, formateo y organización de imports. Este proyecto es el repositorio complementario del tutorial [Biome: la navaja suiza de los toolchain para JavaScript/TypeScript](https://codel.io/articulos/biome-la-navaja-suiza-de-los-toolchain-para-javascript-typescript/).

> [Read in English](README.en.md)

## Stack Tecnológico

- **[Waku](https://waku.gg)** — Framework React minimalista con enrutamiento basado en archivos y generación de sitios estáticos
- **[React 19](https://react.dev)** — Librería de UI con componentes de servidor y cliente
- **[TypeScript](https://www.typescriptlang.org)** — Desarrollo con tipado estricto
- **[Tailwind CSS 4](https://tailwindcss.com)** — Framework CSS basado en utilidades
- **[Biome](https://biomejs.dev)** — Linter y formateador rápido para JavaScript/TypeScript
- **[Vite](https://vite.dev)** — Herramienta de compilación y servidor de desarrollo

## Estructura del Proyecto

```
src/
├── components/
│   ├── counter.tsx      # Componente cliente interactivo (useState)
│   ├── header.tsx       # Encabezado de navegación
│   └── footer.tsx       # Pie de página con enlace a la documentación de Waku
├── pages/
│   ├── _layout.tsx      # Layout raíz (header, footer, estilos)
│   ├── index.tsx        # Página principal (renderizado estático)
│   └── about.tsx        # Página "Acerca de" (renderizado estático)
└── styles.css           # Punto de entrada de Tailwind CSS

public/
├── images/
│   └── favicon.png
└── robots.txt

biome.json               # Configuración de Biome
tsconfig.json             # Configuración de TypeScript
waku.config.ts            # Configuración de plugins Waku/Vite
package.json
```

## Primeros Pasos

### Requisitos Previos

- [Node.js](https://nodejs.org) (v18 o superior recomendado) o [Bun](https://bun.sh)

### Instalación

1. Clonar el repositorio:

```bash
git clone https://github.com/codel-io/ejemplo-uso-biome.git
cd ejemplo-uso-biome
```

2. Instalar dependencias:

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

### Desarrollo

Iniciar el servidor de desarrollo:

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

## Scripts Disponibles

| Script | Comando | Descripción |
|--------|---------|-------------|
| `dev` | `waku dev` | Iniciar el servidor de desarrollo |
| `build` | `waku build` | Compilar para producción |
| `start` | `waku start` | Iniciar el servidor de producción |
| `format` | `biome format --write` | Formatear todos los archivos con Biome |
| `lint` | `biome lint --write` | Analizar y corregir problemas con Biome |
| `check` | `biome check --write` | Ejecutar todas las verificaciones de Biome (formato + lint + imports) |

## Ver resultados

Antes de ejecutar algún comando de Biome revisa los archivos .ts/.tsx del proyecto para ver su formato por defecto. Luego ejecuta el comando `check` que encontrarás más abajo y vuelve a ver los archivos, notarás que el formato ha cambiado. Adicional te mostrará un error en el archivo src/components/counter.tsx indicando que el elemento `<button>` no tiene el prop *type*, esto es por las reglas que ya trae configurado por defecto. Si añades el prop y vuelves a ejecutar el comando el error desaparecera.

## Configuración de Biome

Biome está configurado en `biome.json` con los siguientes ajustes:

- **Formateador** — Habilitado con indentación por tabulaciones y comillas dobles para JavaScript/TypeScript
- **Linter** — Habilitado con reglas recomendadas
- **Organización de Imports** — Ordena y organiza los imports automáticamente
- **Integración con VCS** — Compatible con Git, respeta `.gitignore`

Ejecutar una verificación completa del proyecto:

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

## Licencia

[Unlicense](https://unlicense.org)

## Autor

Sergio Gallardo - [codelio](https://codel.io)
