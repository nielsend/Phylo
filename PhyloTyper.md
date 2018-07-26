# PhyloTyper

#### A script that returns Clermont's Original[^1] and Revised[^2] Phylogenetic Groups for *Escherichia coli* when given genomic data in a FASTA format.

This script was used in Nielsen *et al.* (2018). Working title: Association of Outer Membrane Protein A.

<br>

## Assumptions
 * Python is installed on machine. [Download python 2.7 here](https://www.anaconda.com/download/#macos).
 * User has bash terminal. 

<br>

## Input
1. Open Terminal
2. ```Call phylotyper, give phylotyper FASTA files```   **e.g.:** ```./PhyloTyper.py fasta_files/*```


<br>


## Output
* A .csv file will be created containing concise information about the strain.
	* The file will be named ```phylotyped_mm_dd_yyy_hh_mm.csv```
	* The file will be created wherever the script is located.
	* E.g.: ![]()
* Verbose output on the screen is also an output. This output can be sent to a file.
```./PhyloTyper.py fasta_files/* > Information.txt```

```
Accession: U00096.3

----------ORIGINAL PHYLOTYPING-----------
chuA results:
Primer:  ATCCTGACCGTTGGTT No primer match.
Primer:  TGCCGCCAGTACCAAA No primer match.
Primer:  GACGAACCAACGGTCA No primer match.
Primer:  TGTCTTTGGTACTGGC No primer match.
Original chuA negative

yjaA results:
Primer:  CAGCGTCTCCTGACA No primer match.
Primer:  ATGGAGAATGCGTTCC No primer match.
Primer:  TGAAGTGTCAGGAGA Exact Match:  [4213366]
Primer:  GTTGAGGAACGCATTC Exact Match:  [4213556]
Original yjaA positive

TspE4C2.1 results:
Primer:  TGAATGCCCCGACAT No primer match.
Primer:  CGCGCCAACAAAGTA No primer match.
Primer:  GAGTAATGTCGGGGC Near Match:  [624146] Matches:  ['GATTAATGTCGGGGC']
Primer:  CGTAATACTTTGTTG No primer match.
Original TspE4C2.1 negative


----------REVISED PHLYLOTYPING-----------
Revised chuA results:
Primer:  ATGGTACCGGACGAACCAAC No primer match.
Primer:  TGTCTTTGGTACTGGCGGCA No primer match.
Primer:  TGCCGCCAGTACCAAAGACA No primer match.
Primer:  GTTGGTTCGTCCGGTACCAT No primer match.
Revised chuA negative!

Revised yjaA results:
Primer:  CAAACGTGAAGTGTCAGGAG Exact Match:  [4213360]
Primer:  CACAGGTTGAGGAACGCATT Exact Match:  [4213551]
Primer:  AATGCGTTCCTCAACCTGTG No primer match.
Primer:  CTCCTGACACTTCACGTTTG No primer match.
Revised yjaA positive!

Revised TspE4C2.1 results:
Primer:  CACTATTCGTAAGGTCATCC No primer match.
Primer:  GCGACCCGCAGCGATAAACT No primer match.
Primer:  AGTTTATCGCTGCGGGTCGC No primer match.
Primer:  GGATGACCTTACGAATAGTG No primer match.
Revised TspE4.C2.1 negative!

Revised arpA (400 bp) results:
Primer:  TCTCCCCATACCGTACGCTA No primer match.
Primer:  GCAAGCTGGCGAATAGCGTT No primer match.
Primer:  AACGCTATTCGCCAGCTTGC Exact Match:  [4219989]
Primer:  TAGCGTACGGTATGGGGAGA Exact Match:  [4220369]
Revised arpA positive!

Revised arpA (301 bp) results:
Primer:  GATTCCATCTTGTCAAAATATGCC Near Match:  [4221869] Matches:  ['GATTCCATCTTGTCAAAATATGCT']
Primer:  CTCTTGGGAATTCTTTTTCTTTTC Near Match:  [4222146] Matches:  ['TTCTTGGGAATTCTTTTTCTTTTC']
Primer:  GAAAAGAAAAAGAATTCCCAAGAG No primer match.
Primer:  GGCATATTTTGACAAGATGGAATC No primer match.
Revised arpA (301 bp) positive!

Revised trpA results:
Primer:  AGTTTTATGCCCAGTGCGAG No primer match.
Primer:  GGGCGTGACCGGCGCAGA No primer match.
Primer:  TCTGCGCCGGTCACGCCC Near Match:  [1316733] Matches:  ['TCTGCGCCGGTCACGCCT']
Primer:  CTCGCACTGGGCATAAAACT Near Match:  [1316933] Matches:  ['TTCGCACTGGGCATAAAACT']
Revised trpA positive!

Revised trpBA results:
Primer:  CGGCGATAAAGACATCTTCAC No primer match.
Primer:  CTTCCGCCAGGCCGCGTTGC No primer match.
Primer:  GCAACGCGGCCTGGCGGAAG Exact Match:  [1316857]
Primer:  GTGAAGATGTCTTTATCGCCG Exact Match:  [1317326]
Revised trpBA positive!

-----------CONCLUSIONS----------

 ORIGINAL PHYLOGROUP: 
Group A

 REVISED PHYLOGROUP: 
Group C

Have a great day!
```

<br>
<br>

##Citations
[^1]: [Olivier Clermont, O., Bonacorsi, S., and Bingen, E. (2000), Rapid and Simple Determination of the Escherichia coli Phylogenetic Group Appl. Environ. Microbiol. October 2000 66:10 4555-4558; doi:10.1128/AEM. 66.10.4555-4558](http://aem.asm.org/content/66/10/4555.short). 
[^2]: [Clermont, O. , Christenson, J. K., Denamur, E. and Gordon, D. M. (2013), A new E. coli phylo‐typing method. Environmental Microbiology Reports, 5: 58-65. doi:10.1111/1758-2229.12019](https://onlinelibrary.wiley.com/doi/abs/10.1111/1758-2229.12019)

