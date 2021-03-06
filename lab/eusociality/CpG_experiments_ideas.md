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
		- They both also don't possess a copy of *Dnmt1*.
	- There's one other Braconidae in this set, *M. demolitor*, not from the same subfamily, and whose median $CpG_{O/E}$ value is $\approx 0.95$;
		- This species is also a parasite, but seems to target specifically species from the order Lepidoptera;
	- All of the above facts could account for the lower median $CpG_{O/E}$ in *F. arisanus* and *D. alloeum* being due to a common evolutionary origin (a phylogenetic signal, and not an evidence of common function);
- Even though the median $CpG_{O/E}$ in *C. cinctus* is lower than in *A. cephalotes*, the mTOR pathway genes are enriched among the overmethylated genes in the ant compared with the sawlfy (comparing the $log_2$ difference of $CpG_{O/E}$ values between both);
- Take a look at *dsx* NP_001104725 and its domain PF08828, which is absent in social species for some reason (but appears in an old annotation file: `work/komodo_inputs/old/old_hymenoptera/komodo_input_hymenoptera_pfam/GCF_003254395`);
	- Take this gene and find the homologs in all Hymenoptera (and ants as well) and check the basic stats: alignment, conservation in solitary an eusocial, positive selection tests, etc.
	- The OG for this gene is OG0009093 and it is absent in a bunch of ants.

# Paper
## Figuras principais
1. Distribui????o do CpG OR nas cinco esp??cies iniciais
2. Scatterplots pras compara????es de CpG OR dos ort??logos entre Formiga X sawfly e Abelha x sawfly (colorindo/labelling os pontinhos da via mTOR)
3. An??lise de enriquecimento dos seguintes grupos de genes: Amel over/Amel under/Aros over/Aros under
4. An??lise de enriquecimento dos seguintes grupos de genes: overmethylated em Amel x Aros / overmethylated em Acep x Ccin
5. boxplots de um exemplo de gene mTOR demonstrando os valores de A) CpG OR; B) (CpG OR gene) - (CpG OR mediana); 3) CpG OR percentile (OG0006916)
6. ??rvore filogen??tica das esp??cies analisadas (talvez essa seja a figura 1, na verdade)
## Figuras suplementares
1. Distribui????o do CpG OR em todas as esp??cies
2. Boxplots dos demais genes
3. Boxplot com o percentile de todos os genes da via mTOR enriquecidos (talvez essa seja uma figura principal tb)

## TODO
- [x] Take a look at the font sizes of the figures. Maybe will have to increase them;
- [x]  Maybe update the legend box position of Figure 2 (CpG density plots for aaacd) to be where the 6th pannel would be (below *D. melanogaster*, right to *At. rosae*);
- [x] Generate the labeled scatter plots for *A. mellifera* x *At. rosae* and *Att. cephalotes* and *C. cinctus* (use `ggrepel`);
- [x] Generate a single figure with two pannels for the enrichment analysis in *A. mellifera* hyper and hypo (Figure 4a) and *At. rosae* hyper and hypo (Figure 4b) (==Chico==);
- [x] Generate a single figure for the enrichment analysis of the overmethylated *A. mellifera* genes compared to *At. rosae* (Figure 5a) and *Att. cephalotes* compared to *C. cinctus* (Figure 5b) (==Chico==);
- [x] Assemble a figure containing the boxplots for the $CpG_{O/E}$, difference from median $CpG_{O/E}$ and percentile position of $CpG_{O/E}$ for the orthogroup OG0006916;
- [x] Add a heatmap to the tree, with the z-score for $CpG_{O/E}$, diff to median and percentile position for OG0006916 and OG0003581;
- [x] Create two new sets of boxplot triplets (same as the previous one for OG0006916) for OG0003581 and OG0006916 but adding the p-values and q-values for each metric as a text label;
- [x] Add results and discussion for the ANOVA analysis, focusing on OG0006916 - NP_001259636.1 (wacky) - significant after FDR - and slightly less so on OG0003581 - NP_732114.1 (Akt1) - loses significance after FDR;
- [x] Create a tree figure without the heatmaps but with a matrix showing the state of the DNMT ezymes (also create a figure with both the heatmaps and the matrix);
- [x] Create two scatter plots to evaluate the correlation between $CpG_{O/E}$ and diff from median, and between $CpG_{O/E}$ and percentile (per gene), for the 5 studied species (with orthologs between all 5) (make a q-q plot);
- [ ] Metadata sheet;
- [ ] Table with gene ids for the tree;
- [x] Put the medians of each distribution onto the overlapped density plots;
- [ ] Organize the data and code for reproductibility;
- [x] Rewrite the paper to follow the order discussed with Chico;
- [x] ~~Make the scatterplots (*amel vs aros* and *acep vs ccin*) a single panel~~ (ignore this for now);
- [ ] Generate the BUSCO figure (maybe...).

