# Summit Resume Studio

A premium, single-file resume builder and cover-letter generator with a guided wizard, live preview, multiple visual schemas, and a built-in role-specific writing library.

## Overview

Summit Resume Studio is designed to help users move from rough career notes to a polished, professional application package in one place. The app combines structured form entry, recruiter-style coaching, example answers, role-family playbooks, layout switching, and print-ready output.

The project is intentionally delivered as a **single HTML file** so it can be dropped into a portfolio, shared quickly, or deployed without a build pipeline.

## Core capabilities

### Guided resume wizard
- Multi-step flow covering:
  - identity and targeting
  - summary writing
  - experience bullets
  - education and credentials
  - skills architecture
  - projects and proof points
  - differentiators
  - cover-letter generation
- Inline coaching on what strong answers look like
- Recruiter checks and example responses for each stage

### Role-aware writing support
- Role-family starter packs to tailor the experience for different career tracks
- Deep example-answer library matched to the selected role family and current step
- Writing prompts to help users extract better stories, metrics, and outcomes
- Bullet lab for turning rough notes into sharper accomplishment statements
- Cover-letter angle suggestions tied to the selected role track

### Resume generation and preview
- Live resume preview beside the editor
- Multiple preloaded resume schemas/layouts
- Theme-driven visual presentation without requiring content re-entry
- Print-friendly formatting for PDF export

### Cover-letter generator
- Generates a tailored draft from user profile, work history, target role, and company context
- Supports editable output so users can refine tone and specificity
- Includes role-aware prompts and reusable phrasing cues

### Utility features
- Local autosave using browser storage
- Resume text copy
- Cover letter copy
- JSON export of user-entered profile data
- Print / PDF generation

## Visual design

The interface uses a high-contrast, glassmorphism-inspired UI with an animated background featuring:
- mesh-grid mountain forms
- blurred lava-lamp style color motion
- layered gradients and atmospheric depth

This styling is intended to make the product feel premium while keeping the editor legible and task-focused.

## Tech stack

- **HTML** for the single-file shell
- **CSS** for layout, theming, motion, and print styling
- **JavaScript** for app logic and data handling
- **React** for component structure and state management
- **ReactDOM** for rendering
- **Babel (browser runtime)** for JSX transpilation in the single-file setup

## Architecture notes

This project is intentionally self-contained.

### Delivery model
- One HTML file contains the UI, styles, data structures, and app logic
- No bundler or external project structure is required to run it
- Suitable for demos, prototypes, portfolio artifacts, or static deployment

### Runtime behavior
- User content is stored in `localStorage`
- Resume and cover-letter content are generated client-side
- The preview updates immediately as form values change

### Content system
The app includes large embedded data structures for:
- role starter packs
- example-answer libraries
- recruiter guidance
- writing prompts and support content

These are built into the file so the product feels fully fleshed out without depending on an external backend.

## Getting started

### Option 1: Open directly
Open `resume_builder_wizard.html` in a modern browser.

### Option 2: Serve locally
For the most reliable local experience, serve the file from a small local web server.

Example with Python:

```bash
python -m http.server 8000
```

Then open the page in your browser through the local server.

## Usage flow

1. Open the app.
2. Choose a role family or apply a starter pack.
3. Work through the guided steps.
4. Use the example library and recruiter prompts to improve weak sections.
5. Select a resume schema.
6. Generate and edit the cover letter.
7. Print to PDF or copy/export your content.

## File contents

```text
resume_builder_wizard.html   # Complete application in one file
```

## Customization guide

### Add or change role families
Update the embedded role-pack and writing-library data structures in the script section.

### Add more layouts
Extend the layout preset definitions and add corresponding preview / render logic.

### Adjust branding
You can change:
- title text
- color variables
- gradients
- button styling
- layout card labels
- background animation tuning

### Modify export behavior
Print styling is handled in CSS. Resume / cover-letter export behavior can be extended in JavaScript.

## Strengths of this implementation

- very easy to distribute
- no build tooling required
- strong visual presentation
- live editing and preview in one interface
- role-aware guidance instead of generic empty forms
- good fit for demos, showcases, and MVP-style deployments

## Known considerations

- The app is a front-end artifact and does not include a backend or user accounts
- Data persists locally in the browser rather than in cloud storage
- Because the project uses browser-loaded React/Babel in a single-file format, it is best treated as a polished static application rather than a production-scale web platform foundation
- The file is intentionally large because it includes substantial embedded guidance and example content

## Browser expectations

Recommended for current versions of:
- Chrome
- Edge
- Firefox
- Safari

## Privacy

The current implementation stores entered information locally in the browser via `localStorage`. No server-side submission flow is included in this version.

## Future enhancement ideas

- DOCX export
- ATS scoring breakdowns by section
- job-description parsing and keyword weighting
- downloadable theme packs
- richer multi-page resume controls
- account sync / cloud persistence
- admin-editable content libraries
- AI-assisted rewrite suggestions backed by an API

## Positioning

Summit Resume Studio is best suited for:
- premium prototype delivery
- portfolio presentation
- recruiter-tech concept demos
- static hosting scenarios
- career tool MVPs that need strong UX and immediate utility

## License / ownership

Add your preferred license or internal ownership language here.

---

If you are packaging this for GitHub, a product demo site, or a client handoff, this README can also be adapted into:
- a shorter public README
- a technical implementation README
- a client-facing handoff document
