# 🧮 Simulateur de Retraite Progressive - Fonctionnaire d'État

[![Version](https://img.shields.io/badge/version-4.2.5-green.svg)](https://github.com/votre-repo/simulateur-retraite)
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

1. **Téléchargez** le fichier `simulateur_retraite_Version_V.04.2.5.html`
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
- ✅ **Rachat de trimestres** avec coefficients Fonction Publique d'État

### 📊 Outils d'aide à la décision

- 📈 **Graphiques interactifs** (revenus selon quotité, pensions comparées)
- 💡 **Analyses de rentabilité** (surcotisation, rachat de trimestres)
- 💾 **Export/Import** de simulations (format JSON)
- 🎯 **Recommandations personnalisées** selon votre profil

---

## 🆕 Nouveautés V.04.2.5

### 🔴 CORRECTION MAJEURE - Rachat de trimestres

**✅ Remplacement complet des barèmes de rachat**

Les barèmes utilisés dans les versions précédentes étaient ceux du **régime général (secteur privé)**, ce qui donnait des coûts **2 à 3 fois trop élevés** pour les fonctionnaires d'État !

#### ❌ Ancienne méthode (V.04.2.4 et antérieures)
Barèmes fixes secteur privé :

40 ans, Option 2 : 7 600 € par trimestre
50 ans, Option 2 : 11 200 € par trimestre


**Exemple :** 4 trimestres à 40 ans = **15 200 €** (FAUX)

#### ✅ Nouvelle méthode (V.04.2.5)
Coefficient Fonction Publique × Traitement indiciaire :

40 ans, Option 2 : ~62% du traitement
Traitement 2 353 € × 0,62 = 1 459 € par trimestre


**Exemple :** 4 trimestres à 40 ans = **5 836 €** (CORRECT)

### 📊 Comparaison des résultats

| Critère | V.04.2.4 (FAUX) | V.04.2.5 (CORRECT) | Différence |
|---------|-----------------|--------------------| ------------|
| **Coût 4 trim. (40 ans, Opt. 2)** | 15 200 € | 5 836 € | **-9 364 €** (-62%) |
| **Coût réel (TMI 30%)** | 10 640 € | 4 085 € | **-6 555 €** (-62%) |
| **Durée rentabilisation** | 15-20 ans | 7-10 ans | **÷2** |

### 🔧 Améliorations techniques

- ✅ **Coefficients Fonction Publique** (catégorie sédentaire, base 2024)
- ✅ **Interpolation linéaire** des coefficients selon l'âge précis
- ✅ **Calcul dynamique** basé sur votre traitement indiciaire
- ✅ **Tableau des coefficients** dans l'onglet Sources
- ✅ **Avertissements renforcés** sur le caractère indicatif

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
| **Code des pensions civiles et militaires** | Articles L11 à L18, L89 bis à L89 ter, L9 |
| **Décret n°2023-799** (21/08/2023) | Surcote parentale (1,25% par trimestre, max 5%) |
| **Décret n°82-624** (20/07/1982) | Temps partiel (6/7ème et 32/35ème) |
| **Décret n°2007-262** (27/02/2007) | Rachat de trimestres fonction publique |
| **Loi n°2023-270** (14/04/2023) | Réforme des retraites 2023 |
| **Arrêté du 23/06/2023** | Valeur du point d'indice (4,92278 €) |

**Sources officielles consultées :**
- [Service des Retraites de l'État](https://retraitesdeletat.gouv.fr)
- [Service-Public.fr](https://www.service-public.fr/particuliers/vosdroits/F37400)
- [Service-Public.fr - Rachat](https://www.service-public.fr/particuliers/vosdroits/F13243)
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

### Écart connu - Calcul de la pension

Un écart de **1 à 2 trimestres liquidables** (~1-2% de pension) peut exister avec le calcul officiel du SRE, probablement dû à des règles d'arrondi internes non documentées publiquement.

**Le simulateur applique rigoureusement la méthode SRE documentée.**

### Rachat de trimestres - Coefficients indicatifs

**Important :** Les coefficients utilisés pour le rachat sont indicatifs (base 2024, catégorie sédentaire). Le coût exact dépend de nombreux paramètres :
- Votre traitement indiciaire au moment du rachat
- Votre catégorie (sédentaire, actif, insalubre)
- Les barèmes en vigueur à la date du rachat

**Pour un devis personnalisé et opposable, contactez toujours le SRE via [ensap.gouv.fr](https://ensap.gouv.fr)**

### Règle des six mois

Une augmentation d'indice majoré doit avoir **≥ 6 mois d'ancienneté** avant le départ en retraite pour être prise en compte.

---

## 🧮 Méthodologie de calcul

### Formule de base de la pension
Pension = Traitement indiciaire × 75% × (Trimestres liquidables / Trimestres requis)

### Méthode SRE (base 360 jours/an)

- **1 année = 360 jours**
- **1 mois = 30 jours**
- **1 trimestre = 90 jours**
- **Arrondi final** : ≥45 jours = +1 trimestre

### Rachat de trimestres (Fonction Publique) ⭐ CORRIGÉ V.04.2.5

**Formule :**
Coût = Traitement indiciaire × Coefficient d'âge × Nombre de trimestres

**Coefficients indicatifs (base 2024) :**

| Âge | Option 1 (Taux seul) | Option 2 (Taux + Durée) |
|-----|---------------------|------------------------|
| 20-29 ans | 25-28% | 45-50% |
| 30-39 ans | 28-35% | 50-62% |
| 40-49 ans | 35-48% | 62-85% |
| 50-54 ans | 48-65% | 85-115% |
| 55-59 ans | 65-85% | 115-150% |
| 60+ ans | 85-90% | 150-160% |

**Exemple concret :**
- Âge : 42 ans
- Traitement indiciaire : 2 353 €
- Option 2 (Taux + Durée)
- Coefficient interpolé : ~64%
- Coût par trimestre : 2 353 × 0,64 = **1 506 €**
- Coût 4 trimestres : 1 506 × 4 = **6 024 €**
- Coût réel (TMI 30%) : 6 024 × 0,70 = **4 217 €**

### Pension provisoire (retraite progressive) ⭐ CORRIGÉ V.04.2.4

**Calcul initial (au départ progressif) :**
Pension de référence = Traitement × 75% × (Liquidables au départ / Trimestres requis)
Pension provisoire = Pension de référence × (1 - quotité)

**Si changement de quotité pendant la progressive :**
Nouvelle pension provisoire = Pension de référence × (1 - nouvelle quotité)

**Exemple :**
- Pension de référence : 1 457 €
- Quotité initiale 80% → pension provisoire : 1 457 × 20% = 291 €
- Changement à 70% → nouvelle pension provisoire : 1 457 × 30% = 437 €
- ✅ La pension de référence (1 457 €) ne change pas
- ✅ Seul le pourcentage versé évolue

**À la retraite définitive :**
- Recalcul complet avec TOUS les droits acquis (y compris pendant la progressive)

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

### Exemple 1 : "Dois-je racheter 4 trimestres ?"

**Profil :**
- Âge actuel : 42 ans
- Traitement : 2 353 €
- Trimestres d'assurance : 155 / 172
- TMI : 30%

**Simulation V.04.2.4 (FAUX) :**
- Coût réel : 10 640 €
- Gain mensuel : +86 €
- Rentabilisation : 15 ans
- ❌ **Conclusion erronée** : "Trop cher, pas rentable"

**Simulation V.04.2.5 (CORRECT) :**
- Coût réel : 4 217 €
- Gain mensuel : +86 €
- Rentabilisation : 7,7 ans
- ✅ **Conclusion correcte** : "Rentable si espérance de vie normale"

**Impact de la correction :** Division du coût par ~2,5 → Conclusion complètement différente !

### Exemple 2 : Fonctionnaire avec carrière complète

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

- ⚡ **Chargement instantané** (fichier unique ~110 Ko)
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
├── Coefficients rachat FP (NOUVEAU)
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

// Rachat (NOUVEAU V.04.2.5)
getCoefficientRachat(age, option) // Interpolation coefficients
getCoutRachatParTrimestre(age, option, traitement) // Coût FP

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
V.04.2.5 (Janvier 2025) - Actuelle ⭐

🔴 CORRECTION MAJEURE : Remplacement barèmes secteur privé → coefficients Fonction Publique d'État
✅ Calcul rachat basé sur traitement indiciaire × coefficient d'âge
✅ Interpolation linéaire des coefficients selon l'âge précis
✅ Division du coût par ~2,5 (exemple : 15 200 € → 5 836 €)
✅ Tableau des coefficients dans l'onglet Sources
✅ Avertissements renforcés sur le caractère indicatif

V.04.2.4 (Janvier 2025)

✅ CORRECTION MAJEURE : Documentation pension provisoire (évolution quotité)
✅ Ajout encadré informatif dans Paramètres
✅ Mise à jour onglet Sources
❌ Erreur corrigée en V.04.2.5 : Barèmes rachat incorrects

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
❌ Erreur détectée : Barèmes secteur privé utilisés par erreur

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
 Mise à jour automatique des barèmes rachat

Version 5.0.x (Prévue Q3 2025)

 Application web progressive (PWA)
 Synchronisation cloud optionnelle
 Mode collaboratif (conseiller retraite)


🤝 Remerciements
Ce projet a été rendu possible grâce à :

📚 Documentation officielle du SRE, Service-Public.fr et Légifrance
👥 Retours des utilisateurs fonctionnaires d'État
🐛 Signalements de bugs permettant les corrections (pension provisoire, barèmes rachat)
💡 Suggestions d'amélioration de la communauté

Merci particulier :

Aux utilisateurs qui ont signalé l'inexactitude sur la pension provisoire (V.04.2.4)
À l'utilisateur qui a remarqué que les coûts de rachat étaient "très chers" (V.04.2.5)

Ces retours ont permis des corrections majeures qui améliorent significativement la précision du simulateur !

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

ensap.gouv.fr - Simulation officielle + devis rachat
retraitesdeletat.gouv.fr - SRE
service-public.fr - Retraite progressive
service-public.fr - Rachat de trimestres
info-retraite.fr - Portail commun

Documentation technique

Légifrance - Code des pensions
Décret 2023-799
Décret 2007-262 - Rachat FP
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
Version : V.04.2.5 | Date : Janvier 2025 | Réglementation : Décret n° 2023-799 du 21 août 2023
🔴 Correction critique V.04.2.5 : Barèmes rachat Fonction Publique d'État (coûts divisés par ~2,5)
</div>
```