# 🧪 QA & Testing Track

Testing isn't a phase at the end — it's how you ship without fear. This track is
for developers who want to build a real testing mindset, whether you're QA by role
or a solo dev who *is* the QA team.

> Prerequisite: you can build a small app or service (Phase 2 of the
> [main roadmap](../README.md)).

## Mindset first

- **Quality is everyone's job**, especially when you're solo. If you built it, you
  test it.
- Think in terms of **what could go wrong**, not just "does the happy path work."
  Empty inputs, huge inputs, no network, slow network, wrong permissions.
- A bug caught before release costs minutes; the same bug in production costs
  hours and trust.

## Stage 1 — Manual testing, done properly

- Learn to write a clear **bug report**: steps to reproduce, expected vs actual,
  environment, severity. A vague bug report is a wasted one.
- Learn **test cases** and **edge cases**: boundaries, empty/null, duplicates,
  invalid input, interruption (kill the app mid-action).
- Explore deliberately: try to *break* your own app before a user does.

**Milestone:** a written test checklist for one of your projects, plus a
well-formed bug report you actually filed against yourself.

## Stage 2 — Automated tests

- **Unit tests:** test one function/class in isolation. Fast, many, cheap. Start
  here. (JUnit/Kotest for Kotlin, Vitest/Jest for JS, pytest for Python.)
- **Integration tests:** test that pieces work together (e.g. a database query, an
  API call).
- **End-to-end / UI tests:** test the app like a user would. Fewer of these — they're
  slower and more brittle. (Playwright for web, Espresso/Compose test for Android.)
- Learn the **testing pyramid**: lots of unit, some integration, few E2E.

**Milestone:** a project with a real test suite that runs with one command and
actually catches regressions.

## Stage 3 — Test automation & CI

- Run your tests automatically on every push with **GitHub Actions**.
- Fail the build when tests fail — a red build should block a merge.
- Learn to read a failing CI log fast and reproduce the failure locally.
- Add basic checks: linting, type-checking, formatting.

**Milestone:** a repo where every pull request runs tests + checks automatically,
and you trust a green build.

## Stage 4 — Ship with confidence

- **Regression testing:** keep a suite that proves old features still work after
  changes.
- **Release checklist:** version bumped, tests green, no secrets, changelog,
  screenshots, store/privacy requirements met.
- **Cross-platform / cross-device:** the thing that works on your machine breaks
  on someone else's. Test on real variety where it matters.
- **Post-release:** crash reporting + a feedback channel so real-world bugs come
  back to you.

**Milestone:** a repeatable release process you follow every time, so shipping is
boring (in the best way).

## Reference

- [Ministry of Testing](https://www.ministryoftesting.com/) — community + learning.
- [ISTQB Foundation syllabus](https://www.istqb.org/) — the vocabulary of QA
  (free syllabus PDF).
- Framework docs: Playwright, JUnit/Kotest, pytest, Espresso.

**Rule of thumb:** if a bug ever escapes to production, add a test that would have
caught it before you fix it. That's how a suite gets strong over time.
