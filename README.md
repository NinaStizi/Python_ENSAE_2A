# Python_ENSAE_2A

Projet Python de deuxième année pour le cours Python pour la Data Science réalisé par Dmitri Lebrun, Corentin Pernot, Nina Stizi. 

## Le but de ce projet est de prédire le Revenue d'un film en fonction de ses caractéristiques. 
Pour cela nous avons travaillé les thématiques suivantes : 
- I. Récupération des données 

      - I.1. Scrapping les titres de films sur une page Wikipédia https://en.wikipedia.org/wiki/List_of_years_in_film
      
      - I.2. Récupération de l'identifiant des films grâce à une API TMDB (the movie database)


            - I.2.1. Cas particulier pour un film
            - I.2.2. Généralisation 
      - I.3. Récupération des informations détaillées des films à partir de leur identifiant grâce à une autre API TMDB 


- II. Nettoyage des données 
      - II.1. Première visualisation/analyse rapide des données
      - II.2. Choix des variables utiles
      - II.3. Résolution des problèmes du dataset


- III. Visualisation et analyse graphique
      - III.1. Analyse de la répartition des données : description du dataset
      - III.2. Liens entre les variables
      - III.3. Analyse cartographique 

- IV. Modélisation 
      - IV.1. Preprocessing 
      - IV.2. Les modèles 
      - IV.3. Tuning des hyperparamètres pour le RandomForest

- V. Conclusion 


## Voilà les modules et packages nécessaires à la lecture du code :

1. Récupération des données et webscrapping

`!pip install lxml` \
`import requests`\
`import urllib`\
`import bs4`\
`import pandas as pd`\
`from urllib import request`\
`import re`\
`from tqdm import tqdm`\
`from scipy import *`

2. Visualisation et analyse des données

Lecture et traitement du dataframe:\
`import pandas as pd`\
`import numpy as np`

Rapport sur les données pandas :\
`!pip install pandas_profiling`\
`!pip install ipywidgets`\
`from pandas_profiling import ProfileReport`

Visualisation et analyse graphique des données\
`import matplotlib.pyplot as plt`

Visualisation et analyse cartographique des données\
`!pip install pandas fiona shapely pyproj rtree`\
`!pip install contextily`\
`!pip install geopandas`\
`import geopandas as `\
`import contextily as ctx`

Corrélation entre les données\
`import seaborn as sns`

3. Modélisation

Pour normaliser les données, on choisit MinMaxScaler de la librairie Sklearn\
`from sklearn.preprocessing import MinMaxScaler`\
`from sklearn.model_selection import train_test_split`\
`from sklearn.preprocessing import RobustScaler`\
`from sklearn.preprocessing import StandardScaler`

On implémente notre modèle grâce à la librairie Sklearn\
`from sklearn.linear_model import Ridge`
`from sklearn.linear_model import LassoCV`
`from sklearn.ensemble import RandomForestRegressor`
      
Pour mesurer la performance de nos modèles\
`from sklearn.metrics import mean_absolute_percentage_error, mean_squared_error, mean_absolute_error, explained_variance_score`\
`from scipy import stats`\
`from sklearn.model_selection import GridSearchCV`
