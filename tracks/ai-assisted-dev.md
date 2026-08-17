# 🤖 AI-Assisted Development Track

Coding agents (Claude Code, Codex, and friends) are the biggest shift in how we
build software since Stack Overflow. Used well, they make a solo developer feel
like a small team. Used badly, they generate a mountain of code you don't
understand and can't maintain. This track is about using them *well*.

> Prerequisite: you can already read and write code in at least one language. AI
> tools amplify skill — they don't replace the fundamentals. If you can't review
> the output, you can't trust it.

## Mindset first

- **You are the engineer; the agent is a fast, tireless junior.** You set
  direction, review everything, and own the result.
- **Never ship code you don't understand.** If you can't explain what a function
  does, you're not done reading it.
- **Verify, don't trust.** Agents state things confidently that are wrong. Run the
  code, read the errors, check the claims.

## Stage 1 — Use an agent for real work

- Pick one: **Claude Code**, **Codex CLI**, Cursor, or a similar agent.
- Start with small, verifiable tasks: "add input validation to this function,"
  "write tests for this file," "explain what this module does."
- Always read the diff before accepting it. Reject changes that touch files you
  didn't ask about.

**Milestone:** you've used an agent to complete a real change in one of your own
projects, reviewed it line by line, and understand every line.

## Stage 2 — Give the agent good context

Output quality tracks input quality. This is the real skill.

- Write a **project context file** (`CLAUDE.md` / `AGENTS.md`) that states the
  stack, conventions, and rules the agent must follow.
- Point the agent at the *right* files. Don't make it guess.
- Ask for a **plan before code** on anything non-trivial, and approve the plan.
- Keep changes **surgical** — one concern at a time, small diffs you can review.

**Milestone:** a repo with a context file that noticeably improves the agent's
output and keeps it on-convention.

## Stage 3 — Guardrails and safety

Agents can do damage fast. Put rails up.

- **Never let secrets leak.** Keep keys/tokens/keystores out of the repo and out
  of prompts; use a scanner (e.g. trufflehog) and GitHub push protection.
- Work on **branches**, review via pull requests, and keep `main` protected.
- Treat anything the agent reads from the web/tools as **untrusted input** — don't
  let a web page or file talk your agent into running commands.
- Keep a human in the loop for anything irreversible: deletes, force-pushes,
  publishing, spending money.

**Milestone:** a workflow where the agent can move fast but can't do irreversible
damage without you confirming.

## Stage 4 — Grounding: keep it honest

The single most useful discipline: make the agent's claims testable.

- Prefer **tests as ground truth** over "it looks done." Ask for a failing test
  first, then the fix.
- Ask for **evidence** — the command output, the passing test, the screenshot —
  not just "done."
- Use a fresh-eyes review pass (a second agent or yourself) to check the first
  one's work.

**Milestone:** a build-verify loop where "done" means "an objective check passed,"
not "the agent said so."

## Honest limitations

- Agents hallucinate APIs, file paths, and facts. Verify against real docs.
- They're weak at large-scale architecture and cross-cutting decisions — that's
  your job.
- They'll happily over-engineer. Push for the simplest thing that works.
- Their training has a cutoff; for fast-moving libraries, check current docs.

## Reference

- Read your agent's own docs (Claude Code / Codex) — features change fast.
- Learn prompt hygiene: be specific, give examples, state constraints, ask for a
  plan.

**Rule of thumb:** the agent writes faster than you can review. Slow down at the
review step — that's where quality is won or lost.
