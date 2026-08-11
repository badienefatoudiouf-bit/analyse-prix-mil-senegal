# Analyse des prix du mil au Sénégal (2000-2020)

Analyse de la saisonnalité des prix du mil au Sénégal sur 20 ans, avec identification des régions les plus exposées aux variations de prix et recommandation d'action pour les producteurs.

## Contexte

Le mil est l'une des céréales vivrières les plus cultivées au Sénégal. Comme pour la plupart des denrées de base non stockées à grande échelle, son prix varie fortement selon la période de l'année : bas juste après la récolte, plus élevé en période de soudure (avant la récolte suivante). Cette analyse vise à quantifier cette variation saisonnière et à identifier les régions les plus concernées, afin d'orienter une recommandation concrète pour les producteurs et décideurs locaux.

## Sources de données

- **WFP (World Food Programme) — Food Prices Senegal**, via [Kaggle](https://www.kaggle.com/datasets/mexwell/crop-price-prediction-in-senegal) : relevés mensuels de prix de denrées de base (mil, riz, sorgho, arachide, niébé, maïs) par marché et région, de 2000 à 2020.

## Méthodologie

1. **Nettoyage des données** (Python / pandas)
   - Suppression d'une ligne de métadonnées techniques (format HXL)
   - Conversion de la colonne prix en type numérique
   - Conversion de la colonne date en type date
2. **Analyse exploratoire**
   - Évolution du prix moyen du mil dans le temps (2000-2020)
   - Calcul du prix moyen par mois (toutes années confondues) pour identifier la saisonnalité
   - Comparaison de l'écart saisonnier (min-max) entre les 14 régions du Sénégal
3. **Visualisation** (Power BI)
   - Dashboard interactif avec filtre par produit
   - Graphique d'évolution temporelle, comparaison régionale, saisonnalité mensuelle

## Résultats clés

- Le prix du mil a suivi une tendance à la hausse générale entre 2000 et 2020.
- Un pic marqué en 2005 suivi d'une chute en 2006-2007, une période cohérente avec la crise alimentaire mondiale de 2007-2008.
- **Écart saisonnier national : 13,7%** en moyenne entre février (prix le plus bas, post-récolte) et septembre (prix le plus haut, période de soudure).
- Forte disparité régionale : **Thiès (25,6%)** est la région la plus exposée à cette variation saisonnière, contre seulement **9% à Ziguinchor**.

## Recommandation

L'analyse des prix du mil au Sénégal entre 2000 et 2020 montre un écart moyen de 13,7% entre la période post-récolte (février) et la période de soudure (septembre). Cette variation est particulièrement marquée dans la région de Thiès, où l'écart atteint 25,6%, contre seulement 9% à Ziguinchor. Il est donc recommandé de construire des hangars de stockage, en priorité dans la région de Thiès. Cela permettrait aux producteurs de pouvoir garder plus longtemps le mil et de le vendre avec plus de bénéfices durant la période de soudure.

## Outils utilisés

- **Python** (pandas, matplotlib) — nettoyage et analyse exploratoire
- **Power BI** — dashboard interactif
- **Excel/CSV** — données sources

## Limites

- Les pourcentages obtenus pour les régions de Sédhiou et Kédougou sont à interpréter avec prudence : leurs données sont nettement plus limitées (moins de 250 relevés chacune, contre plus de 800 pour Fatick ou Dakar), ce qui réduit la fiabilité des écarts calculés pour ces deux régions.
- L'analyse porte uniquement sur le mil ; les autres produits du dataset (riz, sorgho, arachide) suivent probablement des dynamiques saisonnières différentes.
- La recommandation se limite à ce que les données de prix montrent ; elle ne s'appuie pas sur des données de coûts d'infrastructure ou de rentabilité économique du stockage, qui mériteraient une analyse complémentaire.

## Fichiers du dépôt

- Notebook Python (nettoyage + analyse)
- Fichier CSV nettoyé
- Capture d'écran du dashboard Power BI
