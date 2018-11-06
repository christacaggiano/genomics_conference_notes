# Quantitative Genetics and Association Mapping

### David Balding, University of Melbourne, *Improved models for the genetic basis of complex human traits using association statistics*
* the heritability tagged by a SNP increased linearly with its LD
* LD score regression - Uses only GWAS summary statistics - not individual genotype data
  - critique - implicitly assumes every SNP contributes equally
  - expected heritability of each SNP varies with properties know a priori
* Problem with Genome wide models for GWAS data - number of SNPS is much greater than the number of individuals, so without further assumptions we can't estimates effect sizes (overfitting)
  - GCTA - use gaussian  shrinkage function (many weights go to zero), computationally convenient
  - alternative idea - construct better priors from external information (previous GWASes)
* assumes effect size ~ N(0, w*sigma^2)
* add MAF for 1 parameter, allows for phenotype-specific selection effects
* LD model downweights common/well-genotypes SNPs and upweights rare and poorly genotypes SNPs
* hybrid model - data choose between GCTA/LDSC and LDAK/SumHer models, claim their model explains real data better
* over-adjustment for confounding?
* SumhHer model vs LDSC - well correlated but SumHer estimates that heritability is more evenly spread


### Jean Morrison, UChicago, *Accounting for confounding in Mendelian randomization using genome wide summary statistics*
* causal inference in observational studies: mediator -> outcome
  - but confounders make inference harder to measure in observational studies
* instrument - third trait not associated with the confounders that affect the mediatoroo
* proposal- genetic variants are good instruments, fixed at birth, not affected by reverse causality
* Mendelian randomization: variants as instruments
  - association between variant and mediator
  - association between variant and outcome that is not zero
  - can be more than one variant - becomes a regression problem
* assumptions for valid inference: variant casually affects mediator, variant does not affect confounders, variant not affecting outcome through other pathways
* potential sources of confounding - shared biological pathways, gene co-regulation, variants with multiple functions (pleitropy)
* inverse weighted Mendelian randomization, the null hypothesis is no correlation between genetics effects
* new null - CAUSE Model - use unobserved confounder to create a competitive null model 
