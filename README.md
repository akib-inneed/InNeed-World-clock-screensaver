# InNeed World Clock Screensaver

A full-screen, dual-timezone world clock and weather display, built as a screensaver for a 65" TV. Black background, InNeed Intelligent Cloud branding, and live weather.

- **Dhaka, Bangladesh** — Asia/Dhaka
- **Atlanta, Georgia** — America/New_York (Eastern Time)

## Features

- Live, second-by-second clock for both cities
- Live weather (Open-Meteo, no API key required), refreshed every 60 seconds
- Black background with InNeed's navy/blue/teal brand gradient
- Auto-hiding cursor and controls after a few seconds of inactivity
- Gentle periodic position shift to help prevent burn-in on OLED/LED TVs left on for long periods
- One-tap fullscreen toggle (top-right corner)
- Single self-contained file — no build step, no dependencies to install

## Deploying on Netlify

This is a static site with a single `index.html` at the repo root, so Netlify needs no build command.

1. In Netlify, choose **Add new site → Import an existing project**
2. Connect this GitHub repo (`InNeed-World-clock-screensaver`)
3. Leave **Build command** blank and **Publish directory** as `/` (repo root)
4. Deploy — Netlify will serve `index.html` directly

## Running it on the TV

1. Open the deployed Netlify URL in the TV's browser
2. Tap the small fullscreen icon in the top-right corner (or press F11 on a connected keyboard/remote with browser controls)
3. Leave it running — the clock, weather, and burn-in protection all run automatically with no further interaction needed

## Editing

- **Cities/timezones**: edit the `ZONES` and `PLACES` objects near the bottom of `index.html`
- **Weather refresh rate**: change the interval in the `setInterval(refreshWeather, ...)` call (currently 60 seconds)
- **Colors**: CSS custom properties (`--navy`, `--blue`, `--teal`, etc.) at the top of the `<style>` block
