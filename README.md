# SARS_CoV_2_origin_research

This repository contains source code for metagenomic analysis of RaTG13 as part of SARS-CoV-2 origin research.

### Datasets

Two gzipped fastq files containing SRA's for RaTG13 assembly can be found at links below. This dataset was released at 2020-02-13

SRX7724752	https://www.ncbi.nlm.nih.gov/sra/?term=SRX7724752

https://sra-pub-sars-cov2.s3.amazonaws.com/sra-src/SRR11085797/Sars_SL3_R1_171127.fastq.gz

https://sra-pub-sars-cov2.s3.amazonaws.com/sra-src/SRR11085797/Sars_SL3_R2_171127.fastq.gz

### Installation

Install conda (miniconda3 with python 3.6 used here)
conda create -n blastasm 
conda activate blastasm
conda install bioconda megahit matplotlib

download SPAdes, uncompress and add bin to path
export PATH="$PATH:~/appdir/SPAdes-3.15.0-Linux/bin"

### Methodology

1) Run MEGAHIT and or CoronaSPAdes commands to assemble nucleotide contigs. NB the results of assembly we used can be found in this repository.

2) Set dataset locations in Blast2.ipynb and run to generate a consensus fasta file and QC plots.

3) Set multiple consensus fasta file locations in Fasta_Gap_Comparison.ipynb to calculate missing nucleotide locations accross all consensus sequences, and generate QC plots.



