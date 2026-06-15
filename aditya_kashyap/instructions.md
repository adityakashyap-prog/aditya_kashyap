# WD-001: GameVerse - Discover, Track & Explore Gaming Worlds

**Category:** Web Development

---

## Context

GameVerse is a gaming discovery platform built for casual, PC, console, and mobile gamers aged 13–40 who want a centralized destination to explore, organize, and stay informed about game content. The platform is being built as a complete frontend MVP to demonstrate a premium gaming experience featuring curated collections, trending titles, wishlists, editorial content, and a Play Zone showcase previewing future browser-based gaming experiences. This is a frontend-only, client-side React application — no backend, no authentication, and no database are included in this scope.

This milestone covers the full MVP frontend build: all 13 sections and pages described in the scope of work. The platform targets web browsers (Chrome, Firefox, Edge, Safari — latest versions) and must be fully responsive across mobile, tablet, and desktop. Deployment target is Vercel.

---

## Project Information

| Field | Details |
|---|---|
| Project ID | WD-001 |
| Category | Web Development |
| Project Type | Gaming Discovery Web Platform (React SPA) |
| Client / Brand | GameVerse Interactive |
| Platform / Medium | React.js — Web Browser (Chrome, Firefox, Edge, Safari) |
| Deliverable Type | React Application Source Code + Vercel Deployment + GitHub Repository |
| Primary Goal | Build a responsive gaming discovery frontend with curated game browsing, Play Zone preview, wishlists, and editorial content, meeting the visual standards defined in "Visual & Technical Specs" below |

---

## Main Goal

Deliver a complete, fully responsive React.js frontend application for GameVerse Interactive that allows users to:

1. Browse and discover fictional game concepts across curated collections and genres.
2. Explore a Play Zone section showcasing three upcoming browser-based game concepts with "Coming Soon" modal interactions.
3. Save favorite games to a personal wishlist using browser local storage.
4. Explore gaming news, community content, and upcoming releases through a dark-themed interface meeting the design specifications below.

---

## About GameVerse Interactive

GameVerse Interactive is a gaming discovery platform company targeting gamers aged 13–40 across casual, PC, console, and mobile segments. The brand does not yet have an established digital presence — this project establishes its visual identity and web experience from the ground up.

**Brand tone:** dark background, dark futuristic, community-driven — achieved through the color palette, typography, spacing system, and visual hierarchy rules defined in "Visual & Technical Specs."
**Brand line / tagline:** `Discover, Track & Explore Gaming Worlds`

---

## Requirements

The freelancer will build a complete single-page React application covering all 13 sections listed below with a consistent dark futuristic theme, as defined precisely in "Visual & Technical Specs."

### Core Features

