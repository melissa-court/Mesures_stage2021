# Mesure Biovolumes
## Campagne Mars 2021
### Navicula
#### Comparaison Longueur 
Utilisation d'un test de Kruskal-Wallis (source code : [Datanovia](https://www.datanovia.com/en/fr/lessons/test-de-kruskal-wallis-dans-r/))

> LongNavi <- read.xlsx('/Users/fredericwolf/Desktop/Stage 2021/Mesures/Campagne mars 2021/stats_biovolumes.xlsx', 1, header=TRUE, colClasses=NA)
> ggboxplot(LongNavi, x = "Source", y = "Longueur")
> LongNavi <- LongNavi %>%
> + reorder_levels(Source, order = c("Ours", "Estreys", "Bard"))
> LongNavi %>%
> + group_by(Source) %>%
> + get_summary_stats(Longueur, type = "common")
> res.kruskal <- LongNavi %>% kruskal_test(Longueur~Source)
> res.kruskal

Résultat : p = 0.00000000205
![Resultats Kruskal LongNavi](https://zupimages.net/up/21/15/r5tg.png)

-> Il y a donc une différence significative de longueur entre des sources

Utilisation d'un test de Wilcoxon pour voir quelles sources sont différentes 

> pwc <- LongNavi %>%
> + wilcox_test(Longueur~Source, p.adjust.method = "bonferroni")
> pwc

Résultats :
Ours - Estreys : p = 0.000000254
Ours - Bard : p = 0.00000001
Estreys - Bard : p = 0.634
![Resultats Wilcox LongNavi](https://zupimages.net/up/21/15/uf8l.png)

-> Il y a donc une différence significative entre Ours et les deux autres sources. Les diatomées Navicula de la source Ours sont plus petites que dans les autres sources en termes de longueur. 

#### Comparaison Largeur
Utilisation d'un test de Kruskal-Wallis (source code : [Datanovia](https://www.datanovia.com/en/fr/lessons/test-de-kruskal-wallis-dans-r/))

> LargNavi <- read.xlsx('/Users/fredericwolf/Desktop/Stage 2021/Mesures/Campagne mars 2021/stats_biovolumes.xlsx', 2, header=TRUE, colClasses=NA)
> ggboxplot(LargNavi, x = "Source", y = "Largeur")
> LargNavi <- LargNavi %>%
> + reorder_levels(Source, order = c("Ours", "Estreys", "Bard"))
> LargNavi %>%
> + group_by(Source) %>%
> + get_summary_stats(Largeur, type = "common")
> res.kruskal <- LargNavi %>% kruskal_test(Largeur~Source)
> res.kruskal

Résultat : p = 0.0000000087
![Resultats Kruskal LargNavi](https://zupimages.net/up/21/15/uf8l.png)

-> Il y a donc une différence significative de largeur entre des sources

Utilisation d'un test de Wilcoxon pour voir quelles sources sont différentes 

> pwc <- LargNavi %>%
> + wilcox_test(Largeur~Source, p.adjust.method = "bonferroni")
> pwc

Résultats :
Ours - Estreys : p = 0.0000000106
Ours - Bard : p = 0.002
Estreys - Bard : p = 0.00021
![Resultats Wilcox LargNavi](https://zupimages.net/up/21/15/dtew.png)

-> Il y a donc des différences significatives entre toutes les sources. La plus petite largeur de Navicula se retrouve dans la source Ours. La largeur moyenne est à Bard et la plus grande est aux Estreys. 

#### Comparaison Profondeur
Utilisation d'un test de Kruskal-Wallis (source code : [Datanovia](https://www.datanovia.com/en/fr/lessons/test-de-kruskal-wallis-dans-r/))

> ProfNavi <- read.xlsx('/Users/fredericwolf/Desktop/Stage 2021/Mesures/Campagne mars 2021/stats_biovolumes.xlsx', 3, header=TRUE, colClasses=NA)
> ggboxplot(ProfNavi, x = "Source", y = "Profondeur")
> ProfNavi <- ProfNavi %>%
> + reorder_levels(Source, order = c("Ours", "Estreys", "Bard"))
> ProfNavi %>%
> + group_by(Source) %>%
> + get_summary_stats(Profondeur, type = "common")
> res.kruskal <- ProfNavi %>% kruskal_test(Profondeur~Source)
> res.kruskal

Résultat : p = 0.000124
![Resultats Kruskal LargNavi](https://zupimages.net/up/21/15/puw0.png)

-> Il y a donc une différence significative de profondeur entre des sources

Utilisation d'un test de Wilcoxon pour voir quelles sources sont différentes 

> pwc <- ProfNavi %>%
> + wilcox_test(Profondeur~Source, p.adjust.method = "bonferroni")
> pwc

Résultats :
Ours - Estreys : p = 0.002
Ours - Bard : p = 0.274
Estreys - Bard : p = 0.0000279
![Resultats Wilcox LargNavi](https://zupimages.net/up/21/15/3dt1.png)

-> Il y a donc une différence significative entre Estreys et les deux autres sources. Les diatomées Navicula de la source des Estreys sont moins profondes que dans les autres sources en termes de profondeur. 

### Crenotia
#### Comparaison Longueur 
Utilisation d'un test de Kruskal-Wallis (source code : [Datanovia](https://www.datanovia.com/en/fr/lessons/test-de-kruskal-wallis-dans-r/))

> LongCreno <- read.xlsx('/Users/fredericwolf/Desktop/Stage 2021/Mesures/Campagne mars 2021/stats_biovolumes.xlsx', 4, header=TRUE, colClasses=NA)
> ggboxplot(LongCreno, x = "Source", y = "Longueur")
> LongCreno <- LongCreno %>%
> + reorder_levels(Source, order = c("Ours", "Estreys", "Bard"))
> LongCreno %>%
> + group_by(Source) %>%
> + get_summary_stats(Longueur, type = "common")
> res.kruskal <- LongCreno %>% kruskal_test(Longueur~Source)
> res.kruskal

Résultat : p = 0.00266
![Resultats Kruskal LongCreno](https://zupimages.net/up/21/15/p6jm.png)

-> Il y a donc une différence significative de longueur entre des sources

Utilisation d'un test de Wilcoxon pour voir quelles sources sont différentes 

> pwc <- LongCreno %>%
> + wilcox_test(Longueur~Source, p.adjust.method = "bonferroni")
> pwc

Résultats :
Ours - Estreys : p = 0.002
Ours - Bard : p = 0.02
Estreys - Bard : p = 0.072
![Resultats Wilcox LongCreno](https://zupimages.net/up/21/15/h1mk.png)

-> Il y a donc une différence significative (_ça dépend si on met la limite à 0,05 ou 0,01_) entre Ours et les deux autres sources. Les diatomées Crenotia de la source Ours sont plus petites que dans les autres sources en termes de longueur. 

#### Comparaison Largeur
Utilisation d'un test de Kruskal-Wallis (source code : [Datanovia](https://www.datanovia.com/en/fr/lessons/test-de-kruskal-wallis-dans-r/))

> LargCreno <- read.xlsx('/Users/fredericwolf/Desktop/Stage 2021/Mesures/Campagne mars 2021/stats_biovolumes.xlsx', 5, header=TRUE, colClasses=NA)
> ggboxplot(LargCreno, x = "Source", y = "Largeur")
> LargCreno <- LargCreno %>%
> + reorder_levels(Source, order = c("Ours", "Estreys", "Bard"))
> LargCreno %>%
> + group_by(Source) %>%
> + get_summary_stats(Largeur, type = "common")
> res.kruskal <- LargCreno %>% kruskal_test(Largeur~Source)
> res.kruskal

Résultat : p = 0.00000148
![Resultats Kruskal LargCreno](https://zupimages.net/up/21/15/vbp7.png)

-> Il y a donc une différence significative de largeur entre des sources

Utilisation d'un test de Wilcoxon pour voir quelles sources sont différentes 

> pwc <- LargCreno %>%
> + wilcox_test(Largeur~Source, p.adjust.method = "bonferroni")
> pwc

Résultats :
Ours - Estreys : p = 0.000143
Ours - Bard : p = 0.752 
Estreys - Bard : p = 0.000000353
![Resultats Wilcox LargCreno](https://zupimages.net/up/21/15/hfna.png)

-> Il y a donc une différence significative entre les Estreys et les deux autres sources. Les Estreys présentent la plus grande largeur de diatomées. 

#### Comparaison Profondeur
Utilisation d'un test de Kruskal-Wallis (source code : [Datanovia](https://www.datanovia.com/en/fr/lessons/test-de-kruskal-wallis-dans-r/))

> ProfCreno <- read.xlsx('/Users/fredericwolf/Desktop/Stage 2021/Mesures/Campagne mars 2021/stats_biovolumes.xlsx', 6, header=TRUE, colClasses=NA)
> ggboxplot(ProfCreno, x = "Source", y = "Profondeur")
> ProfCreno <- ProfCreno %>%
> + reorder_levels(Source, order = c("Ours", "Estreys", "Bard"))
> ProfCreno %>%
> + group_by(Source) %>%
> + get_summary_stats(Profondeur, type = "common")
> res.kruskal <- ProfCreno %>% kruskal_test(Profondeur~Source)
> res.kruskal

Résultat : p = 0.000124
![Resultats Kruskal ProfCreno](https://zupimages.net/up/21/15/dcph.png)

-> Il n'y a pas de différence significative entre les sources

### Planothidium
#### Comparaison Longueur 
Utilisation d'un test de Kruskal-Wallis (source code : [Datanovia](https://www.datanovia.com/en/fr/lessons/test-de-kruskal-wallis-dans-r/))

> LongPlano <- read.xlsx('/Users/fredericwolf/Desktop/Stage 2021/Mesures/Campagne mars 2021/stats_biovolumes.xlsx', 7, header=TRUE, colClasses=NA)
> ggboxplot(LongPlano, x = "Source", y = "Longueur")
> LongPlano <- LongPlano %>%
> + reorder_levels(Source, order = c("Ours", "Estreys", "Bard"))
> LongPlano %>%
> + group_by(Source) %>%
> + get_summary_stats(Longueur, type = "common")
> res.kruskal <- LongPlano %>% kruskal_test(Longueur~Source)
> res.kruskal

Résultat : p = 0.00000000430
![Resultats Kruskal LongPlano](https://zupimages.net/up/21/15/d2ma.png)

-> Il y a donc une différence significative de longueur entre des sources

Utilisation d'un test de Wilcoxon pour voir quelles sources sont différentes 

> pwc <- LongPlano %>%
> + wilcox_test(Longueur~Source, p.adjust.method = "bonferroni")
> pwc

Résultats :
Estreys - Salins : p  = 0.00000000433
![Resultats Wilcox LongPlano](https://zupimages.net/up/21/15/qsch.png)

-> Il y a donc une différence significative entre Estreys et Salins. Les diatomées Planothidium de la source des Salins sont plus petites que dans l'autre source en termes de longueur. 

#### Comparaison Largeur
Utilisation d'un test de Kruskal-Wallis (source code : [Datanovia](https://www.datanovia.com/en/fr/lessons/test-de-kruskal-wallis-dans-r/))

> LargPlano <- read.xlsx('/Users/fredericwolf/Desktop/Stage 2021/Mesures/Campagne mars 2021/stats_biovolumes.xlsx', 8, header=TRUE, colClasses=NA)
> ggboxplot(LargPlano, x = "Source", y = "Largeur")
> LargPlano <- LargPlano %>%
> + reorder_levels(Source, order = c("Ours", "Estreys", "Bard"))
> LargPlano %>%
> + group_by(Source) %>%
> + get_summary_stats(Largeur, type = "common")
> res.kruskal <- LargPlano %>% kruskal_test(Largeur~Source)
> res.kruskal

Résultat : p = 3.18e-14
![Resultat Kruskal LargPlano](https://zupimages.net/up/21/15/wsg7.png)

-> Il y a donc une différence significative de largeur entre des sources

Utilisation d'un test de Wilcoxon pour voir quelles sources sont différentes 

> pwc <- LargPlano %>%
> + wilcox_test(Largeur~Source, p.adjust.method = "bonferroni")
> pwc

Résultats :
Estreys - Salins : p = 3.21e-14
![Resultats Wilcox LargPlano](https://zupimages.net/up/21/15/niw8.png)

-> Il y a donc une différence significative entre les Estreys et les Salins. Les Estreys présentent les Planothidium les plus larges 

#### Comparaison Profondeur
Utilisation d'un test de Kruskal-Wallis (source code : [Datanovia](https://www.datanovia.com/en/fr/lessons/test-de-kruskal-wallis-dans-r/))

> ProfCreno <- read.xlsx('/Users/fredericwolf/Desktop/Stage 2021/Mesures/Campagne mars 2021/stats_biovolumes.xlsx', 6, header=TRUE, colClasses=NA)
> ggboxplot(ProfCreno, x = "Source", y = "Profondeur")
> ProfCreno <- ProfCreno %>%
> + reorder_levels(Source, order = c("Ours", "Estreys", "Bard"))
> ProfCreno %>%
> + group_by(Source) %>%
> + get_summary_stats(Profondeur, type = "common")
> res.kruskal <- ProfCreno %>% kruskal_test(Profondeur~Source)
> res.kruskal

Résultat : p = 0.231
![Resultats Kruskal ProfPlano](https://zupimages.net/up/21/15/qf64.png)

-> Il n'y a pas de différence significative de profondeur des Planothidium entre les sources Salins et Estreys
