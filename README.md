# Pump Times

A tiny Jekyll site for GitHub Pages, with a pink-and-purple cowboy theme. Log a pump and it shows the next pumps
every 3 hours until 5:00 PM, with a live countdown to the next one.

## Files

- `_config.yml` – site title, pump interval, and cutoff time
- `index.html` – the page
- `apple-touch-icon.png` – the iPhone home-screen icon (180×180)
- `assets/app.js` – schedule and countdown logic
- `assets/cowboy.svg` – the cowboy background tile
- `assets/style.css` – styling (follows light/dark mode)

## Publish on GitHub Pages

1. Create a new repository on GitHub (for example `pump-times`) and upload these files, keeping the folder structure.
2. Go to **Settings → Pages**, set the source to **Deploy from a branch**, pick `main` and `/ (root)`, and save.
3. After a minute, the site is live at `https://<your-username>.github.io/pump-times/`.

## Change settings

Edit `_config.yml`:

```yaml
pump:
  interval_hours: 3
  cutoff: "17:00"
```

Decimals work for the interval (for example `2.5`).

## Notes

There's no password on this site, so anyone with the link can open it.
Pumps are saved in the browser you log them in (localStorage), so each phone
or computer keeps its own log. The log is stored separately from the Bottle
Times site, so the two won't interfere even on the same domain.
