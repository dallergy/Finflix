# Finflix — Raptor

Cinematic custom CSS for **Jellyfin 12** (React / MUI layout) on the Raptor server. Forked from Abyss Net; login shows the **Raptor** wordmark and the branding splash, not the upstream theme name.

## Install

1. Open Jellyfin → **Dashboard → Branding → Custom CSS code**  
   (or **Settings → Display** for one user only)
2. Paste the contents of [`style.css`](./style.css)
3. Save, then hard-refresh the web client (`Ctrl/Cmd+Shift+R`)
4. Set **Display theme** to **Dark** and turn **Backdrops** on

Jellyfin 10.11+ does not load custom CSS on the admin dashboard. That is a server security choice, not a theme bug.

## What Apex changes

- Jellyfin 12 AppBar, toolbar, drawers, menus, chips, and tabs
- OLED black + nebula wash, glass chrome, red corona on poster hover
- Cinzel titles on the detail page, Orbitron section headers
- Login wordmark and glass sign-in card
- Keeps v2 fixes: full titles (no “The Bi…”), progress bars, TV focus, reduced motion

## Library notes

See [`LIBRARY.md`](./LIBRARY.md) for the full Raptor movie list and what to add next.
