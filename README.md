# 📚 OC - Projet 7 : Tableau de bord de suivi de projets - Power BI

Ce projet est une simulation de mission de consulting chez **Sanitoral**, société internationale spécialisée dans les soins bucco-dentaires. 
Rattaché au sein du département Project Management Office, il s’agit de concevoir un dashboard permettant le suivi des performances des projets en cours. 

Contraintes : 
3 niveaux d'accès à l'information en fonction de son rôle utilisateur (Directeur Général, Directeurs de Région et Directeurs de Pays)

---

## 🎯 Objectif de la mission

L’objectif est :
   - de fournir une vue claire et synthétique des indicateurs clés liés aux projets en cours.
   - d'identifier les projets en dépassement de plus de 15% par rapport aux prévisions initiales en termes de coûts, délais et qualité.

3 vues principales ont été développées : VUE GLOBALE (synthèse par zone géographique), VUE PROJET (détail par projet) et VUE PHASE (détail par phase de projet).
3 rôles utilisateurs avec des droits d’accès différenciés : Directeur Général, Directeur de Région et Directeur de Pays ont été pris en compte
Une attention particulière a été portée pour réaliser un tableau de bord permettant de traduire ces objectifs génériques en dashboard orienté métiers.

---

## 🛠️ Technologies et librairies utilisées

- `pandas` pour le traitement des données tabulaires
- `numpy` pour les opérations numériques
- `matplotlib`, `seaborn` pour les visualisations
- `datetime`, `scipy.stats` pour l’analyse temporelle et statistique

---

## 🧰 Méthodologie
3 étapes principales :

1. **Cadrage du besoin avec le client - Product Strategy Canvas (PSC)**
   - Users Stories par rôle utilisateur qui spécifie les besoins fonctionnels et techniques du dashboard
   - Définition des visuels d'avancement des projets, des indicateurs clés et des filtres nécessaires

2. **Conception d'un dashboard opérationnel Power BI**
   - Mockups et blueprint du dashboard issues du PSC
   - Importation, transformation et modélisation des données + relations entre tables
   - Identification des axes de lecture pour décision métiers et des besoins en terme de filtres opérationnels
      - Axe de lecture : Synthèse par Zone, Projets, Phases
      - Axe de lecture par composantes (Coût, Délai, Qualité) : TOP/FLOP pays ou projet ou phase
   - Liste des besoins en variables,calcul DAX, conception des filtres du dashboard pour traduire l'exigence "Alerte visuelle si projet en dépassement de 15%"

3. **Réalisation du dashboard Power BI**
   - Création des caluls DAX nécessaires pour répondre aux besoins métiers :
      - Calcul DAX des écarts (cout, délai, qualité) entre les prévisions initiales et les données réelles en quantité et pourcentage
      - Calcul DAX de l'état (OVERRUN, DRIFT, ON TARGET) de chaque composante (COST, DURATION, DELIVERABLE)
      - Calcul DAX de l'état global (OVERRUN, DRIFT, ON TARGET) d'une phase ou d'un projet à partir des états de ses 3 composantes
   - Création des segments, visuels, filtres et interactions pour une vue MODE, PROJET et PHASE
   - Ajout des drapeaux pays pour une meilleure lisibilité et expérience UX

---

## 📊 Résultats clés
- Vue Globale :
   - Vue synthétique du portefeuille de projets pour voir en un coup d’œil le nombre de projets et leur état (en dérive, OK, en dépassement) par région.​
   - Suivi global des coûts, délais et livrables en comparant le réalisé au planifié afin d’identifier rapidement les zones à risque.

- Vue Projet :
   - Vue détaillée du statut de chaque projet (par pays) avec filtrage par région, type de pays, ID projet et statut, pour repérer rapidement les projets en dérive.
   - Suivi des coûts, délais et livrables par projet avec indicateurs de variation et TOP5/FLOP5, afin d’identifier les pays/projets les plus performants ou les plus à risque.

- Vue Phase :
   - Détail des phases de chaque projet avec filtrage par région, type de pays, ID projet, phase et statut, pour un suivi granulaire.
   - Analyse des coûts, délais et livrables par phase avec indicateurs de variation et TOP5/FLOP5, afin d’identifier les phases les plus critiques.

- Vue Gantt :
   - Visualisation des pays/projets en dépassement de durée, avec le volume de retard en jours pour cibler les plus critiques.
   - Gantt détaillé comparant planning prévu et réalisé par phase, avec la variation de durée en jours pour analyser où se situent les dérives dans le temps.

---

## 🧠 Auteur

Projet réalisé par **ThibautOble** dans le cadre du parcours *Data Analyst* chez OpenClassrooms.

---

## 📄 Licence

Projet destiné à un usage pédagogique et stratégique. Les données ne doivent pas être utilisées à des fins commerciales.
