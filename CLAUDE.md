# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

**Waste Guardian** — Mobile-first food waste reduction app for Brazilian competition (Liga Jovem DLJ4). Two parallel implementations exist:

- `03_Arquitetura_Projeto/spa-workspace/` — Vanilla JS SPA (production deploy)
- `03_Arquitetura_Projeto/react-workspace/` — React + Vite prototype (development)

## Dev Commands

### spa-workspace (Vanilla JS — production)
No build step. Open `index.html` directly or deploy with Netlify CLI:
```bash
cd 03_Arquitetura_Projeto/spa-workspace
netlify deploy --prod --dir=.
```

### react-workspace (React — development)
```bash
cd 03_Arquitetura_Projeto/react-workspace
npm install          # install deps first
npm run dev          # dev server with HMR
npm run build        # production build
npm run preview      # preview production build
```

## Architecture

### spa-workspace (Vanilla JS)
Single-file architecture: `app.js` contains all logic (navigation, state machine for scanner, recipe modal, localStorage persistence, animations). Screen switching via CSS class toggling. Mock data embedded in JS.

Key patterns:
- **State machine** for scanner (`SCANNER_STATES`: idle → scanning → result/error)
- **Navigation**: `navigateTo(screenId)` hides all screens, shows target
- **Screen animations**: `triggerScreenAnimations()` applies stagger/count-up on screen entry
- **Focus trap** in recipe modal for accessibility
- **localStorage** persistence for user data

### react-workspace (React + Zustand)
- `src/App.jsx` — Router with Routes: `/splash`, `/home`, `/scanner`, `/receitas`, `/impacto`, `/doacao`, `/perfil`
- `src/screens/` — One file per screen (Splash, Home, Scanner, Receitas, Impacto, Doacao, Perfil)
- `src/stores/useAppStore.js` — Zustand store for global state
- Tailwind CSS + Framer Motion for styling/animations

## Key Implementation Notes

- All code/docs in **Portuguese** (Brazilian competition)
- No external API calls — mock data only
- Scanner simulates 95% success / 5% error rate with 1.5s delay
- Recipe modal supports keyboard navigation (Escape to close, Tab focus trap)
- `appState` object bridges context between screens (e.g., scanned product → receita/doação)