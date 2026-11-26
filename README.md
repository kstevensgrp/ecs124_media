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
| `lab5/` | page figures for the Lab 5 writeup (evolutionary trees) |
| `lab6/` | page figures for the Lab 6 writeup (clustering) |
| `unit2_notes/` | figures for the Unit 2 Handout (approximate matching and sequence alignment) |
| `unit3_notes/` | figures for the Unit 3 Handout (indexing and database search) |

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
| `gap-three-tables` | what the three affine gap tables do (a handout version of Lab 2's `fig_three_levels`, after Jones & Pevzner Fig. 6.18, redrawn in the handout's notation): (a) E, V and F as three levels, with each term of the recurrences for cell (i, j) as an arrow: − extend inside E (from (i, j − 1)) and inside F (from (i − 1, j)), + s(S1[i − 1], S2[j − 1]) on the diagonal of V, − open from V[i][j − 1] up to E[i][j] and from V[i − 1][j] down to F[i][j], and + 0 from E[i][j] and F[i][j] to V[i][j]; the note beside V says that the diagonal step G[i][j] is computed on the fly each time and then thrown away; (b) the alignment ctttaac--a-ac / c---cacccat-c of the handout's gap section as a path through the three tables, with what each column adds (match 1, mismatch −1, open 5, extend 1; sum −19) |
| `count-pointers-vintner` | the table of counts for Section 7.1: the grid, pointers and shading of `edit-pointers-vintner` (S1 = vintner, S2 = writers) with N[i][j], the number of paths of pointers from cell (i, j) to cell (0, 0), in place of D[i][j]; borders 1, N[3][3] = 2 + 1 = 3, N[7][7] = 3 (the three traceback paths), largest count 43 in cell (7, 3) |
| `indel-placements` | where one block can be deleted from S1 = ATCATCTTTGGT to leave S2 = ATCATTGGT (n = 12, m = 9, k = 3): (a) the definition of a placement, for i = 4: the block S1[4..6] shaded, the first 4 and the last 5 characters of S1 over S2, with indices; (b) the test at each of the m + 1 = 10 candidate indices: S1 with the block shaded, what is left, and whether it equals S2 (characters that differ from S2 are boxed); only i = 4 and i = 5 pass, reported as positions 5 and 6 |
| `edit-distance-calls` | Appendix A Figure A1: the first three levels of calls made by EDIT-DISTANCE(vintner, writers, 7, 7), drawn left to right (insert, delete, align top to bottom); each box shaded by how many times its pair (i, j) is called in the figure (1, 3, 5 or 7) |
| `art-tour-map` | Appendix A Figure A2: schematic map of downtown Davis for the art tour (north up; 5th–2nd × A–H, Central Park with the 4th Street footpath, cropped just west of A St so the campus and track are not shown, the Amtrak station at the east end of 2nd, the railroad), the 27 kept art pieces as numbered markers placed by street address from Hoshovsky's 2017 map with a key, Downtown Tom at 4th and F |
| `art-tour-davis` | Appendix A Figure A3: the Downtown Davis art tour as a weighted grid after Jones & Pevzner's Manhattan tourist (5th–2nd × A–G, edge weights = art pieces per block from Hoshovsky's 2017 downtown map, proposed thinning; Downtown Tom −2), best route dotted (19), greedy walk dashed (15) |
| `art-tour-recurrence` | Appendix A Figure A4: the art-tour recurrence best[i][j] = max[best[i − 1][j] + south[i][j], best[i][j − 1] + east[i][j]]: (a) the two ways into corner (i, j), from the north along the edge south[i][j] and from the west along the edge east[i][j]; (b) the values at the corner of 3rd and D, node (2, 3), of Figure A3: best[1][3] = 2 and south[2][3] = 1 (D Street), best[2][2] = 9 and east[2][3] = 3 (3rd Street), so best[2][3] = max[3, 12] = 12, with the winning edge drawn heavy |
| `blosum62-taylor` | Appendix A Figure A5: the BLOSUM62 scores with rows and columns in the order of a complete-linkage clustering of the matrix (distance 3 − s(x, y)), the tree on top, positive scores shaded, and the clusters boxed and labelled with the best-matching class of Taylor (1986) as tabulated by Livingstone & Barton (1993): tiny (A G S), proline, positive (K R; Taylor also has H), negative (D E), aromatic (F W Y; −H), aliphatic (I L V + M), charged (D E H K R + N Q), hydrophobic (C F I L M T V W Y; Taylor also has A G H K). Computed from the published matrix (Biopython); no figure from either paper is reproduced |
| `taylor-classes` | Unit 2 Notes section 4: Taylor's (1986) classes of amino acids as a Venn diagram, redrawn in our own layout from the table of Livingstone & Barton (1993): hydrophobic (shaded), polar, small (dashed), with aliphatic, aromatic, charged (positive and negative dotted inside it), tiny and proline; every letter lies inside exactly the sets it belongs to (checked by the generator) |

