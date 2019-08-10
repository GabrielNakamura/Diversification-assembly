# Diversification-assembly
Function to compute diversification ([Jetz et al 2012](https://www.nature.com/articles/nature11631) and [Freckleton et al 2008](https://www.journals.uchicago.edu/doi/10.1086/588076)) and Phylogenetic Diversity (PD) metrics combined with analysis of ancestral area reconstruction (with [BioGeoBEARS](https://github.com/nmatzke/BioGeoBEARS))

# Details
diversification-assembly function combines diversification and PD metrics with ancestral area reconstruction to obtain estimatives of diversification and Phylogenetic diversity that emerge locally through evoluionary time by mapping the occurence of ancestral of present day species (diversification and PD inside the biome in which species are actually present).

# arguments
### inputs:

W = composition matrix, in lines the sample units and species in columns;

tree = phylogenetic tree from class phylo;

ancestral.area = data.frame object; lines with node names of the tree and one column containing the ancestral area of each node;

biogeo = data.frame. Lines with names of sample units, must be the same names that in **W** and one column containing the Ecoregion (biome) that each sample unit belongs;

### output:

Ecoregion.per.node = a matrix object. lines containig the nodes and the colums the species. Each cell present the Ecorregion that each ancestral of species i was found;

Diversification.Assembly_Jetz = numeric. Biome Diversification values calculated according to a modifyied version of Jetz's metric of diversification;

JetzTotalComm_mean = numeric. A vector containing mean values of total diversification calculated as harmonic mean of Jetz diversification for each row of matrix W;

JetzLocalComm_mean = numeric. A vector containing mean values of local diversification calculated as the portion of harmonic mean of total Jetz diversification for each row of matrix W;

JetzLocalSpp_mean = numeric. A vector containing mean values of local species diversification calculated as the portion total diverfication of each species;

Diversification.Assembly_Freck =  numeric. Biome Diversification values calculated according to a modifyied version of Freckleton's metric of diversification;

Diversification_total = matrix. Diversification values calculate for species according to Jetz and Freckleton metrics.
