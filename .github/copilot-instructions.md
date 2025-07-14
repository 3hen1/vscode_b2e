# Copilot Instructions for VSCode IDE Slides Project

## Project Overview
This is a **Slidev presentation** about "VSCode IDE from Beginner to Expert" using a custom theme based on Seriph. The project uses Vue 3, TypeScript, and deploys to GitHub Pages with automated CI/CD.

## Architecture

### Key Components
- **`slides.md`**: Main presentation content using Slidev markdown syntax with frontmatter
- **`theme/`**: Custom Slidev theme extending @slidev/theme-seriph
  - `layouts/`: Custom Vue layout components (iframe-left-fixed.vue, fact.vue, etc.)
  - `styles/`: Theme-specific CSS (layouts.css, prism.css)
  - `layoutHelper.ts`: Utility functions for background handling and asset URL resolution
- **`components/`**: Reusable Vue components (Counter.vue)
- **`snippets/`**: External code snippets referenced in slides

### Layout System
Slidev uses layout-based slides. Available layouts in this theme:
- `iframe-left-fixed`: Split layout with scaled iframe on left, content on right
- `fact`, `intro`, `quote`, `section`, `statement`: Content-focused layouts
- `two-cols`, `two-cols-header`: Multi-column layouts
- `center`, `full`: Basic positioning layouts

## Development Workflow

### Commands
- **Development**: `pnpm dev` (opens browser automatically)
- **Build**: `pnpm build` (outputs to `dist/`)
- **Export**: `pnpm export` (generates PDF/images)
- **Theme Eject**: `pnpm theme:eject` (extracts theme for customization)

### Hot Reloading
Edit `slides.md` for instant preview updates. Theme changes in `theme/` require restart.

## Project-Specific Patterns

### Slide Frontmatter Structure
```yaml
---
layout: iframe-left-fixed
url: https://example.com
width: 1280
height: 800
scale: 0.3828  # Transform scale for iframe
---
```

### Custom Layout Props
- `iframe-left-fixed.vue` expects: `url`, `width`, `height`, optional `scale`
- Uses `transform: scale()` with `transformOrigin: 'left center'` for proper scaling
- Grid-based layout: `grid-cols-2` for split view

### Asset Handling
- `layoutHelper.ts` provides `resolveAssetUrl()` for proper base path handling
- `handleBackground()` supports colors, gradients, and images with optional dimming
- Base URL configured in `vite.config.ts` as `/vscode_b2e/` for GitHub Pages

### Styling Conventions
- Uses UnoCSS/Tailwind classes in templates
- Scoped `<style>` blocks for component-specific styles
- Theme styles in `theme/styles/` override default Slidev styles

## Deployment Configuration

### Multi-Platform Deployment
- **GitHub Pages**: Via `.github/workflows/deploy.yml` with pnpm build
- **Netlify**: Via `netlify.toml` with npm build command
- **Vercel**: Via `vercel.json` with SPA rewrites
- All configs set `dist/` as output directory

### Environment Variables
- `BASE_URL` set to `/vscode_b2e/` in GitHub Actions
- Asset URLs automatically prefixed via `resolveAssetUrl()`

## Development Tips

### Adding Custom Layouts
1. Create Vue component in `theme/layouts/`
2. Use `<slot />` for slide content insertion
3. Import layout utilities from `../layoutHelper.ts`
4. Reference by filename in slide frontmatter

### Code Snippets Integration
- External snippets in `snippets/` can be imported: `<<< @/snippets/external.ts#snippet`
- Use `#region snippet` and `#endregion snippet` to define importable sections

### Theme Customization
- Colors via `themeConfig.primary` in slides frontmatter
- Fonts configured in `theme/package.json` slidev.defaults
- CSS customization in `theme/styles/layouts.css`

### languages
- All in English, comments can be in Chinese