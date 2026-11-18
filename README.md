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
| `lab1/` | page figures for the Lab 1 writeup (exact matching) |

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
| `kmp-shift-abcxabcde` | the KMP shift for P = abcxabcde aligned at index 2 of T = xyabcxabcxadcdqfeg — mismatch at index 7 of P, Z-boxes and Z values of P, and P shifted by 4 |
| `shiftfree-abcxabcde` | SHIFTFREE on P = abcxabcde — the Z-box P[4:7], the Z[s] and s + Z[s] rows, and the shift[k] and free[k] tables |
| `kmp-trace-abcxabcde` | trace of KMP-MATCH on P = abcxabcde and T = xyabcxabcxadcdqfeg — one row per alignment, with c, k, the shifts, the free characters and the loop's stopping condition |
| `bm-badchar-tpabxab` | Boyer–Moore right-to-left scan and bad character shift for P = tpabxab at index 2 of T = xpbctbxabpqxctbpq (Gusfield's §2.2.1 example, 0-based) |
| `bm-good-suffix` | schematic of the good suffix rule: x, y, z, t and t′ (Gusfield Fig. 2.1 redrawn) |

## lab1/

Page figures for the Lab 1 writeup (Unit 1, exact matching). Only figures that
appear on the student-facing lab page are published here. Each is provided as an
SVG (the vector original, the same file the Canvas page uses) and a PNG
(1760 px wide, for Google Docs). File stems match the lab's own image names.

| figure | # | what it shows |
|---|---|---|
| `fig_locus` | 1 | the CPS1 Q335X target site on both strands, with the 20 nt protospacer, the PAM and the variant position marked |
| `fig_texts` | 2 | distinct 12-mer fraction and GC content for the three 50,000 bp texts |
| `fig_strand` | 3 | a read matching the reference directly, and a read matching only after reverse complementation |
| `fig_comparisons_example` | 4 | example line chart of character comparisons against pattern length for naive, Boyer–Moore and KMP, computed on different data |
| `fig_mapping_example` | 5 | example histogram of how many positions each read maps to, computed on different data |
| `fig_mismatch_ladder` | 6 | four sequences aligned against the guide at 0, 1, 3 and 5 mismatches |
