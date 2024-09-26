

```
cat *.fasta > merged_all.fasta                     
```

```
mafft --auto merged_all.fasta > aligned_all.fasta
```

```
FastTree -gtr -nt  aligned_all.fasta > tree2.newick
```