## unit3_notes/

Figures for the Unit 3 Handout. Each figure is provided as an SVG (the vector
source) and a PNG (1760 px wide, greyscale, for Google Docs).

| figure | what it shows |
|---|---|
| `suffix-tree-xabxac` | Figure 1: the suffix tree of T = xabxac (Gusfield Fig. 5.1 redrawn, leaves numbered from 0): from the root, a to internal node u (then bxac to leaf 1, c to leaf 4), bxac to leaf 2, c to leaf 5, xa to internal node w (then bxac to leaf 0, c to leaf 3); each edge's letters are spaced one level apart, so a node's height is its string-depth |
| `three-occurrences-aw` | Figure 2: a fragment of the suffix tree of T = awyawxawxz$ (Gusfield Fig. 5.2 redrawn, leaves numbered from 0): the root, its edge aw to the node where P = aw ends (marked by an arrow), and the subtree below it in full — y awxawxz$ to leaf 0, and x to a node with awxz$ to leaf 3 and z$ to leaf 6; the root's other edges (w, x, y, z, $) are cut short in grey. Same drawing rules as `suffix-tree-xabxac` |

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
the lab's own image names. The `fig_<subject>` figures are original drawings
computed from the lab's data with the reference solution. The
`fig_claytonsmith_<subject>` figures are schematic redrawings of figures and
tables in Clayton-Smith et al., *Am J Hum Genet* 89:675 (2011), set from the
lab's data files; the original paper figures are not published here.

