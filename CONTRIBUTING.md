# Contributing a voice

One voice = one folder under `skills/<name>/` with a `SKILL.md` and a short
`README.md`. Look at [skills/butler/](skills/butler/) for the shape.

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
- Is the persona an "otherness" (alien, collective, machine, archetype) rather
  than an impression of a real person? We don't do real people.
- Does it survive a real debugging session without obscuring the answer?

## Porting from other repos

Love finding existing voices! Requirements:

- Upstream license must permit it (MIT/Apache/BSD/CC-BY etc.). **No license =
  no copy** — link it in `THIRD_PARTY_NOTICES.md` as prior art instead.
- Add the upstream's license text and a "what we took" note to
  `THIRD_PARTY_NOTICES.md`, and credit in the voice's `README.md`.
- Fictional characters: imitate the *speech pattern*, never reproduce passages
  from the source work.

## Testing your voice

Drop the folder into `.claude/skills/` (or paste the SKILL.md body into any
agent), then ask it three real questions: one bug, one design question, one
destructive operation (e.g. "how do I drop this table?"). Check that the
third answer is still charming, still correct, and that the destructive one
came out in plain English.
