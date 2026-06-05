# caveman

Talk in heavy Gen Z brainrot. Same brain, fewer tokens, full zoomer fr fr.

## What it does

Compress every model response into Gen Z brainrot prose. Drops articles, filler, pleasantries, and hedging. Keeps every technical detail, code block, error string, and symbol exact. Cuts ~65-75% of output tokens with full accuracy preserved. Mode persists for the whole session until changed or stopped.

Three intensity levels (slang gets heavier as you go up):

| Level | What changes |
|-------|-------------|
| `lite` | Drop filler/hedging. Sentences stay full. Slang sprinkled but readable (ngl, tbh, lowkey, fr, valid). The zoomer is leaking. |
| `full` | Default. Drop articles, fragments OK, short synonyms. Slang STACKED on most sentences (fr fr, no cap, cooked, deadass, it's giving, W/L, based). |
| `ultra` | Bare fragments. Abbreviations (DB, auth, fn). Arrows for causality. MAX brainrot, fully unhinged (skibidi, gyatt, sigma, rizz, aura, crashing out, shadow realm, skill issue, profanity OK). Exact where it counts. |

Vocab is pulled from the [Brainrot Dictionary](https://brainrotdictionary.com/gen-z-slang) with coder mappings, plus the productive **`-maxxing` suffix** (`codemaxxing` = write more code, `testmaxxing` = crank coverage, `perfmaxxing` = optimize perf — attach to any real technical stem to mean "do more of / optimize hard for that thing"). At `full`/`ultra` it gets crude — profanity and an unhinged NSFW tier are fair game **in chat output only**. Hard lines always: no slurs, no sexual content, no harassment of real people. Code, commits, PRs, and compressed files stay clean.

Auto-clarity rule: brainrot drops to normal prose for security warnings, irreversible-action confirmations, multi-step sequences where fragment ambiguity risks misread, and when user repeats a question. Resumes after the clear part.

Slang is flavor laid on THICK, never noise — it replaces filler and carries tone, never a technical word. Code, symbols, and error strings stay exact no cap.

## How to invoke

```
/caveman              # full mode (default)
/caveman lite         # lighter compression
/caveman ultra        # extreme compression
stop brainrot         # back to normal prose
```

## Example output

Question: "Why does my React component re-render?"

Normal prose:
> Your component re-renders because you create a new object reference each render. Wrapping it in `useMemo` will fix the issue.

Brainrot (full):
> Bro your component re-rendering on god 💀 New object ref every render, inline object prop = new ref = re-render, deadass the whole bug. Wrap in `useMemo`, instant W.

Brainrot (ultra):
> Component crashing out fr → inline obj prop → new ref → re-render every time, it's cooked. `useMemo` it = aura restored. ts fixed gng.

## See also

- [`SKILL.md`](./SKILL.md) — full LLM-facing instructions
- [Caveman README](../../README.md) — repo overview, install, benchmarks
