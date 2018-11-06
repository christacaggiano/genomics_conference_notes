# Systems Biology

### David McCandish, Cold Spring Harbor, *Modeling higher-order genetic interactions*
* use minimum epistasis interpolation to model higher order genetic interactions


### Anna Green, Harvard, *Computational inference of protein-protein interactions with residue-level resolution at a genome-wide scale*
* use evolutionary sequence record to infer protein interaction
* interaction of proteins impose constraints on amino acids
* made dataset of true protein-protein interactions, crystal structures, and use this data to predict interactions


### Sam Smith, Brown, *Hierarchical clustering reveals differential genetic architecture between immunological and metabolic phenotypes*
* how do we put causal SNPs into disease relevant pathways?
* past studies test for shared genetic architecture at the variant level
    - testing for colocalization at gene-level
* can cluster gene score matrix, define statistic to examine clusters
* analyze 26 chronic illness phenotypes whose architecture had been previously studied
* use ward Hierarchical clustering
* Significant clusters - clusters that come together by ward clustering and stay together, use branch length of cluster to sort clusters
* clusters that are significant
    - >median branch length
    - branch length gap is > than 2 scaled absolutes deviations from branch length medians
