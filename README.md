# 🧮 Simulateur de Retraite Progressive - Fonctionnaire d'État

[![Version](https://img.shields.io/badge/version-4.2.4-green.svg)](https://github.com/votre-repo/simulateur-retraite)
[![License](https://img.shields.io/badge/license-Informative-blue.svg)](LICENSE)
[![Réglementation](https://img.shields.io/badge/réglementation-Décret%202023--799-orange.svg)](https://www.legifrance.gouv.fr/jorf/id/JORFTEXT000047970226)

Un simulateur pédagogique et transparent pour estimer votre retraite progressive et définitive en tant que fonctionnaire d'État, basé sur la méthode officielle du Service des Retraites de l'État (SRE).

---

## 🎯 Objectif

Ce simulateur vous aide à :
- 📊 **Comprendre** les mécanismes de la retraite progressive
- 💰 **Estimer** votre pension selon différents scénarios
- 📈 **Comparer** l'impact des quotités de travail
- 🔍 **Analyser** la rentabilité de la surcotisation et du rachat de trimestres
- 🎓 **Apprendre** les règles complexes du régime de retraite des fonctionnaires

---

## ⚡ Démarrage rapide

### Installation (aucune installation requise !)

1. **Téléchargez** le fichier `simulateur_retraite_Version_V.04.2.4.html`
2. **Double-cliquez** pour l'ouvrir dans votre navigateur
3. **C'est tout !** Aucun serveur, aucune connexion internet nécessaire

### Première utilisation

1. Rendez-vous dans l'onglet **"Paramètres"**
2. Remplissez vos informations à partir de votre relevé de carrière SRE
3. Cliquez sur **"Calculer la simulation"**
4. Consultez vos résultats dans les différents onglets

---

## ✨ Fonctionnalités principales

### 📋 6 onglets complets

| Onglet | Description |
|--------|-------------|
| **Paramètres** | Saisie de vos données personnelles et professionnelles |
| **Résultats RP** | Simulation détaillée de la retraite progressive |
| **Retraite Définitive** | Projection de votre retraite sans période progressive |
| **Graphique** | Comparaison visuelle des revenus selon la quotité |
| **Analyse Rachat** | Évaluation de la rentabilité du rachat de trimestres |
| **Sources** | Références réglementaires et documentation |

### 🔧 Calculs avancés

- ✅ **Méthode SRE officielle** (base 360 jours/an, arrondi ≥45 jours)
- ✅ **Décote et surcote** (3 types cumulables : classique, parentale, excédentaire)
- ✅ **Bonifications enfants** (avant/après 2004)
- ✅ **Majoration familiale** (10% dès 3 enfants)
- ✅ **Décret n°82-624** (6/7ème pour 80%, 32/35ème pour 90%)
- ✅ **Analyse actuarielle** de la surcotisation (vs placements alternatifs)
- ✅ **Surcote parentale** (Décret 2023-799)

### 📊 Outils d'aide à la décision

- 📈 **Graphiques interactifs** (revenus selon quotité, pensions comparées)
- 💡 **Analyses de rentabilité** (surcotisation, rachat de trimestres)
- 💾 **Export/Import** de simulations (format JSON)
- 🎯 **Recommandations personnalisées** selon votre profil

---

## 🆕 Nouveautés V.04.2.4

### 🔧 Correction majeure

**✅ Documentation corrigée sur la pension provisoire**

Après vérification des sources officielles (Service-Public.fr, SRE, CNRACL), une **correction importante** a été apportée :

#### ❌ Ancienne version (incorrecte)
> "La pension provisoire est figée à la date du départ progressif et ne bouge plus pendant toute la période"

#### ✅ Nouvelle version (correcte)
> "La pension provisoire est calculée au départ progressif, MAIS :
> - Si vous changez de quotité, la part versée s'ajuste automatiquement
> - Exemple : passage de 80% → 70% de travail, la pension passe de 20% → 30%
> - Le montant de référence reste fixe
> - Les nouveaux trimestres acquis ne modifient PAS le montant provisoire
> - Recalcul complet à la retraite définitive"

### 📝 Améliorations

- 🔵 **Encadré informatif** dans l'onglet Paramètres expliquant l'évolution de la pension
- 🔵 **Note dans les résultats** rappelant l'ajustement possible
- 🔵 **Section mise à jour** dans l'onglet Sources avec les explications correctes
- 🔵 **Mode d'emploi et README** entièrement mis à jour

---

## 📚 Documentation

### Mode d'emploi complet
Consultez le fichier **[MODE_EMPLOI.md](MODE_EMPLOI.md)** pour :
- Guide détaillé de chaque onglet
- Explications des calculs
- Cas d'usage concrets
- FAQ complète
- Conseils stratégiques

### Sources réglementaires

Le simulateur s'appuie sur :

| Texte | Description |
|-------|-------------|
| **Code des pensions civiles et militaires** | Articles L11 à L18, L89 bis à L89 ter |
| **Décret n°2023-799** (21/08/2023) | Surcote parentale (1,25% par trimestre, max 5%) |
| **Décret n°82-624** (20/07/1982) | Temps partiel (6/7ème et 32/35ème) |
| **Loi n°2023-270** (14/04/2023) | Réforme des retraites 2023 |
| **Arrêté du 23/06/2023** | Valeur du point d'indice (4,92278 €) |

**Sources officielles consultées :**
- [Service des Retraites de l'État](https://retraitesdeletat.gouv.fr)
- [Service-Public.fr](https://www.service-public.fr/particuliers/vosdroits/F37400)
- [CNRACL](https://www.cnracl.retraites.fr)
- [Code des pensions (Légifrance)](https://www.legifrance.gouv.fr/codes/id/LEGITEXT000006070302/)

---

## ⚠️ Avertissements importants

### Non-opposabilité

| ❌ Ce simulateur | ✅ Simulateur officiel SRE/ENSAP |
|-----------------|----------------------------------|
| Aide à la décision | **Seul résultat opposable** |
| Transparence pédagogique | Calcul exact mais opaque |
| Écart possible 1-2% | Référence légale |

**➡️ Pour une estimation officielle définitive, consultez toujours [ensap.gouv.fr](https://ensap.gouv.fr)**

### Écart connu

Un écart de **1 à 2 trimestres liquidables** (~1-2% de pension) peut exister avec le calcul officiel du SRE, probablement dû à des règles d'arrondi internes non documentées publiquement.

**Le simulateur applique rigoureusement la méthode SRE documentée.**

### Règle des six mois

Une augmentation d'indice majoré doit avoir **≥ 6 mois d'ancienneté** avant le départ en retraite pour être prise en compte.

---

## 🧮 Méthodologie de calcul

### Formule de base
Pension = Traitement indiciaire × 75% × (Trimestres liquidables / Trimestres requis)

### Méthode SRE (base 360 jours/an)

- **1 année = 360 jours**
- **1 mois = 30 jours**
- **1 trimestre = 90 jours**
- **Arrondi final** : ≥45 jours = +1 trimestre

### Pension provisoire (retraite progressive) ⭐ CORRIGÉ V.04.2.4

**Au départ progressif :**
Pension de référence = Traitement × 75% × (Liquidables au départ / Trimestres requis)
Pension provisoire = Pension de référence × (1 - quotité)

**Si changement de quotité :**
Nouvelle pension provisoire = Pension de référence × (1 - nouvelle quotité)

**Exemple concret :**
- Liquidables au départ : 142 trimestres
- Pension de référence : 1 457 €
- Quotité 80% → pension : 1 457 × 20% = **291 €**
- **Changement à 70%** → pension : 1 457 × 30% = **437 €**
- ✅ Le montant de référence (1 457 €) reste identique
- ✅ Seul le pourcentage versé évolue

### Temps partiel

| Type | Comptabilisation |
|------|------------------|
| **Assurance** | Toujours 100% |
| **Liquidables** | Proratisés selon quotité (sauf surcotisation) |
| **Décret 1982** | 80% → 6/7ème, 90% → 32/35ème (si applicable) |

### Surcotes (3 types cumulables)

1. **Surcote classique** : 1,25% par trimestre au-delà de l'âge légal
2. **Surcote parentale** : 1,25% par trimestre l'année avant l'âge légal (max 5%)
3. **Majoration excédentaire** : 1,25% par trimestre excédentaire restant

---

## 🎯 Cas d'usage

### Exemple 1 : Fonctionnaire avec carrière complète

**Profil :**
- Génération 1964 (171 trimestres requis)
- 160 trimestres d'assurance au relevé
- 142 trimestres liquidables au relevé
- Indice 478

**Objectif :** Comprendre l'impact d'une retraite progressive à 80%

**Utilisation du simulateur :**
1. Saisie des données dans l'onglet Paramètres
2. Simulation avec quotité 80% pendant 18 mois
3. Consultation du graphique pour comparer avec d'autres quotités
4. Analyse de la rentabilité de la surcotisation

**Résultat :** Décision éclairée sur la quotité optimale

### Exemple 2 : Fonctionnaire avec carrière incomplète

**Profil :**
- Génération 1968 (172 trimestres requis)
- 155 trimestres d'assurance au relevé
- Décote prévisible

**Objectif :** Éviter la décote

**Utilisation du simulateur :**
1. Onglet Analyse Rachat : simulation du rachat de 4 trimestres
2. Comparaison avec un placement alternatif
3. Calcul de la rentabilité selon l'espérance de vie

**Résultat :** Décision sur l'opportunité du rachat

### Exemple 3 : Parent de 3 enfants

**Profil :**
- 3 enfants élevés 9 ans avant leurs 16 ans
- 2 enfants avant 2004, 1 enfant après 2003
- Génération 1964

**Objectif :** Maximiser les bonifications et la surcote parentale

**Utilisation du simulateur :**
1. Activation des bonifications enfants dans Paramètres
2. Simulation d'un départ l'année avant l'âge légal
3. Vérification de l'obtention de la surcote parentale (max 5%)
4. Calcul de la majoration familiale (+10%)

**Résultat :** Optimisation du moment du départ et de la quotité

---

## 💻 Aspects techniques

### Technologies utilisées

- **HTML5** : Structure de l'application
- **CSS3** : Interface responsive et moderne
- **JavaScript (Vanilla)** : Logique métier et calculs
- **Chart.js** : Visualisations graphiques

### Compatibilité

| Navigateur | Version minimale | Support |
|------------|-----------------|---------|
| Chrome | 90+ | ✅ Complet |
| Firefox | 88+ | ✅ Complet |
| Safari | 14+ | ✅ Complet |
| Edge | 90+ | ✅ Complet |

### Performances

- ⚡ **Chargement instantané** (fichier unique ~100 Ko)
- 🔒 **100% local** (aucune donnée transmise)
- 💾 **Pas de base de données** requise
- 📱 **Responsive** (mobile, tablette, desktop)

### Architecture
simulateur.html
├── Structure HTML
│   ├── 6 onglets (tabs)
│   ├── Formulaires de saisie
│   └── Zones d'affichage des résultats
├── Styles CSS
│   ├── Design moderne
│   ├── Mode responsive
│   └── Thème vert (fonctionnaire)
└── Logique JavaScript
├── Calculs SRE (base 360j/an)
├── Analyses actuarielles
├── Génération de graphiques
└── Export/Import JSON

---

## 🔧 Développement

### Structure du code

**Fonctions principales :**
```javascript
// Calculs de base
calculerPeriodesServiceSRE(dateDebut, dateFin)
arrondirTrimestresLiquidables(totalJours)
calculerDureeAssurance(totalJours)

// Calculs de pension
calculer() // Retraite progressive
calculerRetraiteDefinitive() // Retraite définitive
calculerSurcoteParentaleSRE(...) // Surcote parentale

// Analyses
calculerRentabiliteSurcotisation(...)
analyserRachat()

// Interface
switchTab(tabName)
updateChart(...)
exporterParametresUtilisateur()
Contribuer
Les contributions sont les bienvenues ! Pour contribuer :

Fork le projet
Créez une branche (git checkout -b feature/amelioration)
Committez vos changements (git commit -m 'Ajout fonctionnalité')
Push vers la branche (git push origin feature/amelioration)
Ouvrez une Pull Request

Signaler un bug
Ouvrez une Issue avec :

Description détaillée du problème
Étapes pour reproduire
Captures d'écran si applicable
Version du navigateur


📝 Historique des versions
V.04.2.4 (Janvier 2025) - Actuelle

🔴 CORRECTION MAJEURE : Documentation pension provisoire (évolution quotité)
✅ Ajout encadré informatif dans Paramètres
✅ Mise à jour onglet Sources
✅ Correction MODE_EMPLOI.md et README.md

V.04.2.3 (Janvier 2025)

✨ Nouvel onglet "Retraite Définitive"
✨ Option Décret 1982 (6/7ème et 32/35ème)
📊 Graphiques optimisés (aspectRatio: 3, max-width: 800px)

V.04.2.x (2024)

Amélioration interface utilisateur
Optimisation des performances
Corrections de bugs mineurs

V.04.1.x (2024)

Ajout onglet "Analyse Rachat"
Comparaison avec placements alternatifs
Barèmes 2024

V.04.0.x (2023)

Intégration Décret 2023-799 (surcote parentale)
Refonte complète de l'interface
Système d'onglets

Versions antérieures

V.03.x : Première version publique
V.02.x : Beta testing
V.01.x : Prototype


📋 Roadmap
Version 4.3.x (Prévue Q1 2025)

 Ajout de scenarios "what-if" multiples
 Export PDF des résultats
 Mode sombre
 Comparaison côte à côte de 2 simulations

Version 4.4.x (Prévue Q2 2025)

 Intégration des régimes spéciaux
 Calculateur de pension de réversion
 API pour intégration externe

Version 5.0.x (Prévue Q3 2025)

 Application web progressive (PWA)
 Synchronisation cloud optionnelle
 Mode collaboratif (conseiller retraite)


🤝 Remerciements
Ce projet a été rendu possible grâce à :

📚 Documentation officielle du SRE et de Service-Public.fr
👥 Retours des utilisateurs fonctionnaires d'État
🐛 Signalements de bugs permettant les corrections
💡 Suggestions d'amélioration de la communauté

Merci particulier aux utilisateurs qui ont signalé l'inexactitude sur la pension provisoire, permettant la correction de la V.04.2.4.

📄 Licence
Usage personnel libre - À des fins informatives et pédagogiques uniquement.
Clause de non-responsabilité :

Ce simulateur est fourni "tel quel" sans garantie
Les résultats sont des estimations
Seuls les calculs officiels du SRE font foi
L'auteur ne peut être tenu responsable des décisions prises sur la base de ces estimations

Utilisation commerciale : Requiert une autorisation écrite.

📞 Support et Contact
Questions techniques

🐛 Ouvrir une Issue
💬 Discussions

Questions sur votre retraite

🏛️ Service des Retraites de l'État
💻 ENSAP - Simulation officielle
📞 Votre service RH


🔗 Liens utiles
Sites officiels

ensap.gouv.fr - Simulation officielle
retraitesdeletat.gouv.fr - SRE
service-public.fr - Retraite progressive
info-retraite.fr - Portail commun

Documentation technique

Légifrance - Code des pensions
Décret 2023-799
INSEE - Tables de mortalité


🌟 Donnez une étoile !
Si ce simulateur vous a été utile, n'hésitez pas à :

⭐ Donner une étoile au projet
🔄 Partager avec vos collègues
💬 Laisser un commentaire
🐛 Signaler des bugs
💡 Proposer des améliorations


<div align="center">
Made with ❤️ for French civil servants
Version : V.04.2.4 | Date : Janvier 2025 | Réglementation : Décret n° 2023-799 du 21 août 2023
</div>
```
