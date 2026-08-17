# DevRoadmap

A practical, opinionated roadmap for becoming a developer who **ships** — written
from the perspective of a solo indie developer who builds and publishes real apps
and tools. Less "watch 40 hours of tutorials," more "build the smallest real thing
and put it in front of users."

Maintained by [Sudarshan Chaudhari](https://github.com/SUDARSHANCHAUDHARI)
([SudarshanTechLabs](https://github.com/SUDARSHANCHAUDHARI)). All resources linked
here are free unless marked otherwise.

---

## Who this is for

- Beginners who want a clear path from zero to a first real project.
- Self-taught developers who can write code but feel scattered.
- Anyone who wants to build and ship their own apps/tools instead of only doing
  coursework.

If you want a job, this still applies — the fastest way to look employable is to
have shipped things.

## How to use this

1. Don't read it all. Pick the phase you're in and do the next concrete thing.
2. **Build in public.** Every phase ends in something you can show — a repo, a
   deployed page, an app on a store.
3. Timebox learning. If you've watched a concept twice, stop and build with it.
4. When you get stuck, that's the job. Learn to debug, search, and read docs —
   those are the real skills.

---

## The general roadmap

Four phases. Move on when you've *shipped* the milestone, not when you "feel ready."

### Phase 1 — Foundations (build the muscle)
**Goal:** write and run small programs without hand-holding.

- Pick **one** language and stick with it. Python or JavaScript are the friendliest
  first choices.
- Learn: variables, types, conditionals, loops, functions, arrays/lists, maps/dicts,
  basic error handling.
- Get comfortable with the terminal, Git, and GitHub early — commit daily.
- Free resources: [freeCodeCamp](https://www.freecodecamp.org/),
  [The Odin Project](https://www.theodinproject.com/) (web),
  [Python for Everybody](https://www.py4e.com/) (Python),
  [Harvard CS50](https://cs50.harvard.edu/x/) (foundations).

**Milestone:** a GitHub repo with 3–5 small programs (a calculator, a to-do list,
a number-guessing game). Commit history that shows daily-ish work.

### Phase 2 — Build (make real things)
**Goal:** build an application with a UI and/or data, end to end.

- Learn version control properly: branches, pull requests, resolving conflicts.
- Learn how to read documentation and error messages — this is a superpower.
- Pick a lane and build a real project in it (see the **tracks** below).
- Learn just enough of: HTTP, JSON, a database (start with SQLite), and how a
  client talks to a server.

**Milestone:** one project a stranger could actually use, deployed or installable,
with a README that explains what it is and how to run it.

### Phase 3 — Ship (put it in front of people)
**Goal:** take one project all the way to "released."

- Web: deploy it (Cloudflare Pages, Vercel, GitHub Pages). Buy a domain if it's
  worth it.
- Mobile: publish to Google Play / the App Store. Learn signing, store listings,
  and privacy policies.
- Add the unglamorous parts: error handling, a basic test or two, a LICENSE, a
  real README, and screenshots.

**Milestone:** a link you can send someone: a live URL or a store listing.

### Phase 4 — Grow (level up deliberately)
**Goal:** go from "it works" to "it's good."

- Learn testing, basic CI (GitHub Actions), and how to read a stack trace fast.
- Study data structures & algorithms *enough* to reason about performance and pass
  interviews — don't let it become your whole identity.
- Learn security basics: never commit secrets, validate input, understand auth.
- Contribute to an open-source project, or open-source your own work.

**Milestone:** a second shipped project that's noticeably better-engineered than
your first.

---

## Specialty tracks

Once you have the foundations, go deep in a lane. These are the ones I actually
work in:

| Track | For | File |
|---|---|---|
| 📱 **Android / Kotlin** | Native mobile apps, Jetpack Compose, Play Store | [tracks/android.md](tracks/android.md) |
| 🤖 **AI-assisted development** | Building with coding agents (Claude Code, Codex) the right way | [tracks/ai-assisted-dev.md](tracks/ai-assisted-dev.md) |
| 🧪 **QA & testing** | Testing mindset, automation, shipping with confidence | [tracks/qa-testing.md](tracks/qa-testing.md) |

---

## Principles I actually believe

- **Ship the smallest real thing.** A tiny finished app beats a huge unfinished one.
- **Boring and done > clever and stuck.** Reach for the simplest solution that works.
- **Read the error.** Most answers are in the message you skimmed past.
- **Version control everything, from day one.** Commit small, commit often.
- **Never commit secrets.** Keys, tokens, keystores, `.env` — keep them out of Git.
- **Learn in public.** Your GitHub is your résumé; let it show you doing the work.

---

## Contributing

Suggestions and corrections are welcome — open an issue or a pull request. Keep
recommendations free-first and beginner-friendly.

## License

[MIT](LICENSE) © 2026 Sudarshan Chaudhari. Original work; use it freely.
