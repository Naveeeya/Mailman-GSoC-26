# Site manifest

Repo: `Mailman-GSoC-26` → https://naveeeya.github.io/Mailman-GSoC-26/

## Design tokens

Everything is driven by CSS custom properties at the top of `<style>`.
Change these and the whole page follows.

| Token | Value | Role |
|---|---|---|
| `--paper` | `#FCFCFA` | Warm near-white. Chosen so white-background logos blend in |
| `--card` | `#F4F4EF` | Code blocks, inline code |
| `--ink` | `#1A1D23` | Body text |
| `--muted` | `#646B75` | Captions, labels, secondary text |
| `--rule` | `#E4E4DD` | Light dividers |
| `--rule-strong` | `#CFCFC6` | Section rules, table headers |
| `--accent` | `#0E5257` | Deep teal. Links, section labels, done tags |
| `--flag` | `#8A5A00` | Amber. Outstanding-work tags only |
| `--s1`–`--s7` | 8 / 16 / 24 / 32 / 48 / 64 / 88 px | Spacing scale. All margins use these |

## Type

| Family | Used for | Why |
|---|---|---|
| Source Serif 4 | `h1`, `h3`, the standfirst | Adobe's reading serif. Gravitas without fuss |
| Source Sans 3 | Body, lists, tables | Same superfamily, so it harmonises by construction |
| JetBrains Mono | Code, section labels, facts, captions in the run | The 2026 developer default. Slashed zero, distinct `1 l I` |

Measure is capped at 720px, which lands around 68 characters per line.

## Files

| Path | Purpose |
|---|---|
| `index.html` | The whole page. No JavaScript, no build step |
| `site.webmanifest` | Name, description, theme colour, icons |
| `README.md` | Repo landing page |
| `images/gsoc-logo.png` | Google Summer of Code mark |
| `images/mailman-logo.jpg` | GNU Mailman mark |
| `images/01-environment.png` | `mailman info` |
| `images/02-seeded.png` | Member, owner and moderator counts |
| `images/03-state-before.png` | List state **before** the backup |
| `images/04-backup.png` | `mailman backup` + `ls -lh` |
| `images/05-anatomy.png` | Section-by-section summary of the file |
| `images/06-json.png` | Pretty-printed JSON head |
| `images/07-security.png` | Moderator password absent |
| `images/08-delete.png` | List removed |
| `images/09-restore.png` | `mailman restore` + rosters |
| `images/10-state-after.png` | List state **after** the restore |
| `images/11-fidelity.png` | `IDENTICAL` diff |
| `images/12-cross-domain.png` | `--listname` |
| `images/13-safety.png` | Three failure modes, exit 2 |
| `images/14-overwrite.png` | Confirmation prompt declined |
| `images/15-member-detail.png` | Per-member preferences and ban ordering |
| `images/16-schema.gif` | Backup format walkthrough |
| `images/icon-192.png` | Manifest icon, optional |
| `images/icon-512.png` | Manifest icon, optional |

Step 10 reuses `03-state-before.png` deliberately, for the side-by-side.

## Logos

Both marks sit on white backgrounds. `mix-blend-mode: multiply` plus the warm
near-white paper makes those backgrounds disappear. If you ever darken `--paper`
past about `#F5F5F0`, the white boxes come back and the logos will need
transparent PNGs instead.

Both are trademarks, used here to identify the program and the organisation.

## External dependencies

Google Fonts only. If it disappears the page falls back to Georgia, the system
sans and the system monospace, and stays readable. Nothing else is loaded from
off-site and there is no JavaScript.
