# Projet Python
*Par Matthieu Humbert, Alice Israël et Nour Tekaya, 2025.*

**Sujet :** Etude de la différence de valorisation boursière (PER) des grandes entreprises européennes et américaines

# Table des matières
1. [Définitions](#definitions)
2. [Objectifs](#objectifs)
3. [Sources des données](#sources)
4. [Présentation du dépôt](#pres)

## 1. Définitions <a name="definitions">

**Valorisation boursière (PER)** 

Le *Price Earning Ratio* (PER) est la mesure standard pour comparer deux valorisations boursières. Il s'obtient selon la formule *(Prix de l'action)/(Bénéfice par action)* = *(Capitalisation boursière)/(Résultat net)*.

De manière plus intuitive, il indique qu'une entrerpise "s'achète" *PER fois* ses bénéfices annuels. 

Ainsi, plus le *PER* est élevé, plus l'entreprise est *chère*. Il permet de distinguer des entreprises faiblement valorisées et fortement valorisées.

> Par exemple, au 22/12/2025, NVIDIA affiche un PER de 45, contre seulement 3 pour AirFrance.

Un *PER* élevé indique généralement que le marché anticipe une forte de croissance des bénéfices futurs. Il n'est donc pas surprenant d'avoir des *PER* élevés dans la tech, mais faibles dans l'automobile.

(Source : https://fr.wikipedia.org/wiki/Price-earnings_ratio)

**Grandes entreprises européennes et américaines**

Par souci de concision, nous appelons grandes entreprises europénnes les sociétés cotées sur le continent européen et incluses dans l'indice EuroStoxx 600. De même, sont appelées grandes entreprises américaines les sociétés cotées aux États-Unis et incluses dans le S&P 500.

Dès lors, notre étude se restreint donc aux 600 plus grosses capitalisations boursières européennes et aux 500 plus grosses capitalisations boursières américaines. 

**Le *premium* américain**

Nous appelons *premium* américain l'eventuel surcroît de valorisation des grandes entreprises américaines par rapport à leurs homologues européennes, mesuré par le PER.

## 2. Objectifs <a name="objectifs">

Notre objectif est double, nous cherchons à :
1. Vérifier l’existence du *premium* américain. 
2. Expliquer l'existence de ce *premium*

Plus précisément, nous allons comparer les PER des entreprises européennes et américaines. Diverses données financières (EPS, ROE, Marge nette, Dette, Résultat net...), qualitatives (secteur d'activité) ou macro (spread du pays, taux d'IS, equity-risk premium) seront ensuite exploitées comme variables explicatives.

## 3. Sources des données <a name="sources">

Nos données proviennent des sources suivantes : 

- Professeur Domodaran pour le site NYU (pour les données macro);
- Wikipedia (pour la liste des tickers du S&P500);
- DividendMax (pour la liste des tickers de l'EuroStoxx 600);
- YahooFinance (pour les données financières).

Aucune véritable API gratuite ne permettant de collecter la masse de données nécessaire, nous avons exclusivement eu recours à du *scrapping*. Toutefois, nous avons utilisé une sorte d'API non officielle pour scrapper les données YahooFinance.

## 4. Présentation du dépôt <a name=pres>

Notre rapport est découpé en trois notebooks :
- Le premier explique notre démarche de collecte et de nettoyage des données : ```clean_and_collect.ipynb```
- Le deuxième présente notre analyse préliminaire des données : ```exploratory_data_analysis.ipynb``
- Le troisième expose notre proposition de modélisation explicative : ```modeling.ipynb```

Le dossier ```data``` contient une copie locale des données tirées de nos sources. 