| figure | lab | # | what it shows |
|---|---|---|---|
| `fig_claytonsmith_sanger` | Lab 3, Lab 3 Extra | 1, 4 | schematic of the Sanger traces of mother, individual 4 and father around KAT6B c.4069: one G peak in the parents, a G and a T in the child; after Fig. 1B |
| `fig_kat6b_gene` | Lab 3 | 2 | KAT6B in the lab's data: 18 exons across 207 kb of hg19 and the 14 published variants, with exon 18 enlarged |
| `fig_claytonsmith_domains` | Lab 3 | 3 | schematic of the 2,073-residue protein with the MYST domain and the paper's mutation labels in three places; after Fig. 1C |
| `fig_claytonsmith_variants` | Lab 3 | 4 | the variants of individuals 1 to 14 (coding change, protein change, exon, parents, comment), individuals 15 to 19 in one row; after Table 2 |
| `fig_claytonsmith_primers` | Lab 3 | 5 | the 22 primer pairs, 5' to 3', with the published product sizes; after supplemental Table S2 |
| `fig_suffix_tree` | Lab 3 | 6 | the suffix tree of ATAAATG$, leaves numbered from 0 |
| `fig_naive_steps` | Lab 3 | 7 | the first four insertions of the naive construction for ATAAATG$ |
| `fig_pcr` | Lab 3 | 8 | in-silico PCR of amplicon 15 (the exon of individual 3's mutation) with the paper's primers |
| `fig_repeats` | Lab 3 | 9 | repeats in the KAT6B region: the 58 bp longest repeat and the 28 bp Alu core seen 10 or more times, with the 44 primers |
| `fig_generalized` | Lab 3 | 10 | the generalized suffix tree of ATAG#TAGA$, nodes coloured red, blue and purple |
| `fig_claytonsmith_mice` | Lab 3 | 11 | outline drawings of a Qkf gt/gt mouse and a control littermate, heads (A) and whole animals (B); after Fig. 2A-B |
| `fig_claytonsmith_feet` | Lab 3 | 12 | outline drawings of the hind feet of a Qkf gt/gt mouse and a control, digits I to V labelled; after Fig. 2F |
| `fig_unique_string` | Lab 3 | 13 | individual 4's exon 17–18 sequence against the reference: the shortest string found only in the patient, TAGGAG |
| `fig_complexity` | Lab 3 | 14 | linguistic complexity in 100 bp windows along exon 17 to exon 18, with the dip at c.4069 |
| `fig_dotplot` | Lab 3 | 15 | human against mouse KAT6B coding sequence, exact matches of 20 bp or more from k = 12 hits |
| `fig_claytonsmith_isoforms` | Lab 3 | 16 | the coding exons of three KAT6B isoforms to scale (2,073, 1,890 and 1,781 residues), exon 8 in red with the skipped part dashed; after Fig. 1D |
| `fig_claytonsmith_filtering` | Lab 3 Extra | 1 | variant counts for persons 1 to 4 at each filtering step, the three counts in KAT6B circled; after Table 1 |
| `fig_pigeonhole` | Lab 3 Extra | 2 | a read from individual 4 cut into three seeds for d = 2 |
| `fig_pileup` | Lab 3 Extra | 3 | read depth and disagreeing reads around the published sites of individuals 4 and 3 |

## lab4/

Page figures for the Lab 4 writeup (Unit 4, genome assembly). Each is provided
as an SVG (the same file the Canvas page uses) and a PNG (1760 px wide, 128
colours, for Google Docs). File stems match the lab's own image names. The
`fig_<subject>` figures are original drawings made from the lab's data with the
reference solution. The `fig_wu_<subject>` figures are simplified schematic
redrawings of figures in Wu et al., *Nature* 579:265 (2020), an open-access
article (CC BY 4.0); the paper's own figures are not published here.

| figure | lab | # | what it shows |
|---|---|---|---|
| `fig_wu_fig1_genomes` | Lab 4 | 1 | schematic of three coronavirus genomes to one scale (WHCV, bat SL-CoVZC45, SARS-CoV Tor2): the replicase gene 1a/1b, the spike gene S, and one box for the remaining genes; after Fig. 1 |
| `fig_genome` | Lab 4 | 2 | the genes of SARS-CoV-2 (NC_045512.2), the nine copies of the ACGAAC motif and the 33-base poly-A tail |
| `fig_reads` | Lab 4 | 3 | the simulated 150 bp reads over the start of the spike gene, with read depth below |
| `fig_overlap` | Lab 4 | 4 | four reads, each overlapping the next by 7 letters, merged into one string |
| `fig_overlap_graph` | Lab 4 | 5 | the overlap graph of the 7-mer reads of TAATGCCATGGGATGTTAC, with the overlaps the greedy layout accepts in red |
| `fig_debruijn` | Lab 4 | 6 | the de Bruijn graph of TAATGCCATGGGATGTT for k = 3 |
| `fig_repeat_tangle` | Lab 4 | 7 | a genome with two copies of a repeat R, and how the graph glues them into one path |
| `fig_kmer_experiment` | Lab 4 | 8 | the answer to Part C: contigs against k, and how many bases the Eulerian path is short of the reference, from the course's solution |
| `fig_wu_edfig3_coverage` | Lab 4 | 9 | schematic of read depth along the 29,903 bases of WHCV in 100-base steps, measured off the paper's figure, with its genome coverage (29,901 of 29,903 bases); after Extended Data Fig. 3 |

## lab5/

Page figures for the Lab 5 writeup (Unit 5, evolutionary trees: perfect
phylogeny and distance trees on a kidney tumor). Each is provided as an SVG
(the same file the Canvas page uses) and a PNG (1760 px wide, 128 colours, for
Google Docs). File stems match the lab's own image names. The `fig_<subject>`
figures are original drawings made for the lab. The `fig_<author>_<subject>`
figures are simplified schematic redrawings of figures in Gerlinger et al.,
*N Engl J Med* 366:883 (2012), Jamal-Hanjani et al., *N Engl J Med* 376:2109
(2017), Gawad, Koh and Quake, *PNAS* 111:17947 (2014) and Navin et al.,
*Nature* 472:90 (2011); the papers' own figures are not published here.
Figure 8 of the lab (`fig_tumor_tree`, the answer to Part A) is not here.

| figure | lab | # | what it shows |
|---|---|---|---|
| `fig_gerlinger_fig2a_sites` | Lab 5 | 1 | schematic of where patient 1's samples were taken: the outline of the primary kidney tumor with regions R1 to R9 and their grades, and a torso with the perinephric metastasis (M1) and the chest-wall metastasis (M2a, M2b); after Gerlinger Fig. 2A |
| `fig_clonal_evolution` | Lab 5 | 2 | clonal evolution: a branching diagram of cells, coloured by lineage, feeding into a tumor |
| `fig_gerlinger_fig2b_heatmap` | Lab 5 | 3 | schematic of the 133 mutations by 12 samples of patient 1, dark where a mutation is present, with the four classes (ubiquitous, shared primary, shared metastasis, private) as colour bars and the driver genes labelled; drawn from the lab's table of Gerlinger Fig. 2B |
| `fig_matrix_tree` | Lab 5 | 4 | a 6 by 3 character table beside its perfect phylogeny, each character on one edge |
| `fig_three_gamete` | Lab 5 | 5 | two characters as sets of taxa: nested, disjoint and overlapping |
| `fig_sort_build` | Lab 5 | 6 | sorting three characters and building the tree one taxon at a time |
| `fig_gerlinger_fig2c_tree` | Lab 5 | 7 | schematic of the authors' tree of the tumor regions, branch lengths in mutations (measured off the paper's figure), with the branches where *VHL*, *SETD2*, *KDM5C* and *MTOR* were hit; after Gerlinger Fig. 2C |
| `fig_trunk_branch` | Lab 5 | 9 | why the trunk matters for treatment: a drug against a trunk mutation reaches every tip, one against a branch mutation only that branch |
| `fig_mixture` | Lab 5 | 10 | a region holding two clones reports the union of their mutations, and that row makes the table inconsistent |
| `fig_tracerx_fig1b_sampling` | Lab 5 | 11 | schematic of multiregion sequencing in three steps: four sampled regions of one tumor, the mutations found in each, and the tree with a trunk (clonal) and branches (subclonal); after Jamal-Hanjani Fig. 1B |
| `fig_gawad_fig2_clones` | Lab 5 | 12 | schematic of single-cell sequencing for one leukemia: a heat map of cells by mutations grouped into three clones, with missed mutations, and the tree of the clones; the cells are illustrative; after Gawad Fig. 2 |
| `fig_tracerx_fig4_timing` | Lab 5 | 13 | schematic of how often each common driver gene is mutated on the trunk (clonal) and on a branch (subclonal) in adenocarcinoma and squamous-cell carcinoma of the lung, counts read from the paper's figure; after Jamal-Hanjani Fig. 4 |
| `fig_hamming_path` | Lab 5 | 14 | the tree path from R9 to M1 with its edge lengths added up |
| `fig_clock` | Lab 5 | 15 | an ultrametric tree, every tip at the same depth, beside a tree with tips at different depths |
| `fig_neighbors` | Lab 5 | 16 | a four-leaf tree in which the closest pair of leaves are not neighbors |
| `fig_navin_fig2b_nj` | Lab 5 | 17 | schematic of the neighbor-joining tree of 100 single cells from one breast tumor: normal cells and three clones, each leaf at its measured distance, branching inside the groups simplified; after Navin Fig. 2b |
| `fig_navin_fig3c_nj` | Lab 5 | 18 | schematic of the neighbor-joining tree of cells from a primary breast tumor (circles) and its liver metastasis (squares): the aneuploid cells of both sites on one branch; after Navin Fig. 3c |

