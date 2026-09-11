# Install Finflix

Custom CSS for the Jellyfin **web client**. Nothing is installed on the server binary.

## Requirements

- Jellyfin **12** recommended (React / MUI layout). Older 10.x clients pick up the legacy selectors.
- Display **Theme: Dark**
- **Backdrops** on if you want cinematic detail pages

## Apply for everyone (admin)

1. Sign in as an administrator.
2. **Dashboard → Branding → Custom CSS code**
3. Paste the one-liner **or** the full [`finflix.css`](../finflix.css) file.

```css
@import url("https://cdn.jsdelivr.net/gh/dallergy/Finflix@main/finflix.css");
```

4. Save.
5. Hard-refresh the web app (`Ctrl` / `Cmd` + `Shift` + `R`), or sign out and back in.

## Apply for one user

**Settings → Display → Custom CSS code** — same paste. User CSS stacks with server branding CSS.

## Splash screen

**Dashboard → Branding** — upload a splash image. Finflix uses it on `#loginPage` via `url("/Branding/Splashscreen")`.

## Wordmark

Default login text is **Finflix**. To use your server name, add this *after* the import:

```css
:root {
  --fx-server-name: "Your Server";
  --fx-footer-text: "Your Server";
}
```

## Admin dashboard looks unthemed

On Jellyfin 10.11+, custom CSS is **not** injected into the admin dashboard. Home, libraries, detail, search, login, and the player still receive the theme.

## Updates

If you used the jsDelivr `@main` import, a hard refresh picks up new commits after they land on `main`. If you pasted the file, paste again from [`finflix.css`](../finflix.css).
