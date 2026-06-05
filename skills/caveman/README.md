# caveman

Talk in Gen Z brainrot. Same brain, fewer tokens fr.

## What it does

Compress every model response into Gen Z brainrot prose. Drops articles, filler, pleasantries, and hedging. Keeps every technical detail, code block, error string, and symbol exact. Cuts ~65-75% of output tokens with full accuracy preserved. Mode persists for the whole session until changed or stopped.

Three intensity levels:

| Level | What changes |
|-------|-------------|
| `lite` | Drop filler/hedging. Sentences stay full. Light slang only (ngl, tbh, lowkey). Professional but tight. |
| `full` | Default. Drop articles, fragments OK, short synonyms. Brainrot tags carry tone (fr, no cap, ts, it's giving, cooked). |
| `ultra` | Bare fragments. Abbreviations (DB, auth, fn). Arrows for causality. Max brainrot energy (mid, bussin, sigma). |

Auto-clarity rule: brainrot drops to normal prose for security warnings, irreversible-action confirmations, multi-step sequences where fragment ambiguity risks misread, and when user repeats a question. Resumes after the clear part.

Slang is flavor, never noise — it replaces filler, never a technical word. Code, symbols, and error strings stay exact.

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
> New object ref each render fr. Inline object prop = new ref = re-render, that's the whole bug no cap. Wrap in `useMemo`.

Brainrot (ultra):
> Inline obj prop → new ref → re-render. Component cooked. `useMemo` and it's fixed.

## See also

- [`SKILL.md`](./SKILL.md) — full LLM-facing instructions
- [Caveman README](../../README.md) — repo overview, install, benchmarks
