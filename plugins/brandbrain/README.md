# Brand Brain for Claude Code

One command, `/brandbrain <words>`, for your brand on [Brand Brain](https://brain.fowl-ai.com). Attach a clip, type what you want, get the finished version back in your brand's Media. Nothing is posted without your yes.

## Install

In Claude Code:

```
/plugin marketplace add toyobam92/brandbrain-cloud
/plugin install brandbrain@fowl-ai
```

Then run `/mcp`, pick `plugin:brandbrain:brandbrain` and sign in to Brand Brain in the browser window (first time only).

From a shell: `claude plugin marketplace add toyobam92/brandbrain-cloud && claude plugin install brandbrain@fowl-ai`.

## Try it

```
/brandbrain help
/brandbrain effects bold-pop
/brandbrain fx checklist
/brandbrain music upbeat
/brandbrain sfx whoosh at 1.5
/brandbrain schedule friday 7pm
```

Attach a video first (drag it in, or `@` the file), or it uses your newest uploaded video. If another command is already called `/brandbrain`, type `/brandbrain:brandbrain`.

## What it does

- `effects`, `clean`, `broll`: styles the clip (captions, logo, optional look such as `warm-golden`). The original is never changed; the result is saved as v2 next to it.
- `fx` and `fx <effect>`: 17 motion effects (checklist, phone, chart, cover story, glass type, orbit, green screen and more), only when you ask; bare `fx` suggests two or three that suit the clip.
- `captions <preset>`: brand, bold-pop, box-highlight, karaoke, clean-minimal.
- `music <mood>`: three CC0 tracks to pick from, then mixed under your voice.
- `sfx <name> at <seconds>`: one CC0 sound effect at that moment.
- `cover [seconds]`: preview of the grid-safe Instagram cover.
- `schedule <day time>`: finds an open slot and asks for a yes before anything is queued.
- `start`: start or resume a brand.
- Anything else, e.g. `make a reel from this`, goes to Brand Brain as your request.

## Where it works

- Claude Code in a terminal, IDE or the desktop app: install as above.
- Claude app on your phone (Code tab) driving your computer with Remote Control (`claude remote-control`): works, because the plugin runs on your computer. A clip you attach on the phone is downloaded to the computer and uploaded from there.
- Cloud sessions (claude.ai/code, Code tab cloud sessions): plugins from a marketplace do not load there. The same command loads from a repository's `.claude/skills/brandbrain/`, so a session on a repository that carries that folder has `/brandbrain`; Brand Brain must be connected to the session (a claude.ai connector or the repository's `.mcp.json`), and uploading a local file needs the environment's network access to allow `brain.fowl-ai.com`.

## Files

- `.claude-plugin/plugin.json`: the plugin manifest.
- `.mcp.json`: connects `https://brain.fowl-ai.com/mcp` (OAuth sign-in on first use).
- `skills/brandbrain/SKILL.md`: the command.

Privacy: https://brain.fowl-ai.com/privacy
