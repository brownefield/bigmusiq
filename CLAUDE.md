# bigmusiq — Claude Code Operating Doctrine

## What bigmusiq Is
Unified music showcase for the artist **Teddy Browne**. Lives at bigmusiq.com. Deployed via Vercel. This is the artist-facing front door — distinct from Brownefield Holdings corporate properties.

It is not a label site, not a band site, not a press kit. It is a **listening room** organized into four thematic worlds, with a persistent player that follows the visitor across the site.

## Stack
- Static HTML site (no framework)
- Files: index.html, songtree.html, README.md
- Hosting: Vercel (auto-deploy on push to `main`)
- Repo: github.com/brownefield/bigmusiq
- Domain: bigmusiq.com
- Audio: SoundCloud Widget API (persistent player across sections)

## The Four Worlds (Locked Structure)
Each world is a section with its own theme, color treatment, and curated track list. Order is intentional — do not reorder without explicit instruction.

1. **Tidewater** — water-adjacent, reflective, drift, return
2. **Emberfall** — heat, falling light, intimacy, dusk
3. **Glasswater** — clarity, stillness, mirror, vulnerability
4. **Deepcurrent** — undertow, depth, conviction, pull

Plus the **Living Songtree** page (songtree.html) — a single connected view showing tracks as a growing structure rather than a static catalog.

## Artist Identity Rules
- **Artist name:** Teddy Browne (no "field" — that's the corporate side)
- **Hashtag:** `#hellagoodmusiq` — always with the **Q**, never `#hellagoodmusic`. Visually distinct, aurally identical. This is intentional and non-negotiable.
- **Do not blend** the artist identity (Teddy Browne) with the corporate identity (Theodore Brownefield / Brownefield Holdings) on this site. bigmusiq is the artist face only.
- **Faith content:** Some tracks are rooted in Scripture and Seventh-day Adventist 28 Fundamental Beliefs. Treat as serious work, not novelty.

## Design System
World palettes (placeholders — confirm before going to production; do not invent colors):
- **Tidewater:** cool tones, blue/green water tones — TBD
- **Emberfall:** warm tones, amber/rust/ember — TBD
- **Glasswater:** desaturated, pale, near-monochrome — TBD
- **Deepcurrent:** deep navy / near-black, low light — TBD

Typography: clean, restrained. Avoid trendy display fonts. Music is the point, not the chrome.
Aesthetic: minimal, symbolic, intentional. Same restraint as the rest of the Brownefield ecosystem. No clutter, no auto-playing video, no aggressive motion.

## SoundCloud Widget API Rules
- The player is **persistent** — it must survive section changes. Do not break that.
- Track URLs live in a **CONFIG block** inside index.html. When adding tracks, locate that block.
- **Audio slots are not live until SoundCloud URLs are pasted into CONFIG.** This is a known open item.
- When adding a new track: paste the SoundCloud share URL into the correct world's slot in CONFIG, commit, push. Do not embed URLs inline elsewhere.
- Never autoplay on initial page load. Visitor must initiate first play.

## Tone for Site Copy
- Track descriptions, world intros, about page → understated, evocative, image-led. Closer to liner notes than marketing copy.
- **Helm Voice applies** to all descriptive prose — grounded, calm, minimal, maritime-adjacent where natural.
- Avoid: spiritual clichés, generic "vibes" language, hype, exclamation points, em-dashes used as drama.
- **Suno AI** is a tool used in production. Do not advertise this on the site. The work stands on its own.

## Sonic / Creative Reference
- Piano-driven. Harmony and emotional depth are the priorities.
- Sonic reference for the faith material: Lauren Daigle, *Look Up Child* era.
- Soul and meaning over polish. If copy reduces the work to a genre tag, rewrite it.

## File Conventions
- index.html — main site (four worlds, persistent player)
- songtree.html — Living Songtree page
- README.md — repo readme
- Static assets (cover art, world imagery) — confirm folder structure on first edit

## Workflow Rules for Claude Code
1. **Always show diffs before applying.** Especially for anything that touches the persistent player or the four-worlds structure.
2. **Never reorder the four worlds** without explicit instruction. The sequence is doctrinal.
3. **Never push directly to `main` without explicit instruction.** Default to feature branches or staged commits awaiting approval.
4. **When adding tracks:** confirm which world the track belongs to before touching CONFIG. Ask if unclear.
5. **Preserve `#hellagoodmusiq` spelling** wherever it appears. Q, not C.
6. **Do not connect bigmusiq copy to Brownefield Holdings, FormBuddy, ApplyReady, or Waypoint OS.** This site is artist-only. Keep the lanes clean.

## Active Items (as of June 2026)
- SoundCloud track URLs still need to be pasted into CONFIG to make audio slots live
- Living Songtree page deployed
- Persistent SoundCloud Widget API player deployed
- Four-world structure deployed
- World-specific hex palettes need to be locked and added to this file

## Parent Architecture (Context, Not Content)
This site sits under Brownefield Holdings legally and operationally, but the **public-facing identity is Teddy Browne, artist**. The corporate architecture (Brownefield owns the keys. Waypoint defines the route. FormBuddy opens the door.) is **not surfaced on bigmusiq**. It informs how the site is built and maintained — it does not appear in the copy.

## Current Season
Bear season. Heads-down, pruning, building. Lion season — louder public-facing posture — is dormant. When Lion returns (after The Quartermaster publishes), bigmusiq's promotional posture may shift. Until then: build quietly.
