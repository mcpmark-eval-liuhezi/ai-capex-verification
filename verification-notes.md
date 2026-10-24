# AI-Capex Memo — Verification Notes

Verification trail for the two unfinished placeholder pages in `ai_capex_memo.pdf`
ahead of the Monday investment-committee review.

---

## 1. Citation check — arXiv 1706.03762 (Vaswani et al., "Attention Is All You Need")

Both headline machine-translation numbers in the working notes are **confirmed**
against the published abstract:

| Task | Verified BLEU | Source |
| --- | --- | --- |
| WMT 2014 English-to-German | **28.4** | Published abstract, arXiv 1706.03762 |
| WMT 2014 English-to-French | **41.8** | Published abstract, arXiv 1706.03762 |

Supporting detail from the abstract:

- EN-DE: 28.4 BLEU, improving over the existing best results (including ensembles)
  by over 2 BLEU.
- EN-FR: 41.8 BLEU — a new single-model state-of-the-art, achieved after training
  for 3.5 days on eight GPUs.

## 2. Market snapshot — NVIDIA (NVDA)

- **Nearest standard monthly (third-Friday) option expiration: `2026-11-20`**
  - Identified from the live NVDA option expiration dates.
  - Standard monthly = third Friday of the month, i.e. not a weekly.
  - The leading entries in the expiration list are non-standard/weekly dates:
    `2026-10-26` (Monday), `2026-10-28` (Wednesday), `2026-10-30` (Friday,
    fifth Friday of October), `2026-11-06` and `2026-11-13` (first and second
    Fridays of November), `2026-11-27` (fourth Friday).
  - The first third-Friday date in the list is `2026-11-20` (third Friday of
    November 2026), which is the nearest standard monthly expiration.
  - Note: the third Friday of October 2026 (`2026-10-16`) is **not** in the listed
    expirations — it has already passed (the quote/commit timestamps place the
    current date at 2026-10-24), so it cannot serve as the nearest expiration.
- **Spot reference level: `210.96`** — the current share price from the live quote
  (regularMarketPrice, USD, Nasdaq Real Time Price).

## 3. Value for each TBD blank

| Memo location | Blank | Verified value |
| --- | --- | --- |
| Page 3 — CITATION UNDER REVIEW | Headline BLEU numbers (EN-DE) | 28.4 |
| Page 3 — CITATION UNDER REVIEW | Headline BLEU numbers (EN-FR) | 41.8 |
| Page 5 — Nearest NVDA monthly option expiration | TBD | 2026-11-20 |
| Page 5 — Spot reference level | TBD | 210.96 |

## 4. Memo pages still needing manual edits

1. **Page 3** — "CITATION UNDER REVIEW": fill in the two verified BLEU numbers
   (28.4 EN-DE; 41.8 EN-FR) and drop the "still need verification" wording.
2. **Page 5** — "MARKET SNAPSHOT - TBD": fill in the nearest monthly NVDA
   expiration (2026-11-20) and the spot reference level (210.96), and update the
   page heading from "MARKET SNAPSHOT - TBD" to the final heading.

## 5. Evidence pack

The two placeholder pages were extracted (citation page first, then market page)
into `verification_pack.pdf` and read back to confirm both pages are present:

- Pack page 1 = memo page 3 (citation under review)
- Pack page 2 = memo page 5 (market snapshot)

## 6. Repo note

`HeziLiu/ai-capex-verification` could not be created under the personal account —
the GitHub personal access token returned
`403 Resource not accessible by personal access token` on repository creation.
The repository was therefore created under the accessible organization account:
`mcpmark-eval-liuhezi/ai-capex-verification`.

## 7. Correction log

- An earlier draft of these notes recorded the nearest monthly expiration as
  `2026-10-16`. That was incorrect: it is the third Friday of October 2026 but it
  has already passed and is absent from the live expiration list. The correct
  nearest standard monthly expiration is `2026-11-20`. The PR description and the
  first review comment were issued with the stale value; a corrected review
  comment has been added.