1. Responsive sticky navigation bar with all listed links and mobile hamburger menu.
2. Interactive hero carousel showcasing 3–5 featured fictional games with artwork, title, genre, rating, description, and an Explore button.
3. Horizontal card sliders for each curated collection (Editor's Picks, Story-Driven Adventures, Open World Experiences, Competitive Challenges, Community Favorites, Hidden Gems).
4. Visual genre grid displaying all 10 genres (Action, Adventure, RPG, Racing, Strategy, Sports, Simulation, Sci-Fi, Fantasy, Indie) using custom artwork cards.
5. Trending Arena section with tabs or filters for Trending, Community Favorites, Most Viewed, and Recommended.
6. Play Zone section showcasing 3 upcoming browser-based game concepts with "Coming Soon" modal popups on click.
7. New Horizons section showcasing newly released fictional game concepts.
8. Future Releases section with upcoming game cards showing release window, genre, and platform.
9. Game Details page (route-based) with overview, media gallery, community insights, and similar titles.
10. Wishlist Center using browser local storage — add, remove, and view saved games.
11. Gamer Profile page (frontend-only) displaying avatar, username, favorite genres, wishlist stats, and recently viewed games.
12. Newsroom page with sections for Industry Updates, New Announcements, Community Spotlights, and Feature Articles.
13. Community Hub page with popular discussions, community recommendations, trending topics, and featured games.

### Navigation

- Sticky navigation bar visible on all pages and scroll positions.
- Links: Discover, Collections, Genres, Community Hub, Newsroom, Support, Search, Wishlist, Profile.
- Responsive hamburger menu for mobile viewports.
- Search access from the nav bar (UI display — no backend search required).

### Game Cards

- Cover artwork (placeholder or AI-generated royalty-free images, per "UI Assets" specs below).
- Game title, genre tag, rating (numeric or star display), platform badge.
- Add to Wishlist button/icon on hover or always visible.

### Play Zone

- Dedicated homepage section showcasing 3 upcoming browser-based game concepts.
- Each card displays: game title, genre, description, and a "Coming Soon" status badge.

**Featured Play Zone Games:**

| Game | Genre | Description |
|---|---|---|
| Memory Matrix | Puzzle / Memory Challenge | Test your memory by repeating increasingly difficult patterns and sequences. |
| Quiz Quest | Trivia / Knowledge Challenge | Answer gaming-related trivia questions and test your gaming knowledge. |
| Cyber Runner | Endless Runner | Navigate a futuristic city while avoiding obstacles and collecting energy crystals. |

- Clicking any Play Zone game card triggers a modal popup with the following message:

  > **"Coming Soon**
  > This gaming experience is currently under development.
  > Stay tuned for future updates from GameVerse."

- Modal must include a close button or dismiss-on-overlay-click behavior.
- No actual playable game logic is implemented in this scope.

### Wishlist

- Persist wishlist state in browser local storage.
- Add and remove games from any game card or the details page.
- Wishlist page lists all saved games with removal option.

### Game Details Page

- Route: `/game/:id`
- Sections: Overview (title, description, genre, release info, platforms), Media Gallery (screenshots/artwork — see "Data" below for the exact count required per game), Community Insights (rating summary, featured reviews — static data), Similar Titles (related game cards).

### Data

- All game data sourced from local JSON files (no external API calls required).
- Exactly 10 fictional game concepts, no more and no fewer, using this approved list (final source of truth — no other game list applies):

| # | Title | Genre |
|---|---|---|
| 1 | Shadow Protocol | Action |
| 2 | Void Hunters | Action |
| 3 | Eternal Realms | RPG |
| 4 | Arcane Empire | RPG |
| 5 | Neon Drift | Racing |
| 6 | Velocity Rush | Racing |
| 7 | Project Titan | Strategy |
| 8 | Mystic Legends | Adventure |
| 9 | Crimson Horizon | Open World |
| 10 | Cyber Outbreak | Sci-Fi |

- Play Zone games (Memory Matrix, Quiz Quest, Cyber Runner) stored as a separate JSON entry with `status: "coming_soon"`.
- Each of the 10 game entries must include: id, title, genre, description, rating, platform(s), release date/window, cover image, a `screenshots` array containing **exactly 4 screenshot image references** (used to populate the Game Details Media Gallery), and related game IDs.
- Newsroom JSON must include **at least 2 entries per sub-section** (Industry Updates, New Announcements, Community Spotlights, Feature Articles) — minimum 8 entries total, using static placeholder editorial content written for this project.

### Animations & Interactions

- Page transitions and element entrance animations using Framer Motion.
- Swiper.js for all horizontal card sliders and the hero carousel.
- Hover states on cards (scale, glow, overlay).
- Modal open/close animation using Framer Motion.
- Smooth scrolling behavior.

---

## Visual & Technical Specs

### Dimensions / Sizing

- **Breakpoints:** Mobile ≥ 320px, Tablet ≥ 768px, Desktop ≥ 1280px
- **Hero Section:** Full viewport width, minimum 500px height on desktop
- **Game Cards:** 280px × 380px on desktop; fluid/responsive on smaller screens
- **Play Zone Cards:** 300px × 400px on desktop; fluid/responsive on smaller screens
- **Modal:** Centered, max-width 480px, with semi-transparent dark overlay
- **Color mode:** sRGB

### Spacing System (defines "clean" and "premium" layout)

- **Base spacing unit:** 8px. All margins, paddings, and gaps must be multiples of 8px (8, 16, 24, 32, 40, 48, 64...).
- **Section vertical padding:** minimum 64px (top + bottom) on desktop (≥1280px), minimum 40px on tablet (≥768px), minimum 24px on mobile (≥320px).
- **Grid/card gutters:** minimum 16px between cards on mobile, minimum 24px on tablet and desktop.
- **Content max-width:** page content container max-width 1440px, centered, with minimum 16px side padding on mobile and 24px+ on larger screens.

### Typography

| Usage | Font | Notes |
|---|---|---|
| Headings / Display | Orbitron (Bold, ExtraBold) | All caps acceptable for section titles |
| Body / UI | Poppins (Regular, Medium, SemiBold) | Used for descriptions, labels, nav items, modal text |

Both fonts must be loaded via Google Fonts.

**Not allowed:** System default fonts as primary UI fonts, serif fonts, handwritten or brush fonts.

**Typographic hierarchy (defines "visual hierarchy" requirement):**
- H1 (page/hero titles): font-size ≥ 2.5x the body text font-size.
- H2 (section titles): font-size ≥ 1.75x the body text font-size.
- H3 (card/sub-section titles): font-size ≥ 1.25x the body text font-size.
- Body text baseline: 16px on desktop/tablet, minimum 14px on mobile.

### Colors

| Purpose | Color Name | Hex |
|---|---|---|
| Primary | Electric Violet | `#7C3AED` |
| Secondary / Background | Dark Navy | `#111827` |
| Accent | Cyan | `#06B6D4` |
| Surface / Card BG | Deep Gray | `#1F2937` |
| Text Primary | White | `#FFFFFF` |
| Text Secondary | Muted Gray | `#9CA3AF` |

**Color rules:**
1. Primary (`#7C3AED`) is used for CTAs, active states, highlights, and key UI elements.
2. Accent (`#06B6D4`) is used for badges, secondary highlights, and hover glows.
3. Background surfaces must remain dark (`#111827` or `#1F2937`) — no light-mode treatment.
4. Gradients using the primary and accent colors are permitted for hero artwork overlays and section transitions.
5. Modal overlay background: `rgba(0, 0, 0, 0.75)`.

---

## Technical Requirements

- **Framework:** React.js (Create React App or Vite)
- **Language:** JavaScript (ES6+)
- **Styling:** SCSS / CSS3 (CSS Modules or global SCSS with BEM)
- **UI Libraries:** React Icons, Swiper.js, Framer Motion
- **Data:** Local JSON files (no external API calls)
- **Storage:** Browser Local Storage (wishlist persistence only)
- **Routing:** React Router DOM v6
- **Version Control:** GitHub (public repository)
- **Deployment:** Vercel
- **Browser Support:** Chrome, Edge, Firefox, Safari — latest versions
- **Code quality:** each component file under 200 lines, all hex values stored in SCSS variables sensibly organized folder structure

### Allowed Tech Stack

1. React.js (CRA or Vite)
2. SCSS / CSS3
3. React Icons, Swiper.js, Framer Motion, React Router DOM v6
4. Local JSON for data
5. Browser Local Storage

### Not Allowed

- Backend servers, databases, or authentication systems
- Paid UI component libraries or premium plugins
- Hardcoded game data inside components (must use JSON files)
- Actual playable game logic or game engines (Play Zone is display + modal only)
- Direct copying of layouts or branding from existing gaming platforms (Steam, Epic, IGN, etc.)

---

## Design Direction

**Do:**
- Use dark, atmospheric backgrounds with subtle texture or gradient overlays.
- Apply glowing border effects or neon-style highlights on hover using the accent color.
- Use bold, large typography for section headings (Orbitron), following the Typographic Hierarchy rules above.
- Apply the 8px Spacing System above to create visual breathing room and hierarchy through size, brightness, and spacing.
- Use card-based layouts with rounded corners and drop shadows.
- Style Play Zone cards with a distinct "locked/coming soon" visual treatment (e.g., muted overlay, lock icon, status badge).
- Keep the modal clean, centered, and consistent with the dark theme.

**Do not:**
- Use white or light backgrounds anywhere on the platform.
- Use flat or overly minimal design that doesn't reflect gaming aesthetics.
- Copy specific layout structures from Steam, Epic Games Store, or IGN.
- Use realistic photographs of real games, real people, or copyrighted characters.
- Use AI-generated imagery of real branded content or IP.
- Make Play Zone cards look interactive/playable — they must clearly communicate "Coming Soon."
- Use spacing, margins, or paddings that violate the 8px Spacing System above.

---

## Reference Materials

| Asset | Details |
|---|---|
| Approved Game List | See "Data" section above — exactly 10 fictional games, this is the complete and final list |
| Play Zone Game List | Memory Matrix, Quiz Quest, Cyber Runner — all `status: coming_soon` |
| Color Palette | As defined in "Visual & Technical Specs" above |
| Spacing System | As defined in "Visual & Technical Specs" above |
| Typographic Hierarchy | As defined in "Visual & Technical Specs" above |
| Font References | Google Fonts — Orbitron, Poppins |

**How to use these references:** This instruction.md is the complete and self-contained specification for this project — no external brief, document, or link needs to be consulted. All artwork should be original, AI-generated royalty-free, or custom-designed. No copyrighted or licensed game assets may be used. Where any two requirements appear to conflict, the more specific numeric/technical constraint takes priority.

---

## Deliverables

| # | Item | Format | Notes |
|---|---|---|---|
| 1 | Complete React Application Source Code | `.zip` / GitHub Repo | Organized folder structure, commented code |
| 2 | Live Vercel Deployment | URL | Fully functional, publicly accessible |
| 3 | GitHub Repository | URL | Public repo with clean commit history |
| 4 | Local JSON Data Files | `.json` | Exactly 10 fictional games + 3 Play Zone entries + Newsroom data (minimum 8 entries) |
| 5 | UI Assets — Game Cover Images | `.png` or `.jpg` | Exactly 10 images (1 per game), minimum 1200×675px, optimized to under 300KB each |
| 6 | UI Assets — Game Screenshots | `.png` or `.jpg` | Exactly 4 per game (40 total), minimum 1280×720px each, for the Media Gallery |
| 7 | UI Assets — Play Zone Artwork | `.png` or `.jpg` | Exactly 3 images (1 per Play Zone game), minimum 1200×675px |
| 8 | UI Assets — Genre Grid Artwork | `.png` or `.jpg` | Exactly 10 images (1 per genre), minimum 800×800px |
| 9 | Project Documentation | `README.md` | Setup, run, build, and deployment instructions |

Icons used in the UI (navigation, buttons, badges, etc.) must be sourced from the React Icons library specified in Technical Requirements — no separate custom icon files are required as deliverables.

### File Naming Convention

All delivered files must follow this exact pattern:

```
[PREFIX]_[item-name]_[version]_[YYYY-MM-DD].[ext]
```

**PREFIX is always `GV`** for every delivered file (source code archive, documentation, and any other named deliverable artifacts).

**Example:** `GV_source-code_v1-0_2026-06-20.zip`

Rules:
- PREFIX is always `GV`.
- Use lowercase kebab-case.
- No spaces.
- No alternate naming structures.

This naming convention applies to packaged/named deliverable files (e.g., the source code ZIP, documentation export). Individual UI asset files inside the project's folder structure (e.g., `src/data/games.json`, image files inside `public/assets/images/`) follow the Folder Structure below and standard descriptive lowercase-kebab-case names (e.g., `shadow-protocol-cover.jpg`), not the `[PREFIX]_...` pattern.

### Folder Structure

```
GameVerse/
  public/
    assets/
      images/
      icons/
  src/
    components/
      common/
      layout/
      PlayZone/
    pages/
    data/
      games.json
      playzone.json
      news.json
      collections.json
    styles/
      variables.scss
      global.scss
    hooks/
    utils/
  README.md
  package.json
```

---

## Scope Boundaries

### DO
- Build all 13 sections/pages described in the scope of work.
- Build the Play Zone section with 3 game cards and "Coming Soon" modal popups.
- Use the 10 fictional game concepts listed in the "Data" section above — do not introduce real game titles or additional/fewer games.
- Use placeholder or royalty-free/AI-generated artwork for all game covers, screenshots, and banners, per the "UI Assets" specs in Deliverables.
- Implement the wishlist using browser local storage.
- Build a fully responsive layout for mobile, tablet, and desktop.
- Apply the Spacing System and Typographic Hierarchy rules from "Visual & Technical Specs" throughout.
- Deploy to Vercel and push source code to a public GitHub repository.

### DO NOT
- Build any backend, API, database, or server-side functionality.
- Implement real user authentication, user accounts, or session management.
- Build actual playable games — Play Zone is a showcase/preview section with modal only.
- Build real browser-based games, gaming challenges, or event calendars (listed as future expansion — out of MVP scope).
- Use copyrighted game artwork, branding, logos, or characters.
- Use paid plugins, libraries, or assets.

---

## Tool Requirements

- **Required tools:** VS Code or equivalent, Node.js (v18+), npm or yarn, Git
- **Acceptable alternatives:** Any code editor; Vite as an alternative to CRA
- **Forbidden:** Premium React component libraries (MUI Pro, AG Grid Enterprise, etc.), game engines (Phaser, Three.js for gameplay, Unity WebGL)

---

## Quality Control / Pre-Submission Checklist

Before submitting, confirm all of the following:

1. [ ] All 13 sections/pages are built and functional.
2. [ ] No console errors or broken links on any page.
3. [ ] Play Zone section displays all 3 game cards (Memory Matrix, Quiz Quest, Cyber Runner).
4. [ ] Clicking any Play Zone card opens the "Coming Soon" modal correctly.
5. [ ] Modal closes on button click and on overlay click.
6. [ ] Wishlist add/remove/persist works correctly via local storage.
7. [ ] Game Details page loads correctly for each game via route, with exactly 4 screenshots per game in the Media Gallery.
8. [ ] Responsive layout verified on mobile (≥320px), tablet (≥768px), and desktop (≥1280px).
9. [ ] All fictional game data is loaded from JSON files — not hardcoded in components.
10. [ ] All fonts (Orbitron, Poppins) load correctly, with H1/H2/H3 sizes matching the Typographic Hierarchy ratios.
11. [ ] Color palette matches the approved hex codes throughout.
12. [ ] All spacing, margins, and gutters follow the 8px Spacing System.
13. [ ] Exactly 10 game concepts present (no more, no fewer), matching the approved list exactly.
14. [ ] All named deliverable files follow the required `GV_` naming convention.
15. [ ] GitHub repository is public with a clean commit history.
16. [ ] Vercel deployment URL is live, publicly accessible, and error-free.
17. [ ] README.md includes setup, run, build, and deployment instructions.

---

## Acceptance Checklist

The delivery is complete only if every item passes:

1. [ ] All 13 platform sections render with no layout breaks at any of the three defined breakpoints (320px, 768px, 1280px) — "no layout break" means: no horizontal scrollbar, no text or interactive element clipped or overlapping its container, and no element extending outside its parent container at 100% browser zoom.
2. [ ] Hero carousel auto-plays and supports manual navigation with at least 3 featured games.
3. [ ] All collection sliders scroll horizontally with Swiper.js.
4. [ ] Play Zone section displays all 3 game cards with correct title, genre, and description.
5. [ ] "Coming Soon" modal appears on clicking any Play Zone card and dismisses correctly.
6. [ ] Wishlist persists correctly across browser refresh using local storage.
7. [ ] Game Details page displays full information for every one of the 10 games in the JSON file, including exactly 4 screenshots each.
8. [ ] Framer Motion animations are present on page transitions, card entrances, and modal open/close.
9. [ ] No real game titles, copyrighted artwork, or licensed IP appears anywhere.
10. [ ] Live Vercel URL is functional with no 404s or build errors.
11. [ ] Source code is organized per the specified folder structure.
12. [ ] README covers all steps to run the project locally.
13. [ ] All margins, paddings, and gaps are multiples of 8px per the Spacing System.
14. [ ] H1/H2/H3 heading sizes follow the Typographic Hierarchy ratios (≥2.5x / ≥1.75x / ≥1.25x body text).

---

## Evaluation Criteria

- **Visual Quality:** Dark futuristic theme is applied consistently across all pages, using the specified color palette, the 8px Spacing System, and the Typographic Hierarchy ratios defined in "Visual & Technical Specs."
- **Responsiveness:** Layout adapts correctly to mobile, tablet, and desktop without overflow or broken elements (per the "no layout break" definition in the Acceptance Checklist).
- **Feature Completeness:** All 13 sections and pages are present and functional including the Play Zone.
- **Play Zone Implementation:** Cards are visually distinct with a "coming soon" treatment; modal is smooth, dismissible, and uses the specified colors/typography.
- **Code Quality:** Components are clean, reusable, and logically organized; SCSS variables used for theming; no hardcoded values scattered in components.
- **Data Architecture:** All game and Play Zone content driven by local JSON files, with exactly 10 games and 3 Play Zone entries.
- **Wishlist Functionality:** Add, remove, and persistence work correctly and consistently across pages.
- **Animation Quality:** Swiper.js sliders, Framer Motion transitions, and modal animations are present on every page transition, card entrance, and modal open/close.
- **Originality:** No real game IP, no copied platform layouts, all artwork is royalty-free or original.

---

## Designer's / Developer's Choices

| Decision | Accepted Options |
|---|---|
| Build tool | Create React App, Vite |
| SCSS approach | CSS Modules + SCSS, Global SCSS with BEM |
| Card hover style | Scale + glow, overlay + button reveal |
| Hero carousel style | Auto-play with dots, auto-play with thumbnails |
| Genre section layout | Grid cards, horizontal scroll row |
| Play Zone card style | Muted overlay with lock icon, dimmed with status badge |
| Modal dismiss behavior | Close button only, close button + overlay click |
| Image sourcing | AI-generated royalty-free, custom-designed placeholders |

---

## Delivery Terms

- **Revisions included:** 1 round of minor revisions after delivery
- **Allowed revision types:** Color adjustments, text/copy changes, card layout tweaks, spacing corrections, modal copy changes
- **What does not count as a revision:** Adding new pages or sections, changing the tech stack, redesigning the overall theme, implementing backend features, building actual playable games
- **Delivery method:** GitHub repository link (public) + live Vercel URL + ZIP of source code (if requested); delivery within the agreed 7–10 day timeline

---

## Final Goal

The completed GameVerse platform should meet the Acceptance Checklist and Evaluation Criteria above in full: a consistent dark futuristic identity built on the specified color palette, 8px spacing system, and typographic hierarchy; smooth Framer Motion and Swiper.js animations on every page transition, card entrance, and modal interaction; and fully responsive, layout-break-free browsing across mobile, tablet, and desktop. A gamer visiting the site should be able to explore curated game collections, click into individual game details, save favorites to a wishlist, browse genres, read editorial content, and encounter the Play Zone section that teases exciting upcoming browser-based experiences with a "Coming Soon" modal — all without encountering broken layouts, console errors, or placeholder states.
