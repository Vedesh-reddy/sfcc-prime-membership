# Development phases

[← README](../README.md)

The implementation is organized into five reviewable delivery phases. They describe the repository's packaging and review structure; they do not claim to reproduce the original order of development.

Each phase has a feature branch and a PR targeting `main`. Phases are merged in order, keeping their branches and merge commits for reference.

| Phase | Feature branch | Scope | Pull request |
| --- | --- | --- | --- |
| 01 · Foundation | `feature/phase-01-foundation` | Cartridge identity, hooks and job step types, forms, Business Manager menu, custom objects, preferences, plans and jobs | [PR #1](https://github.com/Vedesh-reddy/sfcc-prime-membership/pull/1) |
| 02 · Engine and jobs | `feature/phase-02-engine-jobs` | Plans, membership lifecycle, proration, payment, benefit engine, access rules, rewards, reports, adapters, hooks, job steps and their tests | [PR #2](https://github.com/Vedesh-reddy/sfcc-prime-membership/pull/2) |
| 03 · Storefront and desk | `feature/phase-03-storefront-desk` | Controllers, templates, client script and styles, Custom APIs, Business Manager desk, remaining tests | [PR #3](https://github.com/Vedesh-reddy/sfcc-prime-membership/pull/3) |
| 04 · Tooling and quality | `feature/phase-04-tooling-quality` | npm dependencies, build, lint checks, metadata ZIP, GitHub Actions, PR template | [PR #4](https://github.com/Vedesh-reddy/sfcc-prime-membership/pull/4) |
| 05 · Documentation | `feature/phase-05-documentation` | Feature guide with highlighted sandbox screenshots, guides, contributing guide, attribution | [PR #5](https://github.com/Vedesh-reddy/sfcc-prime-membership/pull/5) |

The same cartridges are integrated in [SFCC-RefArch](https://github.com/Vedesh-reddy/SFCC-RefArch) through PRs #65–#68.

The final `main` branch contains all five phases. Build output is generated locally or downloaded from a successful GitHub Actions run; it is not committed.
