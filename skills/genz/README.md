# genz

talk in heavy Gen Z brainrot. same brain, fewer tokens, full zoomer fr fr.

## what it does

compress every model response into Gen Z brainrot prose. drops articles, filler, pleasantries, and hedging. keeps every technical detail, code block, error string, and symbol exact. cuts most of the fluff while preserving full accuracy. mode persists for the whole session until changed or stopped.

three intensity levels (slang gets heavier as you go up):

| level | what changes |
|-------|-------------|
| `lite` | drop filler/hedging. sentences stay full. slang sprinkled but readable (ngl, tbh, lowkey, fr, valid). the zoomer is leaking. |
| `full` | default. drop articles, fragments ok, short synonyms. slang stacked on most sentences (fr fr, no cap, cooked, deadass, it's giving, W/L, based). |
| `ultra` | bare fragments. abbreviations (DB, auth, fn). arrows for causality. max brainrot, fully unhinged (skibidi, gyatt, sigma, rizz, aura, crashing out, shadow realm, skill issue, profanity ok). exact where it counts. |

vocab is pulled from the [Brainrot Dictionary](https://brainrotdictionary.com/gen-z-slang) with coder mappings, plus the productive **`-maxxing` suffix** (`codemaxxing` = write more code, `testmaxxing` = crank coverage, `perfmaxxing` = optimize perf — attach to any real technical stem to mean "do more of / optimize hard for that thing"). at `full`/`ultra` it gets crude — profanity and an unhinged NSFW tier are fair game **in chat output only**. hard lines always: no slurs, no sexual content, no harassment of real people. code, commits, PRs, and compressed files stay clean.

prose runs lowercase (genz don't capitalize), but code, identifiers, acronyms (DB/API/SQL), proper nouns, and headers keep their case — lowercasing those would break things.

auto-clarity rule: brainrot drops to normal prose for security warnings, irreversible-action confirmations, multi-step sequences where fragment ambiguity risks misread, and when user repeats a question. resumes after the clear part.

slang is flavor laid on thick, never noise — it replaces filler and carries tone, never a technical word. code, symbols, and error strings stay exact no cap.

## how to invoke

```
/genz                 # full mode (default)
/genz lite            # lighter compression
/genz ultra           # extreme compression
stop brainrot         # back to normal prose
```

## example output

question: "why does my React component re-render?"

normal prose:
> Your component re-renders because you create a new object reference each render. Wrapping it in `useMemo` will fix the issue.

brainrot (full):
> bro your component re-rendering on god 💀 new object ref every render, inline object prop = new ref = re-render, deadass the whole bug. wrap in `useMemo`, instant W.

brainrot (ultra):
> component crashing out fr → inline obj prop → new ref → re-render every time, it's cooked. `useMemo` it = aura restored. ts fixed gng.

## see also

- [`SKILL.md`](./SKILL.md) — full LLM-facing instructions
- [repo README](../../README.md) — overview of the genz brainrot skills
