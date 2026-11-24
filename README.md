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
| `lab2/` | page figures for the Lab 2 and Lab 2 Extra writeups (approximate matching) |
| `lab3/` | page figures for the Lab 3 and Lab 3 Extra writeups (indexing and database search) |
| `lab4/` | page figures for the Lab 4 writeup (genome assembly) |
| `unit2_notes/` | figures for the Unit 2 Handout (approximate matching and sequence alignment) |

## unit1_notes/

Figures for the Unit 1 notes. Each figure is provided twice: an SVG (the vector
source, for slides and print) and a PNG (for Google Docs, which cannot embed SVG).

| figure | what it shows |
|---|---|
| `z-linear-atatag` | Z-LINEAR on P = ATATAG as one figure: the trace table (case, l, r, Z[i] after each step) and one panel for each case — (a) case 1 at i = 2, (b) case 2a at i = 3, (c) case 2b at i = 4 |
| `z-case1-atatag` | (superseded by `z-linear-atatag`) Z-algorithm case 1 at i = 2 on P = ATATAG — no Z-box covers i |
| `z-case2a-atatag` | (superseded) case 2a at i = 3 — the answer lies inside the box, no comparison |
| `z-case2b-atatag` | (superseded) case 2b at i = 4 — the box runs out at r, the scan continues |
| `kmp-f-atatag` | KMP-F on P = ATATAG — Z-boxes over the pattern, and the Z, A, M, S, F arrays |
| `z-boxes-aabcaabxaaz` | the Z-boxes of P = aabcaabxaaz drawn over the pattern, with the Z array underneath |
| `z-case2-inside` | schematic of case 2: index i inside the right-most Z-box, with α, β, twin and known |
| `z-case2a-inside` | schematic of case 2a: Z[twin] < known, so Z[i] = Z[twin] |
| `z-case2b-extends` | schematic of case 2b: Z[twin] ≥ known, so the scan continues past r |
| `z-match-atatag` | Z values of S = P$T for P = ATATAG, T = ATATATAGATA — Z[9] = m marks the occurrence at index 2 of T |
| `kmp-shift-abcxabcde` | the KMP shift for P = abcxabcde aligned at index 2 of T = xyabcxabcxadcdqfeg — mismatch at index 7 of P, Z-boxes and Z values of P, and P shifted by 4 |
| `shiftfree-abcxabcde` | SHIFTFREE on P = abcxabcde — the Z-box P[4:7], the Z[s] and s + Z[s] rows, and the shift[k] and free[k] tables |
| `kmp-trace-abcxabcde` | trace of KMP-MATCH on P = abcxabcde and T = xyabcxabcxadcdqfeg — one row per alignment, with c, k, the shifts, the free characters and the loop's stopping condition (assignments written with ←) |
| `bm-badchar-tpabxab` | Boyer–Moore right-to-left scan and bad character shift for P = tpabxab at index 2 of T = xpbctbxabpqxctbpq (Gusfield's §2.2.1 example, 0-based) |
| `bm-bad-character` | schematic of the bad character rule in three cases: x absent from P, two copies of x left of the mismatch, and copies on both sides (rightmost inside t, shift 1) |
| `bm-good-suffix` | schematic of the good suffix rule: x, y, z, t and t′ (Gusfield Fig. 2.1 redrawn) |

## unit2_notes/

Figures for the Unit 2 Handout. Each figure is provided as an SVG (the vector
source) and a PNG (1760 px wide, greyscale, for Google Docs).

| figure | what it shows |
|---|---|
| `hamming-kj-target` | Hamming distance from the patient's 23-character KJ target S1 (CPS1 Q335X) to the wild-type CPS1 sequence (1), the ATP7B intron site (4) and the DNAI7 exon site (5); differing characters shaded |
| `hamming-f508del` | Hamming distance between the CFTR sequence around F508 (S1 = GAAAATATCATCTTTGGTGTTT, 22 characters) and the patient's F508del sequence (S2, 19): (a) S2 at the left end of S1, 5; (b) at the right end, 5; (c) S3 = S2 with three dashes inserted, 3. Overhanging characters are not counted |
| `edit-table-vintner` | the edit distance table for S1 = vintner and S2 = writers (Gusfield Figs 11.1 and 11.2 redrawn): (a) row 0 and column 0 from the base conditions; (b) filled row by row up to D[4][3], with D[4][4] next and the three cells it reads shaded |
| `edit-pointers-vintner` | the same table with every pointer (Gusfield Fig 11.3 redrawn): ← to (i, j − 1), ↑ to (i − 1, j), ↖ to (i − 1, j − 1); the cells on the three traceback paths from (7, 7) to (0, 0) shaded |
| `local-pointers-pqraxabcstvq` | the local alignment (Smith-Waterman) table for S1 = pqraxabcstvq and S2 = xyaxbacsll (the example of Gusfield §11.7) with match 2, mismatch −2 and gap 1, in the layout of `edit-pointers-vintner`: a pointer out of every cell with a positive value; the largest value, 8, is in cell (9, 8), and the cells on the two tracebacks to the zero cell (3, 2) are shaded (axab-cs / ax-bacs and ax-abcs / axba-cs) |
| `gap-types` | the three types of alignment behind the affine gap recurrences (after Gusfield Fig. 11.8, redrawn): an alignment of the first i characters of S1 and the first j of S2 ends with S2[j − 1] opposite a space (type 1, E[i][j]), with S1[i − 1] opposite a space (type 2, F[i][j]), or with S1[i − 1] opposite S2[j − 1] (type 3, G[i][j]); each panel shows the last column and what the rest of the alignment covers |
| `gap-three-tables` | what the three affine gap tables do (a handout version of Lab 2's `fig_three_levels`, after Jones & Pevzner Fig. 6.18, redrawn in the handout's notation): (a) E, V and F as three levels, with each term of the recurrences for cell (i, j) as an arrow: − extend inside E (from (i, j − 1)) and inside F (from (i − 1, j)), + s(S1[i − 1], S2[j − 1]) on the diagonal of V, − open from V[i][j − 1] up to E[i][j] and from V[i − 1][j] down to F[i][j], and + 0 from E[i][j] and F[i][j] to V[i][j]; (b) the alignment ctttaac--a-ac / c---cacccat-c of the handout's gap section as a path through the three tables, with what each column adds (match 1, mismatch −1, open 5, extend 1; sum −19) |
| `edit-distance-calls` | Appendix A Figure A1: the first three levels of calls made by EDIT-DISTANCE(vintner, writers, 7, 7), drawn left to right (insert, delete, align top to bottom); each box shaded by how many times its pair (i, j) is called in the figure (1, 3, 5 or 7) |
| `art-tour-map` | Appendix A Figure A2: schematic map of downtown Davis for the art tour (north up; 5th–2nd × A–H, Central Park with the 4th Street footpath, cropped just west of A St so the campus and track are not shown, the Amtrak station at the east end of 2nd, the railroad), the 27 kept art pieces as numbered markers placed by street address from Hoshovsky's 2017 map with a key, Downtown Tom at 4th and F |
| `art-tour-davis` | Appendix A Figure A3: the Downtown Davis art tour as a weighted grid after Jones & Pevzner's Manhattan tourist (5th–2nd × A–G, edge weights = art pieces per block from Hoshovsky's 2017 downtown map, proposed thinning; Downtown Tom −2), best route dotted (19), greedy walk dashed (15) |

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

