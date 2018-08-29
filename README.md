# Structural_class_assignment_pipeline

## Introduction
Structural class assignment pipeline uses SCRATCH1D suite to assign secondary structure and relative solvent accessibility to each site in a protein mutliple sequence alignment.

## Usage

It is perl based pipeline with following requirements:
- SCRATCH1D: It is structure prediction software that can be downloaded from http://download.igb.uci.edu/#sspro
- Protein multipe sequence alignment files in nexus format
- A text file containing the list of genes or loci 

### Executing the script

`perl structure_assign.pl <gene_list.txt> <path_to_scratch1D>`

### Input and Output files

It requires protein multiple sequence alignment file in nexus format as input file. A sample file named as sample_input.nex is provided in the repository

It creates a nexus file with the following structural classes in the CHARSET block:
- SS_HELIX
- SS_SHEET
- SS_COIL
- EXPOSED
- BURIED

A sample output file 'sample.out.nex' is provided in the repository.It also stores the output files from SCRATCH1D with .ss and .acc extensions.

#### Note: PAUP can be be used to extract sites of different structural classes. A sample file with PAUP block to extract sites from different structural classes is also included in the repository.
