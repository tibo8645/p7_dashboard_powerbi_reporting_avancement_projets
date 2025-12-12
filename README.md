# 📚 OC - Projet 7 : Tableau de bord de suivi de projets - Power BI

## 📋 Description du projet 

Cette analyse s'inscrit dans une mission de consulting pour Sanitoral, une société internationale spécialisée dans les soins bucco-dentaires. 
Rattaché au sein du département Project Management Office (PMO), l'objectif est de concevoir un dashboard Power BI permettant le suivi des performances des projets en cours à travers différentes zones géographiques. 
Le tableau de bord doit répondre à une contrainte majeure : proposer 3 niveaux d'accès différenciés en fonction du rôle utilisateur (Directeur Général, Directeurs de Région et Directeurs de Pays), avec une attention particulière portée aux projets présentant des dépassements supérieurs à 15% par rapport aux prévisions initiales.

---

## 🎯 Objectif de la mission

L’objectif est :
   - de fournir une vue claire et synthétique des indicateurs clés liés aux projets en cours.
   - d'identifier les projets en dépassement de plus de 15% par rapport aux prévisions initiales en termes de coûts, délais et qualité.

- 3 vues principales ont été développées : VUE GLOBALE (synthèse par zone géographique), VUE PROJET (détail par projet) et VUE PHASE (détail par phase de projet).
- 3 rôles utilisateurs avec des droits d’accès différenciés : Directeur Général, Directeur de Région et Directeur de Pays ont été pris en compte

- Une attention particulière a été portée pour réaliser un tableau de bord permettant de traduire ces objectifs génériques en dashboard orienté métiers.

---

## 💡 Compétences développées

- **Power BI** : Conception de dashboards interactifs, modélisation de données, relations entre tables
- **Langage DAX** : Création de mesures calculées, indicateurs d'écart, logique conditionnelle pour alertes
- **Data modeling** : Structuration de modèles en étoile, optimisation des relations
- **Sécurité des données** : Implémentation de Row Level Security (RLS) pour accès différenciés
- **UX/UI Design** : Product Strategy Canvas, mockups, blueprint, optimisation de l'expérience utilisateur

---

## 📂 Sources de données
Le projet s'appuie sur un fichier Excel structuré contenant :

Projets : Informations sur les projets (ID, zone géographique, pays, région, type)
Phases : Détail des phases de chaque projet avec données prévisionnelles et réelles
Indicateurs : Coûts (budget vs réalisé), Délais (durée prévue vs réelle), Qualité (livrables prévus vs réalisés)

---

## 🛠️ Technologies et librairies utilisées

[![Power BI](https://img.shields.io/badge/Power_BI-F2C811?style=flat&logo=powerbi&logoColor=black)](https://powerbi.microsoft.com)
[![DAX](https://img.shields.io/badge/DAX-0078D4?style=flat&logo=microsoft-dax&logoColor=white)](https://dax.guide)
[![Power Query](https://img.shields.io/badge/Power_Query-0099F0?style=flat&logo=powerquery&logoColor=white)](https://powerquery.microsoft.com)

---

## 🗂️ Méthodologie
Le projet a été mené en plusieurs étapes clés :

1. **Cadrage du besoin client - Product Strategy Canvas (PSC)**
   - Élaboration de User Stories par rôle utilisateur
   - Définition des besoins fonctionnels et techniques du dashboard
   - Spécification des visuels d'avancement, indicateurs clés et filtres nécessaires

2. **Conception et modélisation**
   - Création de mockups et blueprint du dashboard
   - Importation et transformation des données dans Power BI
   - Modélisation des relations entre tables
   - Identification des axes de lecture métiers :
      - Axe synthèse par Zone, Projets, Phases
      - Axe analyse par composantes (Coût, Délai, Qualité)
      - TOP/FLOP pays, projets et phases

3. **Développement DAX et calculs métiers :**
   - Calcul des écarts (coût, délai, qualité) : quantité et pourcentage
   - Détermination de l'état par composante (COST, DURATION, DELIVERABLE) : OVERRUN / DRIFT / ON TARGET
   - Calcul de l'état global d'une phase ou projet (agrégation des 3 composantes)
   - Création des seuils d'alerte à 15% de dépassement

4. **Réalisation du dashboard Power BI**
   - Création des segments, visuels et filtres interactifs
   - Développement des 3 vues principales (Globale, Projet, Phase)
   - Ajout d'une vue Gantt pour le suivi temporel
   - Intégration de drapeaux pays pour améliorer l'UX
   - Implémentation de la sécurité RLS pour les 3 niveaux d'accès

---

**Aperçu du dashboard Power BI :**
https://github.com/tibo8645/p7_dashboard_powerbi_reporting_avancement_projets/blob/main/p7_aper%C3%A7u.pdf

## 📊 Aperçu du Dashboard

**[Voir l'aperçu complet du dashboard (PDF)](https://github.com/tibo8645/p7_dashboard_powerbi_reporting_avancement_projets/blob/main/p7_aper%C3%A7u.pdf)**

[![Aperçu Dashboard](https://img.shields.io/badge/Voir%20Aper%C3%A7u-PDF-red?style=for-the-badge&logo=adobe)](https://github.com/tibo8645/p7_dashboard_powerbi_reporting_avancement_projets/blob/main/p7_aper%C3%A7u.pdf)

---

## Auteur

Projet réalisé par **ThibautOble** dans le cadre du parcours *Data Analyst* chez OpenClassrooms.

---

## 📄 Licence

Projet destiné à un usage pédagogique et stratégique. Les données ne doivent pas être utilisées à des fins commerciales.
