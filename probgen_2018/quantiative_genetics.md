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
* **TL;DR** - we can maybe improve on LDScore but it's complicated


### Jean Morrison, UChicago, *Accounting for confounding in Mendelian randomization using genome wide summary statistics*
* causal inference in observational studies: mediator -> outcome
  - but confounders make inference harder to measure in observational studies
* instrument - third trait not associated with the confounders that affect the mediator
* proposal- genetic variants are good instruments, fixed at birth, not affected by reverse causality
* Mendelian randomization: variants as instruments
  - association between variant and mediator
  - association between variant and outcome that is not zero
  - can be more than one variant - becomes a regression problem
* assumptions for valid inference: variant casually affects mediator, variant does not affect confounders, variant not affecting outcome through other pathways
* potential sources of confounding - shared biological pathways, gene co-regulation, variants with multiple functions (pleitropy)
* inverse weighted Mendelian randomization, the null hypothesis is no correlation between genetics effects
* new null - CAUSE Model - use unobserved confounder to create a competitive null model
* **TL;DR** - we can include genetic variants as an instrument to help control confounding in causality studies


### Barbara Engelhart, Princeton, *Experimental design and single cell RNA-sequencing*
* motivation- statistics to design experiments
  - experiments are costly, need to maximize resources
* Contextual Multi-arm bandits - context, captures info about arms or experiments.
  - when reward is binary, can model this as logistic regression
  - update regression coefficients after each experiment
* how do you select an arm to pull given context and goal?
* Thompson sampling
  - MCMC (Gibbs sampling) - sample the best arm at each iteration from the full posterior of logistic regression
  - laplace approximation, select the MAP using laplace approx of posterior distribution of the logistic regression
* Upper confidence bounds - choose perturbed optimal arm according to confidence bounds on expected rewards -- choose arm with rewards that is as large as plausibly possible
  - doesn't perform as well as thompson sampling in reality
* Logistic bandits to experimental RNA-seq -- in cell atlases need to coordinate across species, cells, tissues etc
  - need to optimize diversity within budget
  - arms- scenarios of interest
  - context- cells characterized by gene expression vectors mapping to tissue labels
  - reward- cell type diversity
* Use GT estimator to estimate diversity
* incidence case versus delayed abundance case
* **TL;DR** using multi-arm bandit type logic for designing experiments can maximize diversity and minimize cost


### Ruthie Johnson, UCLA, *A scalable Bayesian model for estimating the genetic architecture of complex traits using summary statistics from GWAS*
* complex traits have genetic and environmental component
* GWAS traits are polygenic, need to estimate proportion of SNPs that contribute
* what proportion of SNPs contribute to a trait from summary traits? (causal == non-zero effect size)
* the genetic component of a trait can be described by a generative model
* with LD, introduce correlations between observed effect sizes of SNPs
* observed effect sizes of each SNP are not independent
* use gibbs sampler to get prior (O(M^3))
* sparsity of complex traits improves computation
  - precompute LD
  - only loop over causal snps (O(KM))
* **TL;DR** we can leverage sparsity to help improve computation to estimate proportion of casual snps


### Andy Clark, Cornell, *The Elston-Stewart algorithm meets wild pedigreed populations*
* questions addressed by pedigrees - linkage of markers and traits,  rich modeling of drift, transmission of IBD blacks, components of selection
* elston-stewart algorithm - express likelihood of pedigree data given 3 things - probability of founders, transmission rules, penetrance
  - assumes hardy-weinberg, binomial sampling, offspring are independent, nuclear families are independent
* applications of elston-stewart
  - transmission distortion
  - sexual antagonism/sexual conflict
  - impact of non-transmitted allele
* elston-stewart algorithm provdes flexible way to construct LR tests on pedigres  
