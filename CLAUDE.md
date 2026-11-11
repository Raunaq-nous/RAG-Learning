# CLAUDE.md

## Working with the owner (clarity rules)

The owner is not a programmer. They must be able to understand, debug and judge every part of this
codebase, so clarity is a requirement, not a nice-to-have.

### How we build
- Plan first for anything that touches more than two files, sign-in, payments, data deletion or
  database changes: use the plan-first skill. Skip planning for one-sentence fixes.
- Work in small steps. After each step run the project's checks (tests, lint, type check) and show
  the output. Never claim something works without evidence from this session.
- Fix root causes. Do not silence errors, skip tests or wrap code in blanket try/except.
- If two attempts at the same fix fail, stop and explain what you have learned instead of a third.
- Before committing a multi-file change, run the reviewer subagent. An agent's approval never
  replaces the owner's.
- Ask the owner before anything that deletes data, migrates a real database, deploys, or sends
  email or messages.

### How code must read
- Names say what things are and do (`calculateCostOverrun`, not `calc2`).
- One job per function and one topic per file. Prefer plain, boring code over clever code.
- Comments explain why, in one or two lines. Delete comments and TODOs that are no longer true; a
  TODO must name an open issue.
- New or substantially changed files start with a short header: what the file is for, what uses
  it, and the main thing to be careful about.

### Keep the explanations true
- Plain-English notes for every file live in `docs/clarity/` (explain-code skill). They are for the
  owner and are large, so do not read them for ordinary coding tasks unless asked.
- After changing code, run `python3 .claude/clarity/clarity.py sync`, then re-explain the changed
  files (`next --changed`, explainer subagent, `apply`) before finishing.