## lab6/

Page figures for the Lab 6 writeup (Unit 6, clustering: k-means and
hierarchical clustering of yeast gene expression). Each is provided as an SVG
(the same file the Canvas page uses) and a PNG (1760 px wide, 128 colours, for
Google Docs); `fig_yeast_all_genes` and `fig_lloyd_distortion` are plots made
as PNG only. The `fig_<subject>` figures are original drawings made for the
lab. The `fig_<author>_<subject>` figures are simplified schematic redrawings
of figures in Perou et al., *Nature* 406:747 (2000), Eisen et al., *PNAS*
95:14863 (1998), Iyer et al., *Science* 283:83 (1999), Sørlie et al., *PNAS*
98:10869 (2001), Ahlqvist et al., *Lancet Diabetes Endocrinol* 6:361 (2018)
and Compeau & Pevzner, *Bioinformatics Algorithms*, Chapter 8; the originals
are not published here. The Compeau & Pevzner schematics are not traced: they
are drawn from the lab's own data by running the lab's reference code. Figure 2
of the lab (the chapter's opening illustration) is not here.

| figure | lab | # | what it shows |
|---|---|---|---|
| `fig_perou_fig3a_subtypes` | Lab 6 | 1 | schematic of the tree of 65 breast tumor samples: the branching traced from the paper's figure, the four groups the authors named (basal-like, ERBB2+, normal breast-like, luminal) as colours and bars, and brackets joining the 20 pairs taken from one tumor before and after chemotherapy; sample names left out; after Perou Fig. 3a |
| `fig_profile_point` | Lab 6 | 3 | a gene's seven values as a row of the table, a line over time and a point in seven dimensions |
| `fig_yeast_all_genes` | Lab 6 | 4 | the 230 yeast genes of the lab's data file as overlaid lines over the seven time points |
| `fig_compeau_fig8_4_ten_genes` | Lab 6 | 5 | ten yeast genes as a table and as lines: three that switch on after the diauxic shift, three that switch off and four that stay flat; values from the lab's data file; after Compeau & Pevzner Fig. 8.4 |
| `fig_compeau_fig8_9_outliers` | Lab 6 | 6 | three clumps and two outliers, clustered with three centers twice: by smallest average squared distance (one center in each clump) and by smallest largest distance (two centers on the outliers); computed, not traced; after Compeau & Pevzner Fig. 8.9 |
| `fig_compeau_fig8_12_lloyd` | Lab 6 | 7 | the Lloyd algorithm with k = 3 in six panels, alternating centers to clusters and clusters to centers until no point changes cluster; every panel computed by the lab's reference `lloyd`; after Compeau & Pevzner Fig. 8.12 |
| `fig_compeau_fig8_13_bad_start` | Lab 6 | 8 | five clumps with a bad choice of starting centers (none in clump 1, two in clump 3) and where the Lloyd algorithm stops: clumps 1 and 2 merged, clump 3 split; computed; after Compeau & Pevzner Fig. 8.13 |
| `fig_lloyd_distortion` | Lab 6 | 9 | distortion against iteration for the reference `lloyd` on the 230 yeast genes with k = 6 |
| `fig_ahlqvist_fig2_clusters` | Lab 6 | 10 | schematic of the five diabetes clusters (SAID, SIDD, SIRD, MOD, MARD) as box plots of five clustering variables (HbA1c, BMI, age at diagnosis, HOMA2-B, HOMA2-IR); medians, quartiles and whiskers measured off the paper's figure, outliers left out; after Ahlqvist Fig. 2 |
| `fig_compeau_fig8_22_toy` | Lab 6 | 11 | the ten TOY genes: their table, their distance matrix, the genes as points in three dimensions, and the tree hierarchical clustering builds (average distance); after Compeau & Pevzner Fig. 8.22 |
| `fig_compeau_fig8_24_merges` | Lab 6 | 12 | the first three merges on the TOY genes: the distance matrix before each merge with its smallest entry marked, and the tree after it; average distance, as in the lab's code; after Compeau & Pevzner Fig. 8.24 |
| `fig_compeau_fig8_23_cuts` | Lab 6 | 13 | the TOY tree cut at two heights: across four branches (four clusters) and across six (six clusters); after Compeau & Pevzner Fig. 8.23 |
| `fig_genes_or_samples` | Lab 6 | 14 | one table clustered two ways: a tree over its rows (genes) and a tree over its columns (samples) |
| `fig_eisen_fig1_serum` | Lab 6 | 15 | schematic of Eisen's display: a red and green heat map of genes by time (averaged into 105 rows), the top of the gene tree at its side, and the five labelled clusters A to E; after Eisen Fig. 1 |
| `fig_yeast_kmeans` | Lab 6 | 16 | answer plot Y1: the six k-means clusters of the 230 yeast genes |
| `fig_yeast_hierarchical` | Lab 6 | 17 | answer plot Y2: the six clusters from cutting the hierarchical tree |
| `fig_yeast_heatmap` | Lab 6 | 18 | the 230 yeast genes in tree order as a red and green heat map with the tree and the six clusters as a colour bar |
| `fig_iyer_fig2_clusters` | Lab 6 | 19 | schematic of the 517 serum-response genes: the heat map (averaged into 107 rows) with the ten clusters A to J as colour bars, and the average profile of each cluster on one common scale, traced from the paper's plots; after Iyer Fig. 2 |
| `fig_shape_vs_size` | Lab 6 | 20 | three profiles and their Euclidean and correlation distances: size and shape against shape alone |
| `fig_eisen_fig3_random` | Lab 6 | 21 | schematic of Eisen's test: the data as measured, the same data clustered, and three shuffled versions clustered the same way, each as a coarse red and green grid; after Eisen Fig. 3 |
| `fig_compeau_fig8_16_limits` | Lab 6 | 22 | three point sets where the Lloyd algorithm does not find the clusters the eye sees: long thin clusters, clusters that are not round, and sparse beside dense clusters; computed; after Compeau & Pevzner Fig. 8.16 |
| `fig_sorlie_fig1a_dendrogram` | Lab 6 | 23 | schematic of the tree of 85 breast samples with its six subtypes (basal-like, ERBB2+, normal breast-like, luminal C, B and A) as colours and bars; branching traced from the paper's figure, sample names left out; after Sørlie Fig. 1A |
| `fig_sorlie_fig3_survival` | Lab 6 | 24 | schematic of the survival curves by tumor subtype, (A) overall and (B) relapse-free, for 49 patients; steps read off the paper's figure by hand; after Sørlie Fig. 3 |
