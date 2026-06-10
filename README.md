# BIG MUSIQ

The music site for Big Musiq — a living archive at [bigmusiq.com](https://bigmusiq.com).

## What's in here

| File | What it is |
|---|---|
| `index.html` | The main site. Library grouped by four worlds, persistent SoundCloud player, featured single ("The Beacon"). |
| `songtree.html` | The Living Songtree — a 45-minute synchronized ambient experience. Globally clocked, fourteen world-segments, optional Web Audio drone. |
| `README.md` | This file. |

Both pages are single, self-contained HTML files. No build step. No backend. No dependencies beyond Google Fonts and the public SoundCloud Widget API.

---

## Adding music to the main site

Open `index.html` in any text editor. Scroll to the comment that says:

```
===================== CONFIG BLOCK =========================
```

Three things you can edit:

**1. The Beacon** — your featured single. Edit the `BEACON` object:
```js
const BEACON = {
  title:  "Open Water",
  status: "coming soon",       // or "out now" once released
  world:  "tidewater",         // tidewater | emberfall | glasswater | deepcurrent
  daw:    "Logic Pro",
  note:   "First light. The one going to streaming.",
  scUrl:  "",                  // paste your SoundCloud URL here
  links: [                     // streaming links — use "#" until live
    { label:"Spotify",     href:"#" },
    { label:"Apple Music", href:"#" },
    { label:"iTunes",      href:"#" },
    { label:"YouTube",     href:"#" },
  ],
};
```

**2. Tracks** — the full library. Each line in the `TRACKS` array is one song:
```js
{ title:"Salt & Cedar", world:"tidewater", daw:"Logic Pro", status:"demo", scUrl:"" },
```
- `title` — what shows on the page
- `world` — which color palette / theming
- `daw` — Logic Pro or FL Studio (shows as metadata)
- `status` — `released` | `demo` | `idea` | `coming soon`
- `scUrl` — paste a SoundCloud track URL. Empty = grayed out, unclickable.

To add a song: copy a line, change the values. To remove one: delete the line.

**3. Worlds** — colors and labels. The `WORLDS` object controls the palette for each world. Edit hex values to retune the look.

---

## Editing the Songtree

Open `songtree.html`. Scroll to:

```
===================== CONFIG ===============================
```

The `SEGMENTS` array defines the fourteen world-segments and their scripture anchors. Each segment has:

- `name` — section title
- `mood` — color theme key
- `dur` — duration in seconds (the total of all `dur` values is the full piece length)
- `anchor` — short verse fragment shown during this section
- `ref` — verse reference

Default total is 45 minutes (2,820 seconds). Edit `dur` values to retime.

---

## Deploying

The site is hosted on **Vercel**, pointed at **bigmusiq.com**.

**Auto-deploy:** Every commit to `main` triggers a Vercel build. Push to GitHub, the site updates.

**Manual edit via GitHub web UI:**
1. Open the file in GitHub
2. Click the pencil icon (Edit this file)
3. Make your changes
4. Scroll down, write a commit message, click "Commit changes"
5. Vercel deploys in ~30 seconds

---

## Domain & DNS

| Setting | Value |
|---|---|
| Domain registrar | Squarespace Domains |
| DNS records (set on Squarespace) | A `@ → 76.76.21.21`, CNAME `www → cname.vercel-dns.com` |
| Hosting | Vercel |
| SSL | Auto-provisioned by Vercel |

---

## Hashtag

**#hellagoodmusiq** — the Q replaces the C. Visually distinct, aurally identical.

---

*A Brownefield Holdings project.*
