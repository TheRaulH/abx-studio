# WARP.md

This file provides guidance to WARP (warp.dev) when working with code in this repository.

## Project Overview

ABX-Studio is an Astro-based web application configured for deployment to GitHub Pages. The project uses TypeScript with Astro's strict configuration and targets the path `https://TheRaulH.github.io/abx-studio`.

## Common Commands

All commands are run from the root of the project:

- `npm install` - Install dependencies
- `npm run dev` - Start development server at `localhost:4321`
- `npm run build` - Build production site to `./dist/`
- `npm run preview` - Preview the production build locally
- `npm run astro` - Run Astro CLI commands (e.g., `npm run astro add`, `npm run astro check`)

## Architecture

### Project Structure

```
src/
├── assets/        # Static assets (SVG images)
├── components/    # Astro components
├── layouts/       # Page layout templates
└── pages/         # File-based routing pages
```

### Key Architectural Details

**Deployment Configuration**
- Site URL: `https://TheRaulH.github.io`
- Base path: `/abx-studio`
- Output directory: `./dist/`
- All URLs and paths must account for the base path prefix

**TypeScript**
- Uses Astro's strict TypeScript configuration (`astro/tsconfigs/strict`)
- Type definitions auto-generated in `.astro/types.d.ts`

**Component Architecture**
- Pages use the file-based routing system (files in `src/pages/`)
- Layout components provide HTML structure and global styles
- Component imports use relative paths
- Assets are imported as modules and accessed via `.src` property

**Styling**
- Styles are scoped to components using `<style>` tags in `.astro` files
- Global styles defined in `Layout.astro`
- No CSS preprocessor or framework currently configured

## Development Notes

- The project is configured for GitHub Pages deployment with a base path
- Astro 5.x is used (latest version at time of setup)
- VS Code is the recommended editor (extension: `astro-build.astro-vscode`)
- Launch configuration available for debugging the dev server in VS Code
