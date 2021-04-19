# Mesure Biovolumes
## Campagne Mars 2021
### Navicula
#### Comparaison Longueur 
Utilisation d'un test de Kruskal-Wallis (source code : [Datanovia](https://www.datanovia.com/en/fr/lessons/test-de-kruskal-wallis-dans-r/))

> LongNavi <- read.xlsx('/Users/fredericwolf/Desktop/Stage 2021/Mesures/Campagne mars 2021/stats_biovolumes.xlsx', 1, header=TRUE, colClasses=NA)
> ggboxplot(LongNavi, x = "Source", y = "Longueur")
![BoxPlot LongNavi](https://zupimages.net/up/21/16/b64d.png)
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
![BoxPlot LargNavi](https://zupimages.net/up/21/16/806p.png)
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
![BoxPlot ProfNavi](https://zupimages.net/up/21/16/uq8g.png)
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
![BoxPlot LongCreno](https://zupimages.net/up/21/16/jcdr.png)
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
![BoxPlot LargCreno](https://zupimages.net/up/21/16/e275.png)
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
![BoxPlot ProfCreno](https://zupimages.net/up/21/16/pm7n.png)
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
![BoxPlot LongPlano](https://zupimages.net/up/21/16/r26r.png)
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
![BoxPlot LargPlano](https://zupimages.net/up/21/16/hoa4.png)
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
![BoxPlot ProfCreno](https://zupimages.net/up/21/16/kf0o.png)
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

### Vérification Normalité
La normalité est vérifiée par un test de Shapiro-Wilk, complété par des représentations graphiques (Diagramme de densité et QQPlot) (source code : [Datanovia](https://www.datanovia.com/en/fr/lessons/test-de-normalite-dans-r/))
#### Planothidium
> ggdensity(ProfPlano$Profondeur, fill = "lightgray")
![Normalite ProfPlano](https://zupimages.net/up/21/16/z9ba.png)
> ggqqplot(ProfPlano$Profondeur)
![QQPlot ProfPlano](https://zupimages.net/up/21/16/u9na.png)
> ProfPlano %>% shapiro_test(Profondeur)

Résultat : p = 1.92e-17
![Resultats Shapiro ProfPlano](https://zupimages.net/up/21/16/nv48.png)

> ggdensity(LargPlano$Largeur, fill = "lightgray")
![Normalite LargPlano](https://zupimages.net/up/21/16/u6fs.png)
> ggqqplot(LargPlano$Largeur)
![QQPlot LargPlano](https://zupimages.net/up/21/16/8q3l.png)
> LargPlano %>% shapiro_test(Largeur)

Résultat : p = 1.83e-13
![Resultats ShapiroLargPlano](https://zupimages.net/up/21/16/7f97.png)

> ggdensity(LongPlano$Longueur, fill = "lightgray")
![Normalite LongPlano](https://zupimages.net/up/21/16/4ax9.png)
> ggqqplot(LongPlano$Longueur)
![QQPlot LongPlano](https://zupimages.net/up/21/16/stc6.png)
> LongPlano %>% shapiro_test(Longueur)

Résultat : p = 0.00451
![Resultats ShapiroLongPlano](https://zupimages.net/up/21/16/efnv.png)

### Crenotia
> ggdensity(ProfCreno$Profondeur, fill = "lightgray")
![Normalite ProfCreno](https://zupimages.net/up/21/16/91zl.png)
> ggqqplot(ProfCreno$Profondeur)
![QQPlot ProfCreno](https://zupimages.net/up/21/16/u6lu.png)
> ProfCreno %>% shapiro_test(Profondeur)

Résultat : p = 0.00000186
![Resultats Shapiro ProfCreno](https://zupimages.net/up/21/16/ctu2.png)

> ggdensity(LargCreno$Largeur, fill = "lightgray")
![Normalite LargCreno](https://zupimages.net/up/21/16/91zl.png)
> ggqqplot(LargCreno$Largeur)
![QQPlot LargCreno](https://zupimages.net/up/21/16/u6lu.png)
> LargCreno %>% shapiro_test(Largeur)

Résultat : p = 1.40e-14
![Resultats ShapiroLargCreno](https://zupimages.net/up/21/16/nisx.png)

> ggdensity(LongCreno$Longueur, fill = "lightgray")
![Normalite LongCreno](https://zupimages.net/up/21/16/hgzv.png)
> ggqqplot(LongCreno$Longueur)
![QQPlot LongCreno](https://zupimages.net/up/21/16/yndz.png)
> LongCreno %>% shapiro_test(Longueur)

Résultat : p = 8.32e-11
![Resultats ShapiroLongCreno](https://zupimages.net/up/21/16/gtgf.png)

### Navicula
> ggdensity(ProfNavi$Profondeur, fill = "lightgray")
![Normalite ProfNavi](https://zupimages.net/up/21/16/fx1b.png)
> ggqqplot(ProfNavi$Profondeur)
![QQPlot ProfNavi](https://zupimages.net/up/21/16/p260.png)
> ProfNavi %>% shapiro_test(Profondeur)

Résultat : p = 0.00635
![Resultats Shapiro ProfNavi](https://zupimages.net/up/21/16/s26o.png)

> ggdensity(LargNavi$Largeur, fill = "lightgray")
![Normalite LargNavi](https://zupimages.net/up/21/16/26s7.png)
> ggqqplot(LargNavi$Largeur)
![QQPlot LargNavi](https://zupimages.net/up/21/16/9io1.png)
> LargNavi %>% shapiro_test(Largeur)

Résultat : p = 1.41e-15
![Resultats ShapiroLargNavi](https://zupimages.net/up/21/16/1tni.png)

> ggdensity(LongNavi$Longueur, fill = "lightgray")
![Normalite LongNavi](https://zupimages.net/up/21/16/pz2a.png)
> ggqqplot(LongNavi$Longueur)
![QQPlot LongNavi](https://zupimages.net/up/21/16/01yq.png)
> LongNavi %>% shapiro_test(Longueur)

Résultat : p = 0.0000707
![Resultats ShapiroLongNavi](https://zupimages.net/up/21/16/6dr8.png)
