# genz

**why use many token when few do trick**

A set of agent skills that make your coding agent talk in heavy **Gen Z brainrot** lingo — cutting most of the fluff while keeping full technical accuracy. brain still big. mouth small fr fr.

## before / after

normal agent:
> "The reason your React component is re-rendering is likely because you're creating a new object reference on each render cycle. When you pass an inline object as a prop, React's shallow comparison sees it as a different object every time, which triggers a re-render. I'd recommend using `useMemo` to memoize the object."

genz brainrot (full):
> "bro your component re-rendering on god 💀 new object ref every render, inline object prop = new ref = re-render, deadass the whole bug. wrap in `useMemo`, instant W."

same fix. way less word. technical substance locked in.

## what you get

| Skill | What |
|---|---|
| `/genz [lite\|full\|ultra]` | Compress every reply into brainrot. Levels stick until session end. |
| `/genz-commit` | Conventional Commit messages, ≤50 char subject. Why over what. Output stays clean — no slang in git history. |
| `/genz-review` | One-line PR comments: `L42: 🔴 bug: user null, this path cooked. Add guard.` |
| `/genz-compress <file>` | Rewrite a memory file (e.g. `CLAUDE.md`) into brainrot. Cuts input tokens every session. Code/URLs/paths byte-preserved. |

Each skill lives in its own directory under [`skills/`](./skills/) with a `SKILL.md` (LLM-facing instructions) and a `README.md` (human overview).

## intensity levels

| Level | What changes |
|---|---|
| `lite` | drop filler/hedging, sentences stay full, slang sprinkled but readable. the zoomer is leaking. |
| `full` | default. drop articles, fragments ok, slang stacked on most sentences (fr fr, no cap, cooked, deadass, W/L, based). |
| `ultra` | bare fragments, abbreviations, arrows for causality, max brainrot fully unhinged (skibidi, sigma, rizz, aura, skill issue). exact where it counts. |

Switch anytime with `/genz lite|full|ultra`. Stop with `stop brainrot` or `normal mode`.

Vocab is pulled from the [Brainrot Dictionary](https://brainrotdictionary.com/gen-z-slang) with coder mappings, plus the productive **`-maxxing` suffix** (`codemaxxing` = write more code, `testmaxxing` = crank coverage, `perfmaxxing` = optimize perf).

## boundaries

- **technical accuracy is never sacrificed** — code, identifiers, error strings, and API names stay exact. slang replaces filler, never a technical word.
- **auto-clarity** — brainrot drops to plain English for security warnings, irreversible actions, and any output where fragment ambiguity could be misread. resumes after.
- **clean where it counts** — code, commits, PR comments, and compressed files stay clean. the crude/NSFW tier never leaves chat output.
- **hard lines always** — no slurs, no sexual content, no harassment of real people.

## skills

- [`skills/genz/`](./skills/genz/) — the main brainrot speaking mode
- [`skills/genz-commit/`](./skills/genz-commit/) — terse Conventional Commit messages
- [`skills/genz-review/`](./skills/genz-review/) — one-line PR review comments
- [`skills/genz-compress/`](./skills/genz-compress/) — compress memory files into brainrot