## Parte Chico
- Webgestalt
- Overrepresentation Enrichment Analysis
- GO
- Biological process non-redundant
- refseq peptide
- drosophila genome protein-coding
- Genes com $log2fold < 0$;

## Discussion
- o ??nico grupo que passa no phylogenetic ANOVA p??s-corre????o de m??ltiplas hip??teses ?? o OG0006916 - NP_001259636.1 (wacky);
- O outro que ?? significativo, mas deixa de ser quanto fazemos o FDR ?? o OG0003581 - NP_732114.1 (Akt1)

## Refs
- [Akt1](https://www.nature.com/articles/srep18794)
- [wacky](https://pubmed.ncbi.nlm.nih.gov/26757981/)
- [Dnmt3 *A. rosae*  and *O. abietinus* (supplementary material)](https://academic.oup.com/gbe/article/12/7/1099/5842140?login=true#206041224)
- [Dnmt3 *B. impatiens* (supplementary material)](https://genomebiology.biomedcentral.com/articles/10.1186/s13059-015-0623-3)
- [Dnmt3 *A. colombica* (classified as homologous to *A. mellifera* dnmt3)](http://hymenopteramine-v15.rnet.missouri.edu/hymenopteramine/report.do?id=99315613)
- [Dnmt3 *C. floridanus* (classified as homologous to *A. mellifera* dnmt3)](http://hymenopteramine-v15.rnet.missouri.edu/hymenopteramine/report.do?id=115119741)
- [Dnmt3 *C. cinctus* (classified as homologous to *A. mellifera* dnmt3)](http://hymenopteramine-v15.rnet.missouri.edu/hymenopteramine/report.do?id=117715675)
- [Dnmt3 *C. calcarata* (classified as homologous to *A. mellifera* dnmt3)](http://hymenopteramine-v15.rnet.missouri.edu/hymenopteramine/report.do?id=120128252)
- [Dnmt3 *C. floridanum* (seems to actually exist, but is truncated and possibli non-functional)](https://ir.lib.uwo.ca/etd/4920/)
- [Dnmt3 *D. quadriceps* and *S. invicta* (seems to actually exist)](https://www.pnas.org/doi/full/10.1073/pnas.1515937112)
- [Dnmt3 *D. novaeangliae* and *E. mexicana* and *M. rotundata* (seems to actually exist)](https://www.pnas.org/doi/full/10.1073/pnas.1515937112)
- [Dnmt3 *H. saltator* (ref 1)](https://www.pnas.org/doi/full/10.1073/pnas.1515937112)and [(ref 2)](https://www.science.org/doi/abs/10.1126/science.1192428)
- [Dnmt3 *L. humile* (ref 1)](https://www.pnas.org/doi/full/10.1073/pnas.1515937112)and [(ref 2)](https://www.pnas.org/doi/full/10.1073/pnas.1008617108)
- [Dnmt1 *M. demolitor* (seems to actually exist)](https://www.mdpi.com/2075-4450/11/2/121/htm)
- [Dnmt1 and dnmt3 *P. barbatus* (seems to actually exist)](https://www.pnas.org/doi/full/10.1073/pnas.1007901108)
- [Dnmt1 and Dnmt3 *T. pretiosum*](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC5960102/)

## Pra mandar pro chico
- ~~Os 3 density plots com todo mundo;~~
- ~~As figuras de overlap (fazer um painel tbm);~~
- ~~Os scatter com todas as m??tricas;~~
- ~~As compara????es entre as m??tricas.~~

## Paper corrections
- ~~Criar o density AAACD pra diff to median, e fazer um painel junto com o do raw cpg~~.
- ~~Definir o odds ratios na intro tbm~~.
- ~~Introdu????o, falar que o processo de hipometila????o parece ser "ativo", parece existir algo que mant??m o conte??do CG (citando o bewick), falando dos problemas das diferen??as nas medianas, falando do status geral de um gene~~.
- Estudar dial??tica. 
- ~~Figura 6 talvez vire suplementar. Fazer uma figura com apenas os 14 genes com overlap~~.
- Comentar que a gente "ajudou" o raw odds (na intro).
- Dar uma melhorada no t??tulo (Accounting for genomewise methylation levels reveals)
- Citar isso mais na frente no paper: "Interestingly, those two species also possess some of the lowest median values of $CpG_{O/E}$ (0.7729 and 0.7984).", falando sobre as Opiinae que n??o possuem Dnmt1