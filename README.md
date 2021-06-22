# RWAS

RWAS is a method for connecting properties of regulatory regions to risk built using MAGMA's covariate mode. These commands were run using MAGMA 1.06, later versions may require some tweaking.

1. Annotate SNPs to regulatory regions:
```
magma \
--annotate --snp-loc [SNP location file].bim \
--gene-loc [input regulatory regions].loc \
--out [output file prefix]
```

2. Regulatory region- based GWAS:
```
magma \
--bfile [1000 genomes bfile prefix] \
--pval [GWAS summary statistics file name] N=[N of GWA study]  \
--gene-annot [input file name].genes.annot \
--out [output file prefix]
```

3. Association testing (covariate mode): 
```
magma \
--gene-results [input file name].genes.raw \
--gene-covar [input file name].covar.tsv \
--out [output file prefix]
```
