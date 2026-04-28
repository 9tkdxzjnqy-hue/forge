# Handoff — wc-sim-market
Date: 2026-04-27 (session 2)

## Where things stand

**The full build sprint is complete. Product is live at wc-sim.fly.dev.**

All FLY-46 through FLY-50 delivered, deployed, and marked Done in Linear.
Remaining backlog: FLY-51 (PostHog analytics), FLY-52 (auth unit tests).

## Next action

Pick up **FLY-51 (PostHog analytics)** — instrumentation is independent of everything
completed; can start immediately. The memory file `project_wcsim_posthog_mcp.md` has
the context: set up PostHog MCP before first sprint review (~June 11 2026).

## What was completed this session

### Issues closed

| Issue | Title | Notes |
|-------|-------|-------|
| FLY-46 | Live Elo pipeline | Added `elo_last_updated` (ratings.json mtime) to `/api/status` |
| FLY-47 | Auth UI | `soft-auth.jsx`: signup, login, auth widget, purchase success screen, AuthShell |
| FLY-48 | Scorers tab | `soft-scorers.jsx`: fetches `/api/goalscorers`, entitlement gating, `??` concealment, upsell |
| FLY-54 | Hide early-bird bundle after cutoff | `EARLYBIRD_CUTOFF_DATE` env var → `earlybird_available` bool in `/api/status` → `window.WC_CONFIG` |
| FLY-49 | Elo override UI | `EloOverridePanel` inline on Teams screen; GET/POST `/api/elo/overrides`; sticky "Run with my ratings" CTA; desktop-only |
| FLY-50 | Mobile layout | 5-tab bottom nav, More drawer, `useIsMobile` hook, per-screen responsive grids, compact fixture cards |

### Deployment

Pushed 18 commits to `github.com/flylower10/monte` and deployed to Fly.io.
Build cached — deploy took ~90 seconds.

### Key technical patterns established

- **Concealment model**: server returns `"??"` string for unentitled fields; frontend renders as muted monospace
- **Auth flow**: Flask routes (`/api/auth/register`, `/api/auth/login`, `/api/auth/me`) backed by Supabase; JWT in localStorage
- **Entitlement flags**: `has_groups_access`, `has_knockout_access`, `has_goalscorer_access`, `is_admin` — all from `user_profiles` table; admin bypass returns all-true
- **Mobile breakpoint**: `useIsMobile()` hook at 768px, exported globally; bottom nav via CSS `display:none` / `display:flex`
- **Elo overrides**: stored as JSON dict `{teamCode: delta}` on `user_profiles.elo_overrides`; POST replaces entire field

## Open items / backlog

- **FLY-51** — PostHog instrumentation (before June 11 sprint review)
- **FLY-52** — Auth unit tests: `get_entitlements()` test isolation (Supabase not installed locally)
- **`EARLYBIRD_CUTOFF_DATE` secret** — set `fly secrets set EARLYBIRD_CUTOFF_DATE=2026-06-11` before launch
- **Squad/player data** — `player_data.py` raises `NotImplementedError`; Scorers tab shows empty state until ingested
- **FLY-21–35** — Synthesis issues not yet in Linear; recreate before first sprint review

## Key references

- `world-cup-sim/docs/DESIGN.md` — design system
- `world-cup-sim/docs/CLAUDE.md` — build context
- Claude Design URL: `https://api.anthropic.com/v1/design/h/8_15zT3M8XK4OwX1WQy-Eg?open_file=World+Cup+Simulator.html`
