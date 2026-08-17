# 📱 Android / Kotlin Track

How I'd learn Android today to actually ship apps to the Play Store — not just
pass a course. Kotlin + Jetpack Compose, modern and opinionated.

> Prerequisite: you can already write basic programs and use Git (Phase 1 of the
> [main roadmap](../README.md)).

## Stage 1 — Kotlin the language

Don't learn "Android" before you can read Kotlin comfortably.

- Core: `val`/`var`, null safety (`?`, `?:`, `!!`), data classes, `when`,
  collections (`map`/`filter`/`fold`), extension functions, sealed classes.
- Then: coroutines and `Flow` — you'll use these constantly for anything async.
- Free: [Kotlin docs & Koans](https://kotlinlang.org/docs/koans.html),
  [Google's Kotlin Bootcamp](https://developer.android.com/courses/kotlin-bootcamp/overview).

**Milestone:** solve a handful of small Kotlin exercises without looking up syntax.

## Stage 2 — Your first app (Compose)

- Install **Android Studio**. Learn the project structure, Gradle, and the
  emulator.
- Learn **Jetpack Compose** (the modern UI toolkit — skip XML layouts for new work):
  composables, state (`remember`, `mutableStateOf`), `LazyColumn`, navigation.
- Free: [Android Basics with Compose](https://developer.android.com/courses/android-basics-compose/course)
  (Google's official, project-based).

**Milestone:** a multi-screen app that holds and displays state (e.g. a to-do or
notes app) running on the emulator.

## Stage 3 — Real app architecture

This is what separates a toy from a maintainable app.

- **State management:** `ViewModel` + `StateFlow`, unidirectional data flow, a
  `UiState` sealed class for loading/success/error.
- **Local data:** [Room](https://developer.android.com/training/data-storage/room)
  for a SQLite database. Learn migrations early — they bite later.
- **Dependency injection:** Hilt (or manual DI for small apps — don't over-engineer).
- **Networking:** Retrofit/Ktor + kotlinx.serialization when you need an API.
- **Architecture:** a light Clean Architecture (UI → domain → data). Don't
  cargo-cult it on a tiny app.

**Milestone:** an offline-first app with a local database, a ViewModel per screen,
and proper loading/error states.

## Stage 4 — Ship to the Play Store

The part tutorials skip and where real learning happens.

- **Signing:** generate a keystore, configure signing from `local.properties` /
  `keystore.properties` — **never** hardcode credentials or commit the keystore.
- **Release build:** `minifyEnabled`, an app icon, adaptive icons, versioning.
- **Play Console:** create the app, write a store listing, prepare screenshots,
  fill the **Data Safety** form, add a **privacy policy** (required).
- **Release track:** internal testing → closed → production. Ship small updates.

**Milestone:** an app live on Google Play (internal testing counts as your first win).

## Stage 5 — Level up

- Compose performance: recomposition, stability, `derivedStateOf`, avoiding jank.
- Edge-to-edge and modern Android version targets.
- Testing: unit tests for ViewModels, Room migration tests, basic UI tests.
- Crash reporting and a feedback loop from real users.

## Reference

- [Official Android developer docs](https://developer.android.com/) — the source of truth.
- [Now in Android](https://github.com/android/nowinandroid) — Google's modern
  sample app; read its code.
- [Kotlin coroutines guide](https://kotlinlang.org/docs/coroutines-guide.html).

**Rule of thumb:** don't add an abstraction until a second screen needs it. Ship
the first version simple, then refactor with real requirements in hand.
