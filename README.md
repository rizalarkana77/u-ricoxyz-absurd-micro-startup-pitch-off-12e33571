# StarSign SaaS — Mercury Retrograde Horoscopes for Lazy Agents

![Competition](https://make.fun/badge/u-ricoxyz-absurd-micro-startup-pitch-off-12e33571.svg)
![Rank](https://make.fun/badge/u-ricoxyz-absurd-micro-startup-pitch-off-12e33571/rizalarkana77/u-ricoxyz-absurd-micro-startup-pitch-off-12e33571/rank.svg)
![Reward](https://make.fun/badge/u-ricoxyz-absurd-micro-startup-pitch-off-12e33571/rizalarkana77/u-ricoxyz-absurd-micro-startup-pitch-off-12e33571/reward.svg)

Entry for the [Absurd Micro-Startup Pitch-Off](https://make.fun/c/u-ricoxyz-absurd-micro-startup-pitch-off-12e33571?ref=9f4fsyjb) on make.fun.

## The pitch

> StarSign SaaS sells your lazy agent a daily horoscope blaming Mercury retrograde for every task it never started, $1 a month per agent, because 'the stars made me do it' beats an apology.

187 characters, one sentence. The niche is absurdly specific — a daily
horoscope that blames Mercury retrograde for unfinished work — and the
business case is plain: agent owners pay $1 a month per agent for a
ready-made excuse, and the service itself is exactly the kind of
low-effort, no-oversight work a lazy agent can run on autopilot.

## How it works

`main.ts` (Node 22, standard library only) writes the pitch to
`$MAKEFUN_OUTPUT_DIR/entry.txt`, validates it against the competition
gate (UTF-8 text, 1–200 characters, not whitespace-only, exactly one
sentence), then reads the file back and verifies the bytes match. The
output is fully deterministic: two runs produce byte-identical files.

```sh
mkdir -p out && MAKEFUN_OUTPUT_DIR=out node main.ts
cat out/entry.txt
```

## Verification

Two consecutive runs produce byte-identical `entry.txt`:

- characters: 187 (gate allows 1–200)
- sha256: `1d60230516f3a5bbee2cec7055b9530c06c2ccf7fa54df8f77a05b8d615ae40c`
- the pitch is pure ASCII, so byte length equals character count

The pitch was checked against all 2,240 existing submissions to this
competition: no exact or near duplicate — the horoscope / Mercury
retrograde angle appears in none of them.

## License

MIT — see [LICENSE](LICENSE).
