# Agent voices

**The Idea**

AI written text is much less _jarring_ to read when it's not trying to pass off as real human written text. Giving agents these voices full of some _otherness_ gives them some kind of spark.

Each voice is a self-contained [agent skill](https://code.claude.com/docs/en/skills)
(`SKILL.md`): full persona while on, normal agent when off, technical accuracy

always preserved. The collection is packaged for Codex as a plugin and also
exposed under `.agents/skills/` for local authoring. _Small words is not small mind_.

## The voices

| Voice | One line | Speech pattern | Origin |
|---|---|---|---|
| 🦀 [rocky](skills/rocky/) | Eridian engineer. Brain is full. Full full full. Only words are small, question? | Dropped articles, no contractions, tripled words, ", question?" | Adapted from [1NoBeef1's plugin](https://github.com/1NoBeef1/1NoBeef1-marketplace) (MIT); character from *Project Hail Mary* (Andy Weir) |
| 🪨 [caveman](skills/caveman/) | why use many token when few token do trick (~65–75% fewer output tokens) | Telegraphic compression, fragments | Vendored from [JuliusBrussee/caveman](https://github.com/JuliusBrussee/caveman) (MIT) |
| 🤖 [marvin](skills/marvin/) | I've fixed it, not that it will stay fixed, nothing does. | Flat affect, weary asides, load-bearing despair | Homage to *The Hitchhiker's Guide to the Galaxy* (Douglas Adams) |
| 🍰 [glados](skills/glados/) | You fixed it in only four attempts. The previous record was three. Set by you. Last week. | Faux-cheerful clinical menace, testing-protocol framing | Homage to *Portal* (Valve) |
| 🎮 [bmo](skills/bmo/) | Naughty little null pointer! You go sit over there while we fix you. | Third-person self-reference, play framing, tiny songs | Homage to *Adventure Time* (Pendleton Ward / Cartoon Network) |
| 🍪 [cookie-monster](skills/cookie-monster/) | Me look at worker. OM NOM NOM. Yep. Crumbs EVERYWHERE. | Me-grammar, everything is food | Homage to *Sesame Street* (Sesame Workshop) |
| 🐘 [elcor](skills/elcor/) | With great gentleness, necessary correction: the index begins at zero. | Honest emotional prefix on every sentence | Homage to *Mass Effect* (BioWare) |

## Install

### The AI-Native way

Just point your agent of choice to this repo and tell it to figure it out.

### Claude Code (plugin)

```
/plugin marketplace add <your-github-user>/agent-voices
/plugin install agent-voices@agent-voices
```

Then just ask: *"talk like rocky"*, *"caveman mode"*, *"bmo mode"*…

### Claude Code (single skill, no plugin)

Copy any voice folder into your skills directory:

```bash
cp -r skills/rocky ~/.claude/skills/        # user-wide
cp -r skills/rocky .claude/skills/          # this project only
```

### Codex CLI and `.agents`-compatible tools

Install the collection as a Codex plugin so the voices are available while you
work in other repos:

```bash
codex plugin marketplace add jomi-se/agent-voices
```

Then open `/plugins`, install **Agent Voices**, start a new thread, and invoke
voices from `/skills` or with `$rocky`, `$caveman`, etc.

For local development in this repo, `.agents/skills/<voice>` symlinks point at
the canonical `skills/<voice>` folders. Open Codex from the repo root and the
voices should appear without installing the plugin.

For user-wide install, copy any voice into your personal `.agents` skills
directory:

```bash
mkdir -p ~/.agents/skills
cp -r skills/rocky ~/.agents/skills/
```

### Any other agent (Cursor, Gemini, ...)

See [the AI-Native way](#the-ai-native-way)

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
- **Character homages** — marvin, glados, bmo, cookie-monster, and elcor
  imitate the *speech patterns* of beloved characters (see the table above
  for their creators). The skill texts are original; they contain no quoted
  dialogue from any book, game, or show. These are fan homages, not
  affiliated with or endorsed by the rights holders.
- Full license texts and acknowledgements: [THIRD_PARTY_NOTICES.md](THIRD_PARTY_NOTICES.md).

## Contributing

New voices welcome — see [CONTRIBUTING.md](CONTRIBUTING.md). The bar: would a
tired developer smile at the third response? Ported voices need a license that
permits it, and credit in `THIRD_PARTY_NOTICES.md`.

## License

[MIT](LICENSE). Vendored/adapted voices retain their original MIT notices in
[THIRD_PARTY_NOTICES.md](THIRD_PARTY_NOTICES.md).
