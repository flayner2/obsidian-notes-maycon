# Experiments
- Compare the mTOR $CpG_{O/E}$ values of *A. mellifera* and ants (or an ant);
	- Are those genes significantly more methylated in the bee?
- Compare ants with solitary bees (and/or sawflies or solitary wasps);
- Compare *A. rosae* with another solitary species (bee, wasp or sawfly, or one of each), maybe trying to look for one with a similar $CpG_{O/E}$ distribution.

# Interesting discussion points
- *D. melanogaster* has a left-shifted median $CpG_{O/E}$ value (with $m \approx 0.87$);
- Two solitary wasps, *F. arisanus* and *D. alloeum* have low median $CpG_{O/E}$ values ($m \le 0.79$);
	- They are both from the family Braconidae, subfamily Opiinae;
		- They are bot parasites and apparently with specific hosts from the fruit fly family Tephritidae;
	- There's one other Braconidae in this set, *M. demolitor*, not from the same subfamily, and whose median $CpG_{O/E}$ value is $\approx 0.95$;
		- This species is also a parasite, but seems to target specifically species from the order Lepidoptera;
	- All of the above facts could account for the lower median $CpG_{O/E}$ in *F. arisanus* and *D. alloeum* being due to a common evolutionary origin (a phylogenetic signal, and not an evidence of common function);
- Even though the median $CpG_{O/E}$ in *C. cinctus* is lower than in *A. cephalotes*, the mTOR pathway genes are enriched among the overmethylated genes in the ant compared with the sawlfy (comparing the $log_2$ difference of $CpG_{O/E}$ values between both);
- Take a look at *dsx* NP_001104725 and its domain PF08828, which is absent in social species for some reason (but appears in an old annotation file: `work/komodo_inputs/old/old_hymenoptera/komodo_input_hymenoptera_pfam/GCF_003254395`);
	- Take this gene and find the homologs in all Hymenoptera (and ants as well) and check the basic stats: alignment, conservation in solitary an eusocial, positive selection tests, etc.
	- The OG for this gene is OG0009093 and it is absent in a bunch of ants.

# Paper
## Figuras principais
1. Distribuição do CpG OR nas cinco espécies iniciais
2. Scatterplots pras comparações de CpG OR dos ortólogos entre Formiga X sawfly e Abelha x sawfly (colorindo/labelling os pontinhos da via mTOR)
3. Análise de enriquecimento dos seguintes grupos de genes: Amel over/Amel under/Aros over/Aros under
4. Análise de enriquecimento dos seguintes grupos de genes: overmethylated em Amel x Aros / overmethylated em Acep x Ccin
5. boxplots de um exemplo de gene mTOR demonstrando os valores de A) CpG OR; B) (CpG OR gene) - (CpG OR mediana); 3) CpG OR percentile (OG0006916)
6. Árvore filogenética das espécies analisadas (talvez essa seja a figura 1, na verdade)
## Figuras suplementares
1. Distribuição do CpG OR em todas as espécies
2. Boxplots dos demais genes
3. Boxplot com o percentile de todos os genes da via mTOR enriquecidos (talvez essa seja uma figura principal tb)

## TODO
- Maybe update the legend box position of Figure 2 (CpG density plots for aaacd) to be where the 6th pannel would be (below *D. melanogaster*, right to *At. rosae*);
- Generate the labeled scatter plots for *A. mellifera* x *At. rosae* and *Att. cephalotes* and *C. cinctus*;
- Generate a single figure with two pannels for the enrichment analysis in *A. mellifera* hyper and hypo (Figure 4a) and *At. rosae* hyper and hypo (Figure 4b) 
- Generate a single figure for the enrichment analysis of the overmethylated *A. mellifera* genes compared to *At. rosae* (Figure 5a) and *Att. cephalotes* compared to *C. cinctus* (Figure 5b);
- Assemble a figure containing the boxplots for the $CpG_{O/E}$, difference from median $CpG_{O/E}$ and percentile position of $CpG_{O/E}$ for the orthogroup OG0006916.