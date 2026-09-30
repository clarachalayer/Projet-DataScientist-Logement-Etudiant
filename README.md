# 🏠 Aide à la recherche de logement étudiant en Île-de-France

Projet du cours **Data Scientist** : un notebook interactif d'aide à la décision pour un étudiant qui cherche un logement **adapté à son budget**, **proche de son école** et dans un **environnement agréable** (transports, espaces verts, commerces, sécurité).

Il croise des données ouvertes : logements CROUS et privés, établissements d'enseignement supérieur, gares, espaces verts, commerces et criminalité par département.

## Les 10 widgets

| # | Widget | Ce qu'il permet |
|---|---|---|
| 1 | Carte école / transports / logements | Voir une école, les résidences CROUS, les logements privés et les gares les plus proches |
| 2 | Espaces verts | Trouver les parcs les plus proches d'un logement |
| 3 | Écoles par secteur | Répartition public / privé par département |
| 4 | Recommandation de logements | Classer les logements CROUS et privés autour d'une école selon budget, distance et surface |
| 5 | Commerces par arrondissement | Densité de commerces alimentaires et classiques |
| 6 | Loyers CROUS vs privés | Comparer loyers et surfaces |
| 7 | Sécurité et coût de la vie | Criminalité et loyer moyen par département |
| 8 | Score d'accessibilité | Indice composite par école (transports, logements, services) |
| 9 | Simulateur de budget | Budget mensuel complet selon l'école et le logement choisis |
| 10 | Carte de densité | Heatmap des services étudiants |

## Lancer le notebook

```bash
pip install -r requirements.txt
jupyter notebook logement_etudiant_paris.ipynb
```

Les widgets `ipywidgets` fonctionnent dans Jupyter ou Google Colab (pas dans l'aperçu GitHub, qui affiche seulement les sorties enregistrées).

### Données

Les fichiers CSV sont à placer dans `data/` :

```
crous_idf_loyers_geo_complet.csv
idf_lt50_appart_avec_prix_location.csv
etablissements_IDF_final.csv
emplacement-des-gares-idf.csv
espaces_verts_idf.csv
magasins_nourriture_long.csv
magasins_classiques_long.csv
taux_criminalite_idf_par_departement_2024.csv
```

## Stack

Python · pandas · NumPy · Folium (cartes, heatmaps) · Plotly · Matplotlib · Seaborn · ipywidgets · geopy · pyproj
