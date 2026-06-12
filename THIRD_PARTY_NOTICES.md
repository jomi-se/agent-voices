# Third-party notices

This repository adapts material from the following projects. Both are
MIT-licensed; their original license texts are reproduced below.

## caveman

- **Voice:** `skills/caveman/`
- **Upstream:** <https://github.com/JuliusBrussee/caveman>
- **Author:** Julius Brussee
- **What we took:** the core `caveman` SKILL.md, lightly trimmed. The upstream
  project is much bigger — installers for 30+ agents, benchmarks, a compression
  CLI, review/commit skills, wenyan (classical Chinese) modes. If you like the
  voice, go get the full toolkit there.

```
MIT License

Copyright (c) 2026 Julius Brussee

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
```

## Rocky Mode

- **Voice:** `skills/rocky/`
- **Upstream:** <https://github.com/1NoBeef1/1NoBeef1-marketplace>
- **Author:** 1NoBeef1
- **What we took:** the dialect rules and mode instructions from the plugin's
  session-start hook, reworked into a single self-contained SKILL.md. The
  upstream plugin also ships Rocky-themed spinner verbs and tips for Claude
  Code, and a `/rocky` toggle command with persistence across sessions.

```
MIT License

Copyright (c) 2026 1NoBeef1

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
```

## Related projects we did **not** copy from (license or scope)

- [hpbyte/rocky](https://github.com/hpbyte/rocky) — a strong Rocky skill with
  benchmarks showing ~47% token savings. **No license file**, so nothing was
  copied; linked here as prior art and credit.
- [SijuEC/eridani-speak](https://github.com/SijuEC/eridani-speak) (MIT) —
  token compression library inspired by the same friendly alien engineer.
- [lahirumaramba/rocky](https://github.com/lahirumaramba/rocky) (MIT) — "Your
  Own Personal Eridanian Buddy."

## Character acknowledgements

Rocky the Eridian is a character from *Project Hail Mary* by Andy Weir. The
`rocky` voice here imitates a speech *style* (telegraphic grammar, repeated
words for emphasis, trailing ", question?") and contains no text from the
book. If you haven't read it: read it. It is good good good.
