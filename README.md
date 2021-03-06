# PRDHOUS
PRDHOUS stands for Probing RNASeq Datasets for Hidden Or Undiscovered Species.
This is a supportive material for an Mphil thesis of Lukas Konecny. 
This tool wass designed to find and assemble cytochrome oxidase 1 (COX1) sequences present in a provided RNASeq datasets.
COX1 sequences are provided as a FASTA file with specific formating of the headers.
RNASeq datasets are provided as list of SRA accession numbers from NCBI.
The tool is based on a Python script "SRA_parasites_final". To run the tool, you need to download the script and all the necessary software that the tool works with
that includes - MAGIC-BLAST, TransDecoder, Megahit, Samtools.
The text file "ncbi_gastropoda_all.txt" contains all SRA accession numbers for RNAseq datasets of gastropods used for the analysis in the thesis. 
The database files 
"mollusca_platyhelminthes_no_biomphalaria_bioawk_cdhit_final.fasta",
"mollusca_platyhelminthes_merged_bioawk_cdhit_1.fasta",
"mollusca_platyhelminthes_merged_bioawk_no_pfeiferi_cdhit1_final1.fasta",
"mollusca_platyhelminthes_noplanorb_bioawk_cdhit_final.fasta",
"nematoda_merged_bioawk_cdhit_1.fasta" are databses used in the analyses presented in the thesis. 

The tool run as follows: SRA_parasites_final -fi [path/to/database] -sra [path/to/SRAlist] -tpm 1  -n [number of threads] [optional arguments]

Required arguments:
-sra  The list of SRA accession numbers
-fi input database of COI genes in FASTA format
-tpm  Transcripts per million threshold
-n  Number of CPU threads used for the analyses

Optional arguments:
-O  Output folder name
-t  Timing of individual steps of the analysis
-e  “gap extend” parameter of MAGIC BLAST
-o  “gap open” parameter of MAGIC BLAST
-p  “penalty” parameter of MAGIC BLAST
-ws “word size” parameter of MAGIC BLAST

