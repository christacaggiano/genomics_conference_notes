# Microbiome, Cancer, and Beyond

### Emily Davenport, Cornell, *Simultaneously modeling host genetics and microbiome composition reveals the heritability and the proportion of variance explained due to the microbiome of immune-related traits*
* Composition of of microbiome determined by method of birth, diet, antibiotics, some genetics
* For complex traits imn humans - how much inter-individual variability is explained by genetics vs the microbiome?
* If we include microbiome as a covariate in GWAS can we improve our power to identify genetic associations with a trait?  
* normal GWAS linear mixed model: phenotype=[covariates]+relatedness
* extend GWAS linear mixed model to microbiome: phenotype=[covariates]+relatedness+microbiome relatedness(beta diversity)
* microbiome explains some (~25%) of variance
* traits with a large amount of variance explained by microbiome also increase power in GWAS of these traits
* **TL;DR**- you would think microbiome data would be a GWAS slam dunk, but it's not


### Tommi Maklin, University of Helsinki, *Accurate bacterial genome assembly from multi-strain enrichment cultures*
* steps strain identification - sweep & sequence, pseudoalign reads w/ kallisto, estimate proportions, then genome assembly
* pseudo-alignment grouped by clonal complex or sequence type
* model consists of pseudoalignment vectors,   latent cluster indicators, mixing proportions
* prior- dirichlet, posterior- collapsed variation bayes
* **TL;DR** - assembling genomes would be helpful for antibiotic resistance, read binning based probabilities can help this problem


### Anastasia Teterina, University of Oregon, *Mode of reproduction drives the distribution of polymorphism across the genome—Theory and empirical tests in Caenorhabditis nematodes*
* genetic variability affected by genome structure and population structure, including differences in mating types
  - mating types affects population size, recombination freq
* effect of recombination of variation?
  - dna polymorphism correlates with recombination rates


### Quaid Morris, University of Toronto, *Pair-tree: Reconstructing cancer phylogenies using pairwise correlations*
* cancer evolution makes nearly perfect phylogenies
* infinite sites assumption- each single nucleotide variant only occurs once during evolution and never reverts
* clonal mutations are present in all cancer cells - occur somewhere between fertilized egg and most recent common ancestors
* collinear mutations- one mutation is a descendent of another mutation type
* branched mutation- mutually exclusive set of mutations
* each collinear mutation represents a subclonal lineage aka subclone
* perfect phylogenies only made of branched/collinear mutations
* reconstructing perfect phylogenies requires only pairwise relationships, can solve in linear time
* not really perfect though... many cancers are highly aneuploid, mostly use population sequencing
* generative modeling solution - phyloWGS
* sum rule identifies some collinear pairs - if frequencies of two mutations is > 100%  cannot be branching
* two mutations cannot be collinear because neither's cells can be the subset of the other's
* four gamete rule - if not branching or collinear, cannot be perfect phylogeny
* pairwise rules highly constrain phylogenies
* **TL;DR** making cancer phylogenies is harder than you'd expect, there are simple rules to make clever programs to make it easier though

### Heather Gibling, Ontario Institute for Cancer Research
* PRDM9 impacts pan-cancer genomic landscape
* use k-mer count profiles to call alleles
* k-mer count profile similarity measured using the probability mass function of a Poisson distribution
* eventually going to use paired end allele calling and genotyping
* **TL;DR** ? idk
