# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is an Astro website project using Tailwind CSS for styling. The project is a personal website for Atticus Wang.

## Common Commands

### Development
- `npm run dev` - Start development server at localhost:4321
- `npm run build` - Build the production site to ./dist/
- `npm run preview` - Preview the build locally before deploying

### Astro CLI
- `npm run astro check` - Check project for TypeScript and other errors
- `npm run astro add` - Add integrations to the project

## Architecture

### Framework Setup
- **Astro** - Static site generator with component-based architecture
- **Tailwind CSS** - Configured via Vite plugin in astro.config.mjs
- **TypeScript** - Configured with strict mode via tsconfig.json

### Project Structure
- `src/pages/` - File-based routing for pages
- `src/components/` - Reusable Astro components
- `src/layouts/` - Page layout templates
- `src/styles/` - Global styles (includes Tailwind imports)
- `public/` - Static assets served directly

### Key Files
- `astro.config.mjs` - Main configuration file for Astro and integrations
- `src/styles/global.css` - Global CSS with Tailwind imports and Open Sans font
- `src/layouts/Layout.astro` - Base layout wrapper for pages
- `tailwind.config.mjs` - Tailwind configuration with Open Sans as default font

## Current Site Structure

### Pages
- `index.astro` - Homepage with bio, photo, and navigation (CV | Blog | GitHub | Projects)
- `blog.astro` - Blog page (currently shows "coming soon")
- `projects.astro` - Projects page with learning seminar notes and references

### Static Assets
- `public/cv.pdf` - CV document (linked from homepage)
- `public/profile.jpg` - Profile photo (referenced in homepage)  
- `public/projects/` - Directory containing PDF files for projects/notes

### Design Decisions
- **Font**: Open Sans throughout (configured in global.css and tailwind.config.mjs)
- **Navigation**: Pipe-separated links with subtle color hover effects
- **Photo**: Aspect ratio preserved, sized at w-56
- **Typography**: Left-aligned headings, consistent text-lg sizing for content
- **GitHub**: Links to https://github.com/chry-santhemum

### Deployment
- Deployed to Netlify with custom domain using Netlify nameservers