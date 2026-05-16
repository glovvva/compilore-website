# compilore-landing

Landing page for compilore.pl — static single-file HTML.

## Stack
- Single HTML file (index.html)
- All CSS inline in `<style>`
- All JS inline in `<script>`
- Deployed via Coolify → nginx:alpine on Hetzner (89.167.98.1)
- Auto-deploy: git push origin master → Coolify webhook

## Files
- index.html — production landing page
- compilore-logo.png — logo (PNG, requires transparent bg for nav use)
- compilore-logo-horizontal.jpg — horizontal variant
- compilore-logo-small-app.jpg — app icon variant
- compilore-logo-vertical.jpg — vertical variant

## Deploy
```
git add index.html
git commit -m "description of change"
git push origin master
```

Coolify auto-deploys within 1-2 minutes.

## DNS
compilore.pl → A record → 89.167.98.1 (DNS only, no Cloudflare proxy)
www.compilore.pl → same

SSL handled by Traefik + Let's Encrypt on Hetzner.

## Email
bartek@compilore.pl → Cloudflare Email Routing → bartek@gaproll.eu

## Known issues
- Logo PNG has black background — requires transparent PNG or SVG 
  for proper nav display. Currently using text wordmark as fallback.
- YouTube URL ingest generates wiki about YouTube platform 
  (not video content) — landing page does not mention YouTube ingest.

## Section structure
1. Hero — TWOI LUDZIE WIEDZĄ. TWOJA FIRMA — NIE.
2. Problem — 3 sytuacje (handlowiec, onboarding, odejście pracownika)
3. Jak to działa — vertical timeline 4 steps
4. Różnica — cost-of-status-quo asymmetric layout
5. Co Compilore Potrafi — 6-card features grid
6. Knowledge Protection — transfer wiedzy stats
7. AI Foundation — signal/noise animated diagram
8. Dla kogo — 4 industry cards
9. Odbiorcy technologii — TRL 7+, pilotaż B2B
10. Waitlist / Pilot form — client-side success state
11. Footer — NIP/KRS/adres + privacy modal
