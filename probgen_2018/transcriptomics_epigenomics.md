# Transcriptomics and Epigenomics

### Michael Hoffman, University of Toronto, *Segway and the Graphical Models Toolkit—A framework for probabilistic genomic inference*
* semi-automated genome annotation - genomic signal --> pattern discovery --> annotation, visualization, interpretation
* graphical models toolkit- general purpose toolkit for probabilistic inference in temporal signals - can express arbitrary structure dynamic graphical models
* Segway software uses dynamic bayesian network for genome segmentation
* Uses EM training to find parameters, then annotates based on those parameters
* **TL;DR** you can use GMTK to build lots of cool models to learn about epigenetic marks on DNA


### Ziyue Gao, Stanford *Overlooked roles of DNA damage and maternal age in generating human germline mutations*
* study of human germline mutations by indirect approaches- incidence of mendelian disease, phylogenetic comparison
* Point mutation rate - 10^-8 per basepair per generation
* higher mutation rate in males than in females (male mutation bias)
* mutation rate increases with father's age (paternal age effect)
* differences could be from sex difference in germ cell development - males have 23 divisions/year through life
* direct sequencing of parent-offspring trio enables direct survey of de novo germline mutations
* Replication errors are not the only source of spontaneous mutations
* male-to-female mutation ratio is stable with parental age
* Use a likelihood model to infer the parental age effects on mutation rate
* Different mutation classes show distinct trends of male bias
* Genomic distribution of paternal CpG > TpG mutations is associated with methylation levels in testis
* Can accumulation of DNA damage explain increase in maternal mutations?
* **TL;DR** there are differing male/female mutation rates, largely attributed to differences in spermatogenesis, oovogenesis 


### Smita Krishnaswamy, Yale, *Manifold learning yields insight into cellular state space under complex experimental conditions*
* scRNA-seq is very heterogeneous, high dimensional
* Use unsupervised methods to understand patterns in data
* Challenges w/ scRNA-seq - sparsity, noise, non-linearity, scale
* Data seems high dimensional because of ambient measurements, there are many genes but high degree of redundancy. However, because of cell types/states are constrained by biology, can use this to learn shapes
* Shape can be learned by non-linear dimensionality reduction, included graph signal processing or deep learning
* Differentiation and state change occurs in smooth gradual steps
* Creating a data graph- walk via small local steps in teh data and compute probability of reaching every node
* Random walk = diffusion
* PHATE visualization- keeps local and global structure
* **TL;DR** - use manifold learning techniques to better visualize complex scRNA-seq data


### Danila Bredikhin, EMBL, *Multi-group factor decomposition of single-cell transcriptome profiles*
* Approaches to analyze single-cell RNA sequencing data: clustering, trajectories, factor decomposition
* Modeling considerations - group structure, factors interpretability, scalability
* Multi-group factor analysis (MuGFA) model
* automatic relevance determination, group relevance priors on factors group
* sparsity priors on cells
* **TL;DR** use fancy models to analyze scRNA-seq


### Harold Pimental, Stanford *Fast intron retention quantitative trait loci discovery*
* intron retention - a mode of alternative splicing
* sporadic intron retention events have been observed in neurons, granulocytes and cancers
* Average human intron is long
* Intron retention - nonsense mediated decay
* Intron retention regulates gene expression in granulocytes
* A large fraction of genes contain retained introns
* in typical RNA-seq analysis we ignore reads that map out of transcript annotations
* gene expression covaries with genotype
* irQTL and eQTL effects are mildly anti-correlated
* irQTL and sQTL are midly correlated
* irSNPs are centered in their corresponding genes, and many fall near corresponding introns, very close to junctions
* **TL;DR** - used rna-seq alignment software to find intron retention qtls and observed some genetic effects
