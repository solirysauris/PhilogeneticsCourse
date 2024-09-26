# 1. Commands and tools used

The following packages were installed through conda, bioconda channel:
  1. mafft
  2. FastTree

First, all the sequencing files were united as one:
```
cat *.fasta > merged_all.fasta                     
```
Alignment using Mafft's default parameters:
```
mafft --auto merged_all.fasta > aligned_all.fasta
```
Building the tree:
```
FastTree -gtr -nt  aligned_all.fasta > tree2.newick
```
To make visualisations of the trees, online tool TreeDyn 198.3 was used:

http://www.phylogeny.fr/one_task.cgi?task_type=treedyn

# 2. Calcuations 

Number of mutations for each case was obtained with Unipro Ugene's statistical tools. Central African sample was used as a reference. 

1. To calculate the mitochondrial Eve's age, the sample with the biggest number of mutations was found. The most distinct sample was the Chinese one (haplogruo B4d1), the number of mutations was 94.

> 94 * 5000 : 2 = 235 000

So we assign out mitochondrial Eve age of 235 000 years.

2. To estimate the separation time for Neanderthal and Denisovan branches, the same calcilations were performed to find the maximum amount of mutations amongst the Neanderthal and the Denisovan samples.

Neanderthal branch:

> 224 * 5000 : 2 = 560 000

Denisovan branch:

> 389 * 5000 : 2 = 942 500

Which allows as to conclude that the last common ancestor shred by Homo sapiens and the Denisovans lived approximately 942 500 years ago. Homo sapiens and the Neanderthals splitted 400 000 years later, approximately 560 000 years ago. 
