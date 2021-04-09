# Mesure Biovolumes
## Campagne Mars 2021
### Navicula
#### Comparaison Longueur 
Utilisation d'un test de Kruskal-Wallis (source code : [Datanovia](https://www.datanovia.com/en/fr/lessons/test-de-kruskal-wallis-dans-r/)

'''
> LongNavi <- read.xlsx('/Users/fredericwolf/Desktop/Stage 2021/Mesures/Campagne mars 2021/stats_biovolumes.xlsx', 1, header=TRUE, colClasses=NA)
> ggboxplot(LongNavi, x = "Source", y = "Longueur")
> LongNavi <- LongNavi %>%
+ reorder_levels(Source, order = c("Ours", "Estreys", "Bard"))
> LongNavi %>%
+ group_by(Source) %>%
+ get_summary_stats(Longueur, type = "common")
> res.kruskal <- LongNavi %>% kruskal_test(Longueur~Source)
> res.kruskal
'''

Résultat : p = 0.00000000205
-> Il y a donc une différence significative de longueur entre des sources

Utilisation d'un test de Wilcoxon pour voir quelles sources sont différentes 
'''
> pwc <- LongNavi %>%
+ wilcox_test(Longueur~Source, p.adjust.method = "bonferroni")
> pwc
'''

Résultats :
Ours - Estreys : p = 0.000000254
Ours - Bard : p = 0.00000001
Estreys - Bard : p = 0.634

-> Il y a donc une différence significative entre Ours et les deux autres sources. Les diatomées Navicula de la source Ours sont plus petites que dans les autres sources en termes de longueur. 

#### Comparaison Largeur
Utilisation d'un test de Kruskal-Wallis (source code : [Datanovia](https://www.datanovia.com/en/fr/lessons/test-de-kruskal-wallis-dans-r/)

'''
> LargNavi <- read.xlsx('/Users/fredericwolf/Desktop/Stage 2021/Mesures/Campagne mars 2021/stats_biovolumes.xlsx', 2, header=TRUE, colClasses=NA)
> ggboxplot(LargNavi, x = "Source", y = "Largeur")
> LargNavi <- LargNavi %>%
+ reorder_levels(Source, order = c("Ours", "Estreys", "Bard"))
> LargNavi %>%
+ group_by(Source) %>%
+ get_summary_stats(Largeur, type = "common")
> res.kruskal <- LargNavi %>% kruskal_test(Largeur~Source)
> res.kruskal
'''

Résultat : p = 0.0000000087
-> Il y a donc une différence significative de largeur entre des sources

Utilisation d'un test de Wilcoxon pour voir quelles sources sont différentes 
'''
> pwc <- LongNavi %>%
+ wilcox_test(Longueur~Source, p.adjust.method = "bonferroni")
> pwc
'''

Résultats :
Ours - Estreys : p = 0.0000000106
Ours - Bard : p = 0.002
Estreys - Bard : p = 0.00021

-> Il y a donc des différences significatives entre toutes les sources. La plus petite largeur de Navicula se retrouve dans la source Ours. La largeur moyenne est à Bard et la plus grande est aux Estreys. 
