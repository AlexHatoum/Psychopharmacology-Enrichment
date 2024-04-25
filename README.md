The script above contains the necessary code to run the primary analysis in Hatoum et al. 2024, Psychiatric Genome-wide Association Study Enrichment Shows Promise for Future
Psychopharmaceutical Discoveries (https://www.medrxiv.org/content/medrxiv/early/2023/12/06/2023.12.05.23299434.full.pdf).  The script is annotated. You will need a minimum of 4 files. 
The first two come from FUMA, an automated online platform for annotation of GWAS summary statistics (See: https://fuma.ctglab.nl/). Once a set of GWAS summary statistics 
run with "SNP2Gene" in FUMA, you can download the results for gene table and SNP table. In order to have all the necessary genome annotations to recreate analysis in the paper, make sure you run SNP2Gene with CADD and regulome scoring options clicked. Several files are available (here: https://wustl.box.com/s/c94gup91y63r30zonr1rt4dhvs6wj4e9) that have already been run for psychiatric GWAS through this function, so you will not need to run themselves. Once you have those two FUMA files in hand, you will also need two other files. A coding scheme of drug-gene pairing, and a coding scheme of treatment by indication. For drug-gene pairing, we used a coding scheme available from another group, which is publically available: https://github.com/nybell/drugsets. Drug-indication pairing in our study can be recreated using the copyrighted guide here: Stahl, S. M. (2024). Prescriber's guide: Stahl's essential psychopharmacology. Cambridge University Press. Unfortunately, the first author was not given permission to share as a table on github, so the original guide must be used to recreate analysis. In place of these previusly published files, you will find here: (Link to Box), example files that will show the file format needed to run the script. 

In order to run the script, you will only need to change lines 9 (gene table), 10(SNP table), 13 (Gene-drug), and 15 (drug-indication) to accommodate your files. You may also need to change line 21, depending on your coding scheme, and 29, depending on the size of your file. On line 29, [i,30] needs to be a column of gene-symbols for the script to run, i.e. in my example "30" is the column number in my table of gene-symbols, make sure that "30" is column number for your gene-table. All analyses were run using the same script and changing lines 9, 10, and 29 to accomadate different phenotypes. 