## lab2/

Page figures for the Lab 2 and Lab 2 Extra writeups (Unit 2, approximate
matching). Each is provided as an SVG (the same file the Canvas page uses) and a
PNG for Google Docs: 1760 px wide for the original drawings, and the
instructor's own 2x-3x export for the schematics. File stems match the lab's
own image names. Schematic redrawings of published figures are published here;
the original paper figures are not.

| figure | where | what it shows |
|---|---|---|
| `fig_riordan_f508_gel` | Lab 2 Fig. 1, Lab 2 Extra Fig. 1 | schematic of the normal and cystic fibrosis sequencing gels around F508del, read with the B primer (forward strand) and D primer (reverse strand); after Riordan et al., *Science* 245:1066 (1989), Fig. 4 |
| `fig_f508_site` | Lab 2 Fig. 2 | CFTR exon 11 with codons N505 to V510 and two ways to place the 3-base deletion. |
| `fig_hamming_vs_edit` | Lab 2 Fig. 3 | Reference and patient aligned position by position with ten mismatches, then with a gap and no mismatches. |
| `fig_dp_grid` | Lab 2 Fig. 4 | A 13 by 10 table of edit distances with the optimal paths highlighted. |
| `fig_riordan_f508_sequence` | Lab 2 Fig. 5 | schematic of four lines of CFTR cDNA (1441-1680) with the translation above, the F508 12-mer shaded and the three deleted bases bracketed; after Riordan et al. 1989, Fig. 2 (excerpt) |
| `fig_ingram_hbs` | Lab 2 Fig. 6 | schematic of Ingram's two-dimensional map of peptide No. 4: ten labelled spots, solid outlines for hemoglobin A, dashed for hemoglobin S; after Ingram, *Nature* 180:326 (1957), Fig. 1 |
| `fig_sickle` | Lab 2 Fig. 7 | Two protein sequences differing at residue 6, and a bar chart of substitution costs. |
| `fig_brunkow_nw_alignment` | Lab 2 Fig. 8 | schematic of mouse and human FOXP3 aligned with Needleman-Wunsch: identity bars, the forkhead domain shaded, the scurfy site starred; after Brunkow et al., *Nat Genet* 27:68 (2001), Fig. 5 |
| `fig_wildin_forkhead` | Lab 2 Fig. 9 | schematic of the forkhead domains of human and mouse scurfin aligned with HNF3-gamma and Genesis, with the IPEX mutations on top; after Wildin et al., *Nat Genet* 27:18 (2001), Fig. 1 |
| `fig_global_local` | Lab 2 Fig. 10 | A dot plot of FOXP3 against FOXA3 with the local alignment path in the forkhead domain. |
| `fig_brunkow_scurfy_insertion` | Lab 2 Fig. 11 | schematic of the *Foxp3* exons with the wild-type and scurfy sequences of exon 8; after Brunkow et al. 2001, Fig. 1b |
| `fig_three_levels` | Lab 2 Fig. 12 | Three stacked grids labelled with the stub's tables E, V and F (upper, middle and lower level) with the edges between them. |
| `fig_cooptimal` | Lab 2 Fig. 13 | Six alignments of the same two 12-base sequences, two of them highlighted. |
| `fig_tan_vcf` | Lab 2 Fig. 14 | schematic of one CA deletion in a CA repeat written four ways in VCF, only one normalized; after Tan, Abecasis & Kang, *Bioinformatics* 31:2202 (2015), Fig. 1 |
| `fig_counts` | Lab 2 Fig. 15 | Bar chart of 600, 20 and 4 optimal alignments on a log scale. |
| `fig_fitting` | Lab 2 Extra Fig. 2 | A line plot of edit distance against chr7 position with one sharp dip to 3 inside exon 11. |
| `fig_band` | Lab 2 Extra Fig. 3 | An edit-distance table with only a diagonal band of cells filled. |
| `fig_two_rows` | Lab 2 Extra Fig. 4 | A grid in which only two adjacent rows are kept. |
| `fig_band_example` | Lab 2 Extra Fig. 5 | Example line chart of percent of cells filled and percent of reads resolved against k. |
| `fig_riordan_nbf_alignment` | Lab 2 Extra Fig. 6 | schematic of three conserved segments of CFTR's nucleotide-binding domains aligned with the same segments of 18 other proteins, F508 starred; after Riordan et al. 1989, Fig. 6 |
| `fig_cube` | Lab 2 Extra Fig. 7 | A cube with arrows from seven corners to the eighth. |

