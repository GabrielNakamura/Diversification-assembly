# Diversification-assembly
Function to compute diversification ([Jetz et al 2012](https://www.nature.com/articles/nature11631) and [Freckleton et al 2008](https://www.journals.uchicago.edu/doi/10.1086/588076)) and Phylogenetic Diversity (PD) metrics combined with ancestral area reconstruction (with [BioGeoBEARS](https://github.com/nmatzke/BioGeoBEARS))

# Details
diversification-assembly function combine diversification and PD metrics with ancestral area reconstruction to derive estimatives of diversification and PD that occur locally through time (diversificaiton and PD inside the biome in which species are actually present).

# arguments
### inputs:

W = composition matrix, in lines the sample units and species in columns;

tree = phylogenetic tree from class phylo;

ancestral.area = data.frame object; lines with node names from tree and one column containing the ancestral area of each node;

biogeo = data.frame. Lines with names of sample units, must be the same names that in W and one column containing the Ecoregion (biome) that each sample unit belongs;

### output:

Ecoregion.per.node = a matrix object; lines containig the nodes and the colums the species. Each cell present the Ecorregion that each ancestor of the species i was found;

Diversification.Assembly_Jetz = numeric. Biome Diversification values calculated according to a modifyied version of Jetz's metric of diversification to account only for local diversification;

Diversification.Assembly_Freck =  numeric. Biome Diversification values calculated according to a modifyied version of Freckleton's metric of diversification to account only for local diversification;

Diversification_total = matrix. Diversification values calculate for species according to Jetz and Freckleton metrics.

PD_local = PD metric calculated as the proportion of PD inside the biome;

PD_total = original PD metric;

age_arrival = age of arrival of the most ancient ancestor in the biome that the actual species occupy.
