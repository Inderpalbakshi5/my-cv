# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a static portfolio website built with vanilla HTML, CSS, and JavaScript. The site is deployed on GitHub Pages and features a single-page application structure with smooth scrolling navigation between sections.

## Architecture

### File Structure
- `index.html` - Main HTML file containing all sections (Hero, About, Experience, Skills, Projects, Education, Contact)
- `styles.css` - Complete styling including responsive design, animations, and theme variables
- `script.js` - Client-side interactivity (navigation, animations, form handling, scroll effects)

### Key Architectural Patterns

**Single-Page Layout**: All content sections are in one HTML file with anchor-based navigation (#about, #experience, etc.). Navigation uses smooth scrolling with JavaScript.

**CSS Custom Properties**: Theme colors and common values are defined as CSS variables in `:root` for easy customization:
- `--primary-color: #2563eb`
- `--secondary-color: #1e40af`
- `--text-dark`, `--text-light`, `--bg-light`, etc.

**Responsive Strategy**: Mobile-first approach with hamburger menu that toggles at 768px breakpoint. Grid layouts use `grid-template-columns: repeat(auto-fit, minmax(...))` for automatic responsiveness.

**Animation System**:
- Intersection Observer API for fade-in animations on scroll
- CSS transitions for hover effects
- Keyframe animations defined in CSS (`@keyframes fadeInUp`)
- Custom counter animations for statistics

### Section Dependencies

The HTML sections are self-contained but share common styling patterns:
- `.section` class for all main sections with consistent padding
- `.section-alt` for alternating background colors
- `.section-title` with centered underline effect

## Deployment

This site is hosted on GitHub Pages from the `main` branch.

**Deploy Process**:
1. Make changes to HTML/CSS/JS files
2. Commit and push to `main` branch: `git push origin main`
3. GitHub Pages automatically rebuilds (2-3 minutes)
4. Live site: `https://inderpalbakshi5.github.io/my-cv/`

**No build process required** - this is pure static HTML/CSS/JS with no bundlers or preprocessors.

## Customization Points

When updating content, focus on these areas in `index.html`:
- Hero section: Name, title, social links (LinkedIn, email, phone)
- About section: Professional summary and statistics (years experience, workshops, prototypes)
- Timeline items (work experience): Each `.timeline-item` contains job details with company, dates, and achievements
- Skill categories: Each `.skill-category` with corresponding skill tags grouped by domain (AI Platforms, Generative AI, Automation, etc.)
- Project cards: Update `.project-card` elements - currently use text-only headers with FontAwesome icons (no images to avoid loading issues)
- Education cards: Degree information and certifications organized by category
- Contact section: Email, phone, location, LinkedIn details

**Project Cards Design**: Project cards use icon-based headers without images to ensure reliable display. Each card has:
- Title with FontAwesome icon
- Description paragraph
- Technology tags
- Achievement metrics

## JavaScript Features

All interactivity is in `script.js`:
- Mobile navigation toggle (hamburger menu)
- Smooth scroll with offset for fixed navbar (80px)
- Active navigation link highlighting based on scroll position
- Intersection Observer for scroll-triggered animations
- Counter animation for statistics
- Form submission handling (currently shows alert)
- Parallax effect on hero section
- 3D tilt effect on project cards

## Git Configuration

This repository uses:
- User: Inder (inderpalbakshi5@gmail.com)
- Remote: https://github.com/Inderpalbakshi5/my-cv.git
- Main branch: `main`
