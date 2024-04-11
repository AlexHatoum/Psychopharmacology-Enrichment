The script above contains then necessary code to run the primary analysis in Hatoum et al. 2024, Psychiatric Genome-wide Association Study Enrichment Shows Promise for Future
Psychopharmaceutical Discoveries (https://www.medrxiv.org/content/medrxiv/early/2023/12/06/2023.12.05.23299434.full.pdf).  The script is annotated. You will need a minimum of 4 files. 
The first two come from FUMA, an automated online platform for annotation of GWAS summary statistics (See: https://fuma.ctglab.nl/, for more). Once a set of GWAS summary statistics 
run with "SNP2Gene", you can download the results for gene table and SNP table. In order to run the annotations in file, make sure you run SNP2Gene with CADD and regulome scoring options.
Several files are available on this github that have already been run for psychiatric GWAS. Once you have those files in hand, you will also need two others. A coding scheme of drug-gene 
pairing, and a coding scheme of treatment by indication. For drug-gene pairing, we used a coding scheme available from another group, which is publically available:
https://github.com/nybell/drugsets. Disease-indication pairing can be recreated using the copyrighted guide here: Stahl, S. M. (2024). Prescriber's guide: Stahl's essential psychopharmacology. Cambridge University Press.
but the first author was not given permission to share on github. 

In order to run the script, you will only need to change lines 9 (gene table), 10(SNP table), 13 (Gene-drug), and 15 (drug-indication) to accommodate your files. You may also need to change line 21,
depending on your coding scheme, and 29, depending on the size of your file. On line 29, [i,30] needs to be a column of gene-symbols for the script to run, i.e. in my example
"30" is the column in my table of gene-symbols, make sure that "30" is column number for your gene-table. There are more notes as annotations in the provided R script.  All analyses were
run using the same script and changing lines 9, 10, and 29 to accomadate different phenotypes. 
