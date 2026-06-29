# Velorah — Hero Section

A single-page hero built with React + Vite + TypeScript + Tailwind CSS, using a
shadcn/ui `Button` (with an added `glass` variant) for the glassmorphic CTAs.

## Stack

- Vite + React + TypeScript
- Tailwind CSS (CSS-variable color tokens, shadcn/ui conventions)
- shadcn/ui `Button` component (`class-variance-authority`, `@radix-ui/react-slot`)
- Google Fonts: Instrument Serif (display) + Inter 400/500 (body)

## Run it

```bash
npm install
npm run dev
```

Then open the printed local URL (typically http://localhost:5173).

To produce a production build:

```bash
npm run build
npm run preview
```

## Structure

```
src/
  components/
    ui/button.tsx     shadcn/ui Button (default/secondary/ghost/link/glass variants)
    Navigation.tsx     glassmorphic nav bar
    Hero.tsx           cinematic hero copy + CTA
  App.tsx              fullscreen background video + composition
  index.css            theme tokens, .liquid-glass effect, fade-rise keyframes
```

## Notes

- The background video autoplays muted and loops (`autoPlay loop muted playsInline`),
  required for autoplay to work reliably across browsers.
- `.liquid-glass` is a plain CSS utility class (not a Tailwind plugin) defined in
  `src/index.css`, used on both CTA buttons.
- Entrance animations (`animate-fade-rise*`) respect `prefers-reduced-motion`.
