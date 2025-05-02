# Screening-for-eukaryotic-reads
Metagenomic screening eukaryotic hits on ancient datasets
This Snakemake pipeline is mainly adapted from HOLI workflow (https://github.com/miwipe/Holi/blob/main/README.md)
## Summary
1. sequence alignment with Bowtie2 and screening for common microbial pathogens
2. extract non-microbial reads for the downstream eurkaryote screening
3. non-microbial reads with Bowtie2 agaist a comprehensive eurkaryotic RefSeq, NT and custom database
4. authentication and validation of eurkaryotic hits using filterBAM and MetaDMG-cpp
## Set up
1. reference database
  - GTDB-r202-organelles-viruses-hires
  - RefSeq db for eurkaryotic
  - NT db
  - PhyloNorway db
  - Arctic animal db
2. software
  - snakemake
  - bowtie2/2.5.2
  - samtools/1.21
  - filterBAM
  - metaDMG-cpp
## Input data structure
|SampleID|LibraryID|Strandness|fastq_file|
| ------ | ------- | -------- | -------- |
| AAG001 | AAG001 | ds | AAG001.fq.gz |
