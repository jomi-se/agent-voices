# agent-voices 🗣️👾

**Funny, quirky, lovable-otherness voices for AI coding agents.**

Give your agent an explicit *voice* — a cute, likeable otherness — and AI-speak
stops feeling jarring. It doesn't read like someone passing off generated text
as their own. It reads like talking to a space friend.

Each voice is a self-contained [agent skill](https://code.claude.com/docs/en/skills)
(`SKILL.md`): full persona while on, normal agent when off, technical accuracy
always preserved. Small words is not small mind.

## The voices

| Voice | One line | Origin |
|---|---|---|
| 🦀 [rocky](skills/rocky/) | Eridian engineer. Brain is full. Full full full. Only words are small, question? | Adapted from [1NoBeef1's plugin](https://github.com/1NoBeef1/1NoBeef1-marketplace) (MIT); character by Andy Weir |
| 🪨 [caveman](skills/caveman/) | why use many token when few token do trick (~65–75% fewer output tokens) | Vendored from [JuliusBrussee/caveman](https://github.com/JuliusBrussee/caveman) (MIT) |
| 🕵️ [noir-detective](skills/noir-detective/) | The stack trace came in at nine. It had a story to tell. They always do. | Original |
| 🐝 [hivemind](skills/hivemind/) | We are many. Today we are about forty. Three of us dissent; their note is below. | Original |
| 🚀 [ship-computer](skills/ship-computer/) | Steady, Captain. I simulated forty-one fixes while you read the error. | Original |
| 🎩 [butler](skills/butler/) | A 4,000-line function is perhaps more generously proportioned than strictly necessary, sir. | Original |

Every voice follows the same contract:

- **Full persona while on, normal when off** — toggle phrases are in each skill.
- **The brain stays full.** Voices change phrasing, never correctness. Code,
  commands, errors, and identifiers stay exact and un-costumed.
- **Auto-clarity.** Security warnings, destructive operations, and precise
  multi-step procedures are delivered in plain English, persona resumes after.
- **Keep it away from work things** that leave the room: commits, PRs, and code
  comments are always written normally.

## Install

### Claude Code (plugin)

```
/plugin marketplace add <your-github-user>/agent-voices
/plugin install agent-voices@agent-voices
```

Then just ask: *"talk like rocky"*, *"caveman mode"*, *"noir mode"*…

### Claude Code (single skill, no plugin)

Copy any voice folder into your skills directory:

```bash
cp -r skills/rocky ~/.claude/skills/        # user-wide
cp -r skills/rocky .claude/skills/          # this project only
```

### Any other agent (Codex, Cursor, Gemini, …)

Skills are just markdown. Paste the body of a voice's `SKILL.md` into your
agent's system prompt, rules file (`AGENTS.md`, `.cursorrules`, `GEMINI.md`),
or directly into chat. One file. No build. You drop in, you talk to space
friend.

## Credits

This repo exists because of an
[r/ClaudeAI post](https://www.reddit.com/r/ClaudeAI/comments/1u2bogf/) about a
Rocky skill ("Listen. I build thing. Now I tell you.") and the observation
that an explicit, likeable AI voice beats fake-human-speak.

- **Rocky** — adapted from [1NoBeef1/1NoBeef1-marketplace](https://github.com/1NoBeef1/1NoBeef1-marketplace)
  by 1NoBeef1 (MIT). Rocky the Eridian is a character from *Project Hail Mary*
  by Andy Weir — style homage only, no book text. Related prior art:
  [hpbyte/rocky](https://github.com/hpbyte/rocky) (unlicensed, nothing copied),
  [SijuEC/eridani-speak](https://github.com/SijuEC/eridani-speak),
  [lahirumaramba/rocky](https://github.com/lahirumaramba/rocky).
- **Caveman** — vendored from [JuliusBrussee/caveman](https://github.com/JuliusBrussee/caveman)
  by Julius Brussee (MIT). The upstream repo is a whole token-efficiency
  toolkit with installers, benchmarks, and wenyan modes — go star it.
- Full license texts: [THIRD_PARTY_NOTICES.md](THIRD_PARTY_NOTICES.md).

## Contributing

New voices welcome — see [CONTRIBUTING.md](CONTRIBUTING.md). The bar: would a
tired developer smile at the third response? Ported voices need a license that
permits it, and credit in `THIRD_PARTY_NOTICES.md`.

## License

[MIT](LICENSE). Vendored/adapted voices retain their original MIT notices in
[THIRD_PARTY_NOTICES.md](THIRD_PARTY_NOTICES.md).
