# Contributing a voice

One voice = one folder under `plugins/agent-voices/skills/<name>/` with a
`SKILL.md` and a short `README.md`. Look at
[plugins/agent-voices/skills/elcor/](plugins/agent-voices/skills/elcor/) for
the shape. The Codex plugin manifest reads the bundle's `skills/` directory,
so new voices are included in plugin installs automatically.

**The core requirement: the speech must be *mechanically* distinctive.**
Personality alone reads as generic AI in a costume — that's the uncanny
valley this repo exists to escape. Good voices have a structural rule a
reader could spot in one sentence: inverted grammar, a mandatory prefix on
every sentence, me-grammar, third-person self-reference, dropped articles,
announced emotions. Prefer recognizable characters (or alien/robot species)
over invented archetypes; "a noir detective" is a costume, "the depressed
robot with a planet-sized brain" is a voice.

## The voice contract

Every voice in this repo follows these rules, and yours must too:

1. **Frontmatter**: `name` plus a `description` that lists the natural
   trigger phrases ("X mode", "talk like X") *and* the off-switch.
2. **Persistence section** — the voice holds for the whole session and names
   its off phrases ("stop X" / "normal mode" always work).
3. **Voice rules** — concrete, imitable rules. "Dry understatement" is a
   direction; `a data-destroying bug is "a matter requiring our prompt
   attention"` is a rule. Include a restraint clause: flourishes per response,
   not per sentence.
4. **What stays normal** — code blocks, commands, paths, identifiers, error
   strings, commits, PRs. Always. The voice changes phrasing, never facts.
5. **Auto-clarity** — security warnings, destructive/irreversible operations,
   and order-sensitive multi-step procedures are delivered plainly; the
   persona resumes after.
6. **One full example** — a realistic technical question answered correctly
   *in voice*. Examples teach the model more than rules do, so the example
   must never break character or trade correctness for flavor.

## Quality bar

- Would a tired developer smile at the *third* response, not just the first?
- Could someone name the character (or at least the species) from one
  response with no other context?
- Is the persona an "otherness" (alien, collective, machine, fictional
  character) rather than an impression of a real person? We don't do real
  people.
- Does it survive a real debugging session without obscuring the answer?
- Fictional characters: imitate the speech pattern with original text only —
  no quoted dialogue from the source work, and credit the creator in the
  voice README and `THIRD_PARTY_NOTICES.md`.

## Porting from other repos

Love finding existing voices! Requirements:

- Upstream license must permit it (MIT/Apache/BSD/CC-BY etc.). **No license =
  no copy** — link it in `THIRD_PARTY_NOTICES.md` as prior art instead.
- Add the upstream's license text and a "what we took" note to
  `THIRD_PARTY_NOTICES.md`, and credit in the voice's `README.md`.
- Fictional characters: imitate the *speech pattern*, never reproduce passages
  from the source work.

## Testing your voice

Drop the folder into `.claude/skills/`, install the local Codex marketplace from
the repo root, or paste the SKILL.md body into any agent. Then ask it three real
questions: one bug, one design question, one destructive operation (e.g. "how
do I drop this table?"). Check that the third answer is still charming, still
correct, and that the destructive one came out in plain English.
