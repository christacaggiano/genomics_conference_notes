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
*


## Smita Krishnaswamy, Yale, *Manifold learning yields insight into cellular state space under complex experimental conditions*
* scRNA-seq is very heterogeneous, high dimensional
* Use unsupervised methods to understand patterns in data 
