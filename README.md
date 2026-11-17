# ecs124_media

Public media assets for ECS 124 (Theory and Practice of Bioinformatics, UC Davis).

This repository exists so that figures can be referenced by URL from Google Docs
and other documents. Course materials themselves live in the private repository
`ucdavis/ECS124`.

## Layout

Media is organized by subject, one folder per subject:

| folder | subject |
|---|---|
| `unit1_notes/` | figures for the Unit 1 notes |

## unit1_notes/

Figures for the Unit 1 notes. Each figure is provided twice: an SVG (the vector
source, for slides and print) and a PNG (for Google Docs, which cannot embed SVG).

| figure | what it shows |
|---|---|
| `z-case1-atatag` | Z-algorithm case 1 at i = 2 on P = ATATAG — no Z-box covers i |
| `z-case2a-atatag` | case 2a at i = 3 — the answer lies inside the box, no comparison |
| `z-case2b-atatag` | case 2b at i = 4 — the box runs out at r, the scan continues |
| `kmp-f-atatag` | KMP-F on P = ATATAG — Z-boxes over the pattern, and the Z, A, M, S, F arrays |
| `z-boxes-aabcaabxaaz` | the Z-boxes of P = aabcaabxaaz drawn over the pattern, with the Z array underneath |
| `z-case2-inside` | schematic of case 2: index i inside the right-most Z-box, with α, β, twin and known |
| `z-case2a-inside` | schematic of case 2a: Z[twin] < known, so Z[i] = Z[twin] |
| `z-case2b-extends` | schematic of case 2b: Z[twin] ≥ known, so the scan continues past r |
| `z-match-atatag` | Z values of S = P$T for P = ATATAG, T = ATATATAGATA — Z[9] = m marks the occurrence at index 2 of T |
