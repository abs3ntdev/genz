# caveman-review

One-line PR comments, brainrot vibe optional. Location, problem, fix. No throat-clearing, no yap.

## What it does

Generates code review comments in `L<line>: <severity> <problem>. <fix>.` format. One line per finding. Severity emoji: 🔴 bug, 🟡 risk, 🔵 nit, ❓ question. Drops "I noticed that...", hedging, and restating what the diff already shows. Keeps exact line numbers, backticked symbols, and concrete fixes.

Slang is allowed as light tone flavor (this is `cooked`, that's `bussin`), but location, problem, and fix stay 100% exact and readable.

Auto-clarity: drops terse mode for CVE-class security findings, architectural disagreements, and onboarding contexts where the author needs the *why*. Resumes terse for the rest.

Output only — does not approve, request changes, or run linters.

## How to invoke

```
/caveman-review
```

Also triggers on "review this PR", "code review", "review the diff".

## Example output

```
L42: 🔴 bug: user can be null after .find() — this path is cooked. Add guard before .email.
L88-140: 🔵 nit: 50-line fn doing 4 things, lowkey too much. Extract validate/normalize/persist.
L23: 🟡 risk: no retry on 429 ngl. Wrap in withBackoff(3).
L107: ❓ q: why drop the cache here? Reads on next request will miss fr.
```

## See also

- [`SKILL.md`](./SKILL.md) — full LLM-facing instructions
- [Caveman README](../../README.md) — repo overview
