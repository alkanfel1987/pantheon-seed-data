# Pantheon Seed — user data

**Русский:** [README.md](README.md)

Users of the [mini-core](https://github.com/alkanfel1987/pantheon-seed) send reports on how it works and skills for the shared core here. Anyone can submit, and only we make entries in `data/`, after review.

Why: the core learns from the experience of everyone who trains the mini-core on their own machine. Reports show which skills really work and where they break. Submitted skills, after review, go out to all users in the next release. The full idea is in the [mini-core README](https://github.com/alkanfel1987/pantheon-seed/blob/main/README.en.md#sound-familiar).

## How to submit

**Issues → New issue**, one of two forms:

- **Work report** — the output of `python scripts/routine.py report` from your mini-core. It contains only summary numbers: which skills are called, what failed the integrity check, how the learning cycle is going.
- **Skill for the core** — a link to the skill in your fork and three answers: what it covers, how you know it works, and at what outcome it should be withdrawn.

⚠ **What you submit is visible to everyone at once, before our review.** Do not paste the texts of your session traces, or the paths, names and data of your projects.

We review submissions once a week and **reply within 14 days**. GitHub itself will notify you about labels and comments.

A bug in the mini-core, a question or a vulnerability — not here: see the "Where to write" section in the [mini-core README](https://github.com/alkanfel1987/pantheon-seed/blob/main/README.en.md#where-to-write).

## How to delete your submission

Write "delete" in your issue. We will delete the issue and the entry in `data/`. The previous version of the file stays in the git history — if you need that purged too, say so separately, and we will rewrite the history.

## What happens to a submission

| Label | Meaning |
|---|---|
| `в карантине` | accepted for review |
| `принято` | the entry has been added to `data/`; a skill goes into the core and the next mini-core release |
| `отклонено` | with the reason in a comment |

Skills are never merged automatically: a vulnerability test (text / code / hooks — hooks are not accepted), the 7+1 quarantine filter, a blind check, a human decision.

## What is in `data/`

- `data/reports/<date>-<issue number>.md` — an accepted report: the header has the mini-core version, OS, date of acceptance and a link to the issue; below are the numbers from the report as they are. No login and no comment from the author.
- `data/skills/<date>-<issue number>-<skill name>.md` — the decision on a skill: a link to the submission, which tests were passed (admission zone, 7+1 quarantine, blind check), the outcome and the reason, and the mini-core release in which it appeared.

Only we edit `data/`, and the history of each edit is visible in git.

## Licenses

The numbers from reports are published under [CC0](https://creativecommons.org/publicdomain/zero/1.0/) (consent is a checkbox in the form). Accepted skills are under MIT, like the mini-core itself.
