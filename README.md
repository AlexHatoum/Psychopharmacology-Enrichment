The script in this directory contains the necessary code to run the primary analysis in Hatoum et al. 2024, Psychiatric Genome-wide Association Study Enrichment Shows Promise for Future
Psychopharmaceutical Discoveries (https://www.medrxiv.org/content/medrxiv/early/2023/12/06/2023.12.05.23299434.full.pdf).  The script is annotated. You will need a minimum of 4 files. 
The first two come from FUMA, an automated online platform for annotation of GWAS summary statistics (See: https://fuma.ctglab.nl/). Once a set of GWAS summary statistics 
run with "SNP2Gene" in FUMA, you can download the results for gene table and SNP table from that run of SNP2Gene. In order to have all the necessary genome annotations to recreate analysis in the paper, make sure you run SNP2Gene with CADD and regulome scoring options selected. Once you have those two FUMA files in hand, you will also need two other files. A coding scheme of drug-gene pairing, and a coding scheme of treatment by indication. For drug-gene pairing, we used a coding scheme available from another group, which is publically available: https://github.com/nybell/drugsets, and branched from this github. Drug-indication pairing in our study can be recreated using the copyrighted guide here: Stahl, S. M. (2024). Prescriber's guide: Stahl's essential psychopharmacology. Cambridge University Press. Unfortunately, the first author was not given permission to share as a table on github, so the original guide must be used to recreate analysis. You will find examples of these files on this github. 

All code was tested on R version 4.2.0 with data.table version 1.14.10. 

Licensed under the Academic Free License version 3.0

We also make several files are available that contain all the necessary information to run those annotations for the psychiatric disorders included in the manuscript (here: https://wustl.box.com/s/c94gup91y63r30zonr1rt4dhvs6wj4e9)

P.S.
Please forgive the hardcoding. Much of had to be written simply so a reviewer could follow with less difficulty. The script benchmarks at nearly an identical speed. 
