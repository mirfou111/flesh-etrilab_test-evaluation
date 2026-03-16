# Analyse de la Santé Maternelle en Afrique de l'Ouest
### Test d'évaluation EtriLabs — Programme FLESH

## Contexte

Ce notebook a été développé dans le cadre du processus de sélection du programme
FLESH | EtriLabs. Il porte sur l'analyse des déterminants de l'accouchement assisté
par un professionnel de santé en Afrique de l'Ouest, avec un focus sur les zones
rurales du Sénégal.

L'intérêt pour cette problématique est né d'un projet antérieur de prédiction des
pénuries de sang au Sénégal qui m'a conduit à explorer les causes profondes de
la mortalité maternelle, dont l'hémorragie du post-partum est l'une des premières.

## Objectifs

- Explorer et analyser le dataset sante_maternelle fourni par EtriLabs
- Tester deux hypothèses terrain sur les déterminants du suivi prénatal
- Construire un modèle de scoring de risque pour prioriser les interventions
  des agents de santé communautaires

## Structure du projet
```
etrilab-sante-maternelle/
│
├── data/                          # Dataset source (non versionné)
├── figures/                       # Visualisations générées
│   ├── distributions_cles.png
│   ├── hypothese1.png
│   ├── hypothese2.png
│   ├── evaluation_modeles.png
│   └── score_final.png
├── model/                         # Modèle sauvegardé
│   ├── scoring_risque_sante_maternelle.pkl
│   └── features_columns.pkl
├── analyse_sante_maternelle.ipynb # Notebook principal
└── README.md
```

## Résultats clés

- **H1 confirmée** — corrélation négative significative entre distance et CPN
  (Spearman r=-0.20, p<0.0001)
- **H2 confirmée** — les femmes visitées par un ASC accouchent plus souvent
  avec assistance (66.6% vs 55%, Chi² p<0.0001)
- **Modèle final** — régression logistique (AUC=0.71), le milieu rural et le
  niveau d'instruction sont les variables les plus déterminantes

## Stack technique

- Python 3.10
- pandas, numpy, scipy
- scikit-learn
- matplotlib, seaborn
- joblib

## Auteur

Ousmane NDIEGUENE Candidat au programme FLESH | EtriLabs — Thiès, Sénégal