# Probabilistic Modeling in Genomics 2018

## Population Genomics I: Mutation, recombination and demography inference

### Kelly Harris, University of Washington, *Using archaic introgression to probe enhancer function and evolution*
* neanderthal DNA intro-gressed into non-africans and purged unevenly from the genome (i.e. none in important genes)
* Hypotheses explaining selection against neanderthal DNA - 1) Dobzhansky-Muller incompatibilities (Sankararaman et al 2014), 2) weakly deleterious mutation load (Harris and Nielsen 2016)  
* Can neanderthal DNA help us infer how much of the genome is functional?
* Many neanderthal alleles have deleterious cis-regulatory effects (Mccoy et al 2017)
* Neanderthal DNA depleted in brain regions
* **TL;DR** - increased depletion of archaic alleles in enhancer regions


### Brian Browning, University of Washington, *Efficient probabilistic modeling of large-scale sequence data*
* genotype imputation - SNP array data into sequence data
* use forward-backward algorithm to compute the probability a target haplotype is a particular allele
* Howie, Donnelly and Marchini 2009 - impute in small windows using subset of reference haplotypes w/ highest allele sharing to target haplotype in the window
* A composite reference haplotype is a mosaic of reference haplotype segments
* **TL;DR** - using composite reference decreases time of imputation but no loss to accuracy


### Illan Gronau, The Herzliya Interdisciplinary Center, *Bayesian Model Comparison of Population Histories*
* Uncertainty in parameters and population tree structure in population history inference
* Rank different models of population history by using the uncertainty in the parameter values that can approximate the  posterior probability
* -- Can we use the approximate posterior samples to assess likelihood?
* **TL;DR** Relative Bayes Factors provide a general and flexible framework for Bayesian model comparison


### Sriram Sankararaman, UCLA, *A statistical model for reference free archaic local ancestry inference*
* Deep population structure in Africa a mystery, lack of ancient DNA
* Archaic introgression explorer - combine multiple summary statistics computed from present-day genomes to estimate "archaic local ancestry"
* Goal- for each SNP in each individual, estimate probability of archaic ?
* Use haplotype-level summary statistics
* Yoruba population estimate average archaic fraction ~8% (but not neanderthal or pygmy)
* site frequency spectrum- in SNP x Individuals  0/1 matrix, the number of 1's for each SNP
* Conditional site frequency spectrum- Restrict to all the sites that are 1 in Neanderthal, create spectrum of Africans at those SNPs
* Yoruba population model seems to be a more complicated model of population demography, including non-random mating
* **TL;DR** boosts power by combining weakly informative summary stats from present day genomes, reference free inference of archaic local ancestry; evidence for introgression in Yoruba from a divergent population


### Kelsey Johnson, Penn, *A method to identify recurrent mutations from unphased population-level sequencing data*
* recurrent mutation - derive from same mutation events occurring independently
* Recurrent mutations are hallmarks of Mendelian diseases and some complex, like autism
* Usually done in family based studies, but what about population? How to determine whether it is recurrent or IBD?
* recombination distances follow a predictable pattern
* Recurrent mutation as a function of substitution probability
* **TL;DR** uses a simple model for trying to decide if mutation is recurrent or IBD using population level sequencing data


### Leo Speidel, Oxford, *Reconstructing the genealogies of humans and wild mice*
* Given present day sequence data, can we reconstruct the genealogy? And how can we use the genealogies for inference
* Traditional genealogy estimate based on coalescent with recombination, only scale to tens of samples
* Use Li-and-Stephens model to locally estimate genealogy
* Can estimate population size, mutation rate, evidence for selection
* New statistic that captures to what extent a lineage out-competed other lineages 
* **TL;DR** sequencing data --> genealogy, can use this to do cool stuff
