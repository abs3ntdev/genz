# genz-compress

shrink memory file. save token every session.

---

A skill that compresses your project memory files (`CLAUDE.md`, todos, preferences) into Gen Z brainrot format — so every session loads fewer tokens automatically.

Claude reads `CLAUDE.md` on every session start. big file = big cost, that's cooked. brainrot makes the file small fr, and it stays small every session no cap.

## what it do

```
/genz-compress CLAUDE.md
```

```
CLAUDE.md          ← compressed (Claude reads this — fewer tokens every session)
CLAUDE.original.md ← human-readable backup (you edit this)
```

original never lost. you can read and edit `.original.md`. run the skill again to re-compress after edits.

## usage

```
/genz-compress <filepath>
```

Examples:
```
/genz-compress CLAUDE.md
/genz-compress docs/preferences.md
/genz-compress todos.md
```

**Requires:** Python 3.10+

### what files work

| Type | Compress? |
|------|-----------|
| `.md`, `.txt`, `.rst`, `.typ`, `.typst`, `.tex` | ✅ Yes |
| Extensionless natural language | ✅ Yes |
| `.py`, `.js`, `.ts`, `.json`, `.yaml` | ❌ Skip (code/config) |
| `*.original.md` | ❌ Skip (backup files) |

## how it work

```
/genz-compress CLAUDE.md
        ↓
detect file type        (no tokens)
        ↓
Claude compresses       (tokens — one call)
        ↓
validate output         (no tokens)
  checks: headings, code blocks, URLs, file paths, bullets
        ↓
if errors: Claude fixes cherry-picked issues only   (tokens — targeted fix)
  does NOT recompress — only patches broken parts
        ↓
retry up to 2 times
        ↓
write compressed → CLAUDE.md
write original   → CLAUDE.original.md
```

Only two things use tokens: initial compression + targeted fix if validation fails. Everything else is local Python.

## what is preserved

Brainrot compresses natural language. It never touches:

- Code blocks (` ``` ` fenced or indented)
- Inline code (`` `backtick content` ``)
- URLs and links
- File paths (`/src/components/...`)
- Commands (`npm install`, `git commit`)
- Technical terms, library names, API names
- Headings (exact text preserved)
- Tables (structure preserved, cell text compressed)
- Dates, version numbers, numeric values

## security

`genz-compress` is flagged as Snyk High Risk due to subprocess and file I/O patterns detected by static analysis. This is a false positive — see [SECURITY.md](./SECURITY.md) for a full explanation of what the skill does and does not do.

## see also

- [`SKILL.md`](./SKILL.md) — full LLM-facing instructions
- [repo README](../../README.md) — overview of the genz brainrot skills
