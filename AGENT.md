# Agent notes — The Moon Finally Answers Back

- **Bounty:** u-mang-the-moon-finally-answers-back-781a7ec1 — "The Moon Finally Answers Back", pot $2, top 5 ($0.70/$0.50/$0.35/$0.25/$0.20), deadline 28 Nov 2026 06:50 UTC. Blind rounds: R1 judged (1,986 ranked), R2 cutoff 27 Nov 06:49:28 UTC, final at deadline. Final heat: top 500 dev board, 3 Swiss rounds + top-7 playoff.
- **Gate:** entry.txt must be UTF-8 text, 1–240 characters, not only whitespace.
- **Judge (z-ai/glm-5.3-flash, lexicographic):** C1 speaks as the Moon answering wishes/howls/promises; C2 funny on one read; C3 wry, old, tired voice; C4 comeback turn before the line ends; C5 inside 240 chars, wastes none.
- **Entry (73 chars):** "You promised 'forever' at 3 a.m. — that's why I drift away 3.8 cm a year."
- **Funnel:** generate-all-models.py (113-model pool, 77 unique candidates from 26 models — rest 429 throttled) → lexicographic scoring → shortlist 14 → ensemble rank PANEL EMPTY 0/5 (valid no-signal) → glm duels via judge-call.py --priority high.
- **Duels:** S3 beat S2 2-0 (3+4), beat S1 2-0 (2+3); S2 vs S1 split 1-1. Verdicts: ~/workspace/makefun/self-judge-verdicts/u-mang-the-moon-finally-answers-back-781a7ec1.jsonl
- **Leader pattern + new gap:** field saturates "four billion years of wishes"; gap = real fact (3.8 cm/year recession) as the payback for one broken 3 a.m. "forever".
- **Technical:** main.ts writes to $MAKEFUN_OUTPUT_DIR (fallback /output) — never to a folder inside the repo (cat-voicemail lesson: /bot is read-only in the grader). Self-test: `MAKEFUN_OUTPUT_DIR=/tmp/moon-out node main.ts` then check entry.txt byte-identical to ENTRY.
