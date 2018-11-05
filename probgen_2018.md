# Probabilistic Modeling in Genomics 2018

## Population Genomics

### Kelly Harris, University of Washington, *Using archaic introgression to probe enhancer function and evolution*
* neanderthal DNA intro-gressed into non-africans and purged unevenly from the genome (i.e. none in important genes)
* Hypotheses explaining selection against neanderthal DNA - 1) Dobzhansky-Muller incompatibilities (Sankararaman et al 2014), 2) weakly deleterious mutation load (Harris and Nielsen 2016)  
* Can neanderthal DNA help us infer how much of the genome is functional?
* Many neanderthal alleles have deleterious cis-regulatory effects (Mccoy et al 2017)
* Neanderthal DNA depleted in brain regions
* TL;DR - increased depletion of archaic alleles in enhancer regions

### Brian Browning, University of Washington, *Efficient probabilistic modeling of large-scale sequence data*
* genotype imputation - SNP array data into sequence data
* use forward-backward algorithm to compute the probability a target haplotype is a particular allele
* Howie, Donnelly and Marchini 2009 - impute in small windows using subset of reference haplotypes w/ highest allele sharing to target haplotype in the window
* A composite reference haplotype is a mosaic of reference haplotype segments
* TL;DR - using composite reference decreases time of imputation but no loss to accuracy

### Illan Gronau, The Herzliya Interdisciplinary Center, *Bayesian Model Comparison of Population Histories*
* Uncertainty in parameters and population tree structure in population history inference
* Rank different models of population history by using the uncertainty in the parameter values that can approximate the  posterior probability
* -- Can we use the approximate posterior samples to assess likelihood?
* TL;DR Relative Bayes Factors provide a general and flexible framework for Bayesian model comparison
