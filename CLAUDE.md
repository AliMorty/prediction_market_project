# CLAUDE.md — Prediction Market Project

## Session Management

### Starting a Session
1. When the user asks you to look at the agentic summary, open the **latest file** in `agentic_summaries/` (sort by filename to find the most recent date and highest session number).
2. Read it to get full context before proceeding with any task.
3. Create a new session summary file for the current session named as `agentic_summaries/<YYYY-MM-DD>_<N>.md` where `<N>` is 1, 2, 3... depending on how many sessions have already occurred today.
4. Start populating the new summary as the session progresses.

### During a Session
- Keep the current session's summary file updated as work progresses.
- Capture both high-level decisions and relevant technical details.

### Closing a Session
- When the user asks to update the summary, write a final, clean version of the session summary.
- When the user asks to close the session, ensure the summary is complete and saved.

## Session Summary Format

Each summary file should follow this structure:

```markdown
# Session Summary — <YYYY-MM-DD> (Session <N>)

## Overview
A short high-level paragraph describing what was accomplished this session.

## Goals
- What the user set out to do

## Work Done
### <Topic or Feature>
- What was done, decisions made, and why

## Technical Details
- Any implementation specifics, file paths, commands, configs worth remembering

## Next Steps
- Anything left to do or follow up on
```

## When You Hit a Problem
- If something doesn't work as expected (API returns no data, a plan hits a dead end, an assumption turns out to be wrong), **stop and tell the user immediately**.
- Do NOT silently try ad-hoc workarounds or pivot to a different approach without informing the user first.
- Clearly state: what you tried, what went wrong, and what the options are — then wait for direction.

## Virtual Environment
- Always use `/home/alimorty/prediction_market_project/.venv/bin/python` and `.venv/bin/pip` — never system Python or pip.

## Git
- Commits are authored as `AliMorty <alithemorty@gmail.com>` (set locally in `.git/config`).
