## Age Gate Bypass for Epic Games Store and Steam

Skips the repetitive age‑verification and mature‑content gates on the
Epic Games Store and Steam by setting the relevant cookies automatically.
No clicking, no date‑of‑birth forms — the pages just load.

### Supported pages

- **Steam Store** — date‑of‑birth age checks and mature‑content warnings
  (`store.steampowered.com/.../agecheck`)
- **Steam Community** — app‑hub content gates (`steamcommunity.com`)
- **Epic Games Store** — product‑page age gate (`store.epicgames.com/.../p/...`)

### How it works

The script runs at document start and sets the cookies each platform uses
to remember that the gate was already passed:

- **Steam Store:** `birthtime` (to clear the date‑of‑birth gate) and
  `wants_mature_content` (to clear the content warning).
- **Steam Community:** `wants_mature_content_apps` — the per‑app list Steam
  now uses for community hub gates.
- **Epic Games Store:** `egs_age_gate_dob`.

If a gate is still rendered when the page loads, it reloads once so the new
cookie takes effect. That's the only thing it does — no tracking, no network
calls, no data collection.

### Installation

1. Install a userscript manager such as **Tampermonkey** or **Violentmonkey**.
2. Click **Install** on this page.

### Notes

- Convenience only — it removes repeated prompts, it does not unlock anything
  you couldn't already reach by entering an adult date of birth yourself.
- Please follow each platform's Terms of Service and your local laws.

### Source

Code, issues and updates: <https://github.com/sermelipharo/GameStoreAgeBypass>
