# Exploration de données — Sell4All

Projet de sélection — Parcours Développement en Intelligence Artificielle (YouCode)

## Besoin

Sell4All est une entreprise de vente de vêtements d'occasion en ligne. Elle veut ajouter une fonctionnalité de recommandation de produits basée sur l'IA, et pour ça il faut d'abord explorer et nettoyer les données clients disponibles

Ce dépôt contient l'exploration du fichier `dataset-sell4all.csv` avec Python (Pandas, Matplotlib) dans un notebook Jupyter

## Étapes réalisées

**Jour 1** : création du dépôt GitHub, installation de l'environnement (Jupyter, Pandas, Matplotlib), lecture du fichier CSV, affichage des 5 premières lignes

**Jour 2** : génération et explication du résumé technique du dataset, calcul des statistiques descriptives (moyenne et médiane), calcul de la médiane d'âge par pays (bonus), Visualisation des dépenses par pays, nettoyage des données (suppression des lignes < 10 € et des doublons)

**Jour 3** : export du CSV nettoyé, finalisation et vérification du dépôt

## Fonctionnalités développées

- Lecture du CSV et affichage des 5 premières lignes
- Résumé technique du dataset (nombre de lignes, colonnes, types) avec explication
- Calcul de la moyenne et de la médiane pour `Age` et `Customer spendings`
- Calcul de la médiane d'âge par pays (bonus)
- Graphique à barres des dépenses par pays
- Nettoyage : suppression des lignes < 10 € de dépenses et des doublons
- Export d'un CSV nettoyé avec les colonnes `Country`, `Age`, `Gender`, `Customer spendings`

## Résultats

- Dataset initial : 505 lignes, 11 colonnes, aucune valeur manquante
- Âge moyen : 46,08 ans — médian : 46 ans
- Dépenses moyennes : 311,17 € — médianes : 307 €
- Après nettoyage (dépenses < 10 € + doublons) : 497 lignes
- Fichier final : `dataset-sell4all-clean.csv`

## Difficultés rencontrées

- La colonne `Postal code` est lue comme du texte par Pandas car certains codes contiennent des lettres/tirets selon le pays. Solution : ne pas la convertir, elle n'est de toute façon pas utilisée dans le projet
- Il fallait filtrer les dépenses < 10 € avant de supprimer les doublons, pour que le comptage des doublons se fasse sur les données déjà filtrées

## Mode d'exécution

### Prérequis

- Python 3.13
- Jupyter Notebook
- Pandas, Matplotlib

### Installation

```bash
# Installer directement les packages nécessaires (j'ai déja python)
pip install pandas matplotlib notebook
```

### Lancer le projet

```bash
jupyter notebook
```

Ouvrir `exploration_sell4all.ipynb` et exécuter les cellules dans l'ordre

## Contenu du dépôt

```
.
├── exploration_sell4all.ipynb
├── dataset-sell4all.csv
├── dataset-sell4all-clean.csv
└── README.md
```
