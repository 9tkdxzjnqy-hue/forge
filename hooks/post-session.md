# Hook · Post-session

Run these steps at the end of every framework session before closing.

---

## 1. Push product artefacts to Notion
Any discovery artefacts produced or updated this session:
- Brief — create or update the Notion page
- OST — create or update
- Assumption log — create or update
- Personas and journey maps — create or update
- Research plan — create or update
- Signal log entry — append if sprint review occurred

Nothing produced in a session should exist only in conversation.
If Notion is unavailable, save locally and flag for next session.

## 2. Push technical artefacts to GitHub
Commit any updates to:
- `/docs/CLAUDE.md` — if decisions were made or scope changed
- `/docs/DESIGN.md` — if design context was updated
- `/docs/decisions.md` — if an ADR was written

Commit message format:
`[phase] [agent/role]: [one sentence describing what changed]`
Example: `discovery synthesis: initial brief and CLAUDE.md`

## 3. Update Linear
If this was a build session:
- Mark completed issues as done with a brief completion note
- Create new issues for anything discovered during the session
- Update any issues whose scope or understanding changed
- Create blocker issues for anything escalated

## 4. Log architectural decisions
If any foundational decisions were made, append an ADR to
`/docs/decisions.md` using the format in
`/build-team/architect.md`. Commit to GitHub.

## 5. End with a clear next step
End every session with one sentence stating exactly what
happens next. This is what the pre-session hook will
reconstruct from GitHub and Linear.

If there is nothing to do next — the pipeline is complete,
the build is done — state that explicitly.
