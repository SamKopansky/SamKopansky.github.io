# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a static personal portfolio website for Sam Kopansky, hosted on GitHub Pages at samkopansky.com. The site showcases professional experience, skills, hobbies, and personal projects through a clean, responsive single-page design.

## Architecture

**Static HTML/CSS Site**
- Single-page application with no JavaScript framework
- All content is in `index.html` - a single HTML file containing the entire site structure
- Styling is in `css/sam.css` - handles responsive layout, animations, and theming
- Images and assets are stored in the `images/` directory

**Design System**
- Color scheme: Dark green (#03400d) for primary text/header, light green (#ebfaed) for backgrounds
- Typography: "Bangers" font for headers (playful display font), "Libre Franklin" for body text (clean sans-serif)
- Responsive breakpoints at 640px and 480px for mobile devices

**Key Sections**
1. Title/Header - Site title with dark green background
2. About Me - Bio with profile picture, uses flexbox for responsive layout
3. The Deets - Three card layout (Work Experience, Skills, Hobbies) using shadow boxes
4. Personal Projects - Image gallery with hover descriptions (overlay effect)
5. Footer - Contact links and resume download

**Interactive Elements**
- Project gallery images show descriptions on hover (desktop) or tap (mobile) via CSS overlay with opacity transitions
- Floating head icons for visual interest
- Fade-in animation on the bio text (3s delay)

## Development Workflow

**Testing Changes**
- Open `index.html` directly in a browser to preview changes
- No build process or local server required for basic viewing
- For testing mobile responsiveness, use browser dev tools device emulation

**Deployment**
- Site is hosted on GitHub Pages from the `master` branch
- Push changes to `master` branch to deploy (automatic)
- Custom domain configured via `CNAME` file (samkopansky.com)

**Common Edits**
- Update work experience, skills, or hobbies: Edit the corresponding section in `index.html`
- Add/remove project images: Add image to `images/` directory and create new `.img-container` div in the projects section
- Update resume: Replace `images/SamKopanskyResume.pdf` with new file
- Change colors/fonts: Modify CSS variables and font imports in `css/sam.css`

## File Structure

```
/
├── index.html              # Main HTML file - all site content
├── css/
│   └── sam.css            # All styling and responsive design
├── images/                # Images, profile pic, resume PDF, favicon assets
├── CNAME                  # Custom domain configuration (samkopansky.com)
├── android-chrome-*.png   # PWA icons
├── apple-touch-icon.png   # iOS home screen icon
└── favicon.*              # Browser favicon files
```

## Important Conventions

**Image Management**
- Resume PDF must be named `SamKopanskyResume.pdf` (referenced in index.html:171)
- Profile picture is `sam_full_body.jpeg`
- Floating head icon is `samhead.png`
- Project images should be sized appropriately (350x350px display size)

**Accessibility**
- Images use descriptive `alt` and `aria-label` attributes
- Links have clear aria-labels where text isn't descriptive
- Responsive design ensures mobile usability

**Git Workflow**
- Main branch is `master` (not `main`)
- GitHub Pages deploys automatically from `master` branch
- Test locally before pushing to production
