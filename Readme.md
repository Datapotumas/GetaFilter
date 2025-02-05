# GetaFilter

Pipeline for annotation filter

## Installtation

```shell
git clone git@github.com:Datapotumas/GetaFilter.git
```

## Requirement

[trinity](https://github.com/trinityrnaseq/trinityrnaseq) util script align_and_estimate_abundance.pl need

[PfamScan](https://github.com/SMRUCC/GCModeller/tree/master/src/interops/scripts/PfamScan/PfamScan) need to be install

[hmmer](https://github.com/EddyRivasLab/hmmer) 1.3 and database need  to be install

[samtools](https://github.com/samtools/samtools) 1.6 need to be install

[bedtools](https://github.com/arq5x/bedtools2) 2.31.1 need to be install

[ncbiblast](https://blast.ncbi.nlm.nih.gov/Blast.cgi) need to be install 

[ParaFly](https://github.com/ParaFly/ParaFly.git) need to be install

## Options and usage

```
perl GetaFilter.pl
************************************************************************
    Usage: filterGetaAnno -c config.txt -t threads -s INT
      -h : help and usage.
      -c : config.txt
      -t : threads
      -s : step 1 or 2
      -a : augustus support cutoff (default 30), optional
      -f : FPKM cutoff (default 3), optional
      -b : bedtools coverage (default 0.5), optional
************************************************************************

perl GetaFilter.pl -c config.txt -t 20 -s 1
```

### config file

```
###Program setting
triUtil=/path/to/align_and_estimate_abundance.pl
PfamScan=/path/to/PfamScan/pfam_scan.pl
HMMDB=/path/to/hmmer-3.1/
###RNA-seq reads setting
R1=/path/to/R1.fq.gz
R2=/path/to/R2.fq.gz
###Homologs
HOMO=/path/to/homo.pro.fasta
###Geta annotation
CDS=/path/to/CDS.fasta
PEP=/path/to/pep.fasta
GENE=/path/to/gene.fasta
GFF=/path/to/gff3
PWD=/path/to/PWD
```
