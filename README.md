# Pakenham Solar &amp; Battery — rank-and-rent microsite

Astro static site, deployed to Netlify.

## What this is

A rank-and-rent lead-generation microsite for **solar panel &amp; battery installation**
services in Pakenham, Victoria. Ranks in Google for local "[solar Pakenham]"-type
searches, captures leads via the quote form + tracked phone number, forwards
them to a rented local contractor.

## Structure

```
src/
├── layouts/
│   └── Layout.astro          # Shared shell — schema, nav, footer, GA
├── pages/
│   ├── index.astro           # Homepage
│   ├── services/
│   │   ├── solar-panel-installation.astro
│   │   ├── battery-storage.astro
│   │   ├── solar-battery-systems.astro
│   │   ├── ev-charger-installation.astro
│   │   └── solar-repairs-servicing.astro
│   ├── officer.astro
│   ├── cardinia-lakes.astro
│   └── ... (suburb pages)
├── public/
│   ├── images/logo.svg
│   └── ...
└── package.json
```

## Local dev

```
npm install
npm run dev
```

## Deploy

Netlify auto-deploys from the `main` branch. Astro build → `dist/`.

`netlify.toml` defines the build command + publish dir.

## Environment variables (Netlify)

| Var | Example | Purpose |
|-----|---------|---------|
| `TENANT_BRAND` | `Pakenham Solar &amp; Battery` (default) | What plays after the label — full whisper is `"Pete's Lead. Pete's Lead from Pakenham Solar and Battery."` |
| `LEAD_FORWARD_TO` | `peter@yesai.au` | Where tracked-call leads forward |
| `WHISPER_LABEL` | `Pete's Lead` | Played to contractor before patching caller |

## Notes

- Phone (03) 9003 0108 is a Twilio tracking number → forwards to the rented contractor.
- Brand palette: navy #14304a + warm amber accent #f59e0b.
- All content is original, written for the Pakenham/Cardinia solar market.
```
