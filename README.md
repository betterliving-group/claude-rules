# claude-rules

One place for Akash's Claude Code rules. Edit `rules.md` here; every session reads it at start.

How it is plugged in:

1. This PC: a SessionStart hook in `~/.claude/settings.json`.
2. Cloud sessions: the same hook in each repo's `.claude/settings.json` (labs, spaf).

The hook downloads `rules.md`, keeps a copy in `~/.claude/claude-rules.md`, and uses that copy when GitHub can't be reached.

Hook command:

```sh
f="$HOME/.claude/claude-rules.md"; mkdir -p "$HOME/.claude"; curl -fsSL --max-time 5 https://raw.githubusercontent.com/betterliving-group/claude-rules/main/rules.md -o "$f.tmp" && mv "$f.tmp" "$f"; cat "$f" 2>/dev/null || true
```

Claude chat (claude.ai) does not use this: keep its account settings in step by hand.