## lab3/

Page figures for the Lab 3 and Lab 3 Extra writeups (Unit 3, indexing and
database search). Each is provided as an SVG (the same file the Canvas page
uses) and a PNG (1760 px wide, 128 colours, for Google Docs). File stems match
the lab's own image names. All are original drawings computed from the lab's
data with the reference solution; the figures reproduced from Clayton-Smith et
al. (2011) are not published here.

| figure | lab | # | what it shows |
|---|---|---|---|
| `fig_kat6b_gene` | Lab 3 | 2 | KAT6B in the lab's data: 18 exons across 207 kb of GRCh37 and the 14 published variants, with exon 18 enlarged |
| `fig_suffix_tree` | Lab 3 | 6 | the suffix tree of ATAAATG$, leaves numbered from 1 |
| `fig_naive_steps` | Lab 3 | 7 | the first four insertions of the naive construction for ATAAATG$ |
| `fig_pcr` | Lab 3 | 8 | in-silico PCR of amplicon 15 (the exon of individual 3's mutation) with the paper's primers |
| `fig_repeats` | Lab 3 | 9 | repeats in the KAT6B region: the 58 bp longest repeat and the 28 bp Alu core seen 10 or more times, with the 44 primers |
| `fig_generalized` | Lab 3 | 10 | the generalized suffix tree of ATAG#TAGA$, nodes coloured red, blue and purple |
| `fig_unique_string` | Lab 3 | 13 | individual 4's exon 17–18 sequence against the reference: the shortest string found only in the patient, TAGGAG |
| `fig_complexity` | Lab 3 | 14 | linguistic complexity in 100 bp windows along exon 17 to exon 18, with the dip at c.4069 |
| `fig_dotplot` | Lab 3 | 15 | human against mouse KAT6B coding sequence, exact matches of 20 bp or more from k = 12 hits |
| `fig_pigeonhole` | Lab 3 Extra | 2 | a read from individual 4 cut into three seeds for d = 2 |
| `fig_pileup` | Lab 3 Extra | 3 | read depth and disagreeing reads around the published sites of individuals 4 and 3 |

## lab4/

Page figures for the Lab 4 writeup (Unit 4, genome assembly). Each is provided
as an SVG (the same file the Canvas page uses) and a PNG (1760 px wide, 128
colours, for Google Docs). File stems match the lab's own image names. All are
original drawings made from the lab's data with the reference solution; the
figures reproduced from Wu et al. (2020) are not published here.

| figure | lab | # | what it shows |
|---|---|---|---|
| `fig_genome` | Lab 4 | 2 | the genes of SARS-CoV-2 (NC_045512.2), the nine copies of the ACGAAC motif and the 33-base poly-A tail |
| `fig_reads` | Lab 4 | 3 | the simulated 150 bp reads over the start of the spike gene, with read depth below |
| `fig_overlap` | Lab 4 | 4 | four reads, each overlapping the next by 7 letters, merged into one string |
| `fig_overlap_graph` | Lab 4 | 5 | the overlap graph of the 7-mer reads of TAATGCCATGGGATGTTAC, with the overlaps the greedy layout accepts in red |
| `fig_debruijn` | Lab 4 | 6 | the de Bruijn graph of TAATGCCATGGGATGTT for k = 3 |
| `fig_repeat_tangle` | Lab 4 | 7 | a genome with two copies of a repeat R, and how the graph glues them into one path |
