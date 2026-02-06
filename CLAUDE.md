# CLAUDE.md

This file provides guidance for AI assistants working with this repository.

## Repository Overview

**Build a House** — a browser-based educational block-stacking game. Players drag and drop blocks labeled with construction trades (e.g., Foundation, Framing, Roofing) and stack them in the correct order to build a house.

Repository: `dylanhaan-dotcom/Test`

## Project Structure

```
/
├── CLAUDE.md       # AI assistant guidance (this file)
├── index.html      # Complete game — HTML, CSS, and JavaScript in a single file
└── .git/
```

## Tech Stack

- **Vanilla HTML/CSS/JavaScript** — no frameworks, no build step, no dependencies
- Single-file architecture: everything lives in `index.html`

## Development Setup

1. No install needed — just open `index.html` in a browser
2. Any modern browser with ES6 support works (Chrome, Firefox, Safari, Edge)

## How the Game Works

- **15 construction trade blocks** are shuffled in the "Block Yard"
- Players drag blocks to the "Build Site" and stack them bottom-to-top
- **Check Order** validates placement; correct blocks get green borders, wrong ones shake red
- **Hint** reveals which trade belongs in the first incorrect position
- **Reset** shuffles and restarts
- Tracks number of attempts

### Correct Build Order (bottom to top)

1. Site Preparation & Excavation
2. Foundation & Concrete
3. Framing
4. Roofing
5. Windows & Exterior Doors
6. Plumbing Rough-In
7. Electrical Rough-In
8. HVAC
9. Insulation
10. Drywall
11. Interior Finishes & Paint
12. Flooring
13. Cabinets & Countertops
14. Final Plumbing & Electrical
15. Landscaping & Exterior

## Code Conventions

- All code is in a single `index.html` file (inline `<style>` and `<script>`)
- CSS uses a mobile-friendly layout with flexbox
- Drag-and-drop uses the native HTML5 Drag and Drop API with touch fallbacks
- Colors are assigned per trade for visual distinction
- No external dependencies or CDN links

## Git Workflow

- Feature branches use the `claude/` prefix when created by AI assistants
- Commit messages should be clear and descriptive
- Push to the designated feature branch, not directly to `main`

## Important Notes for AI Assistants

- Read existing code before proposing changes
- This is a zero-dependency project — avoid adding frameworks or libraries unless explicitly requested
- Touch support is implemented alongside desktop drag-and-drop; keep both paths working
- The `TRADES` array defines game content and order — modify it to add/remove/reorder trades
- Test in a browser after making changes (no automated test suite)
