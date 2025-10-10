# 🧮 Simulateur de Retraite Progressive - Fonctionnaire d'État

[![Version](https://img.shields.io/badge/version-4.2.7-green.svg)](https://github.com/TON_USERNAME/TON_REPO/blob/main/simulateur_retraite_V.04.2.7.html)
[![License](https://img.shields.io/badge/license-Gratuit%20%C3%A9ducatif-blue.svg)](https://github.com/TON_USERNAME/TON_REPO/blob/main/LICENSE)


Un simulateur pédagogique gratuit et transparent pour estimer votre retraite progressive et définitive en tant que fonctionnaire d'État, basé sur la méthode officielle du Service des Retraites de l'État (SRE).

**🎓 Outil éducatif gratuit** - Aucune inscription, aucun paiement, aucune donnée collectée.

---

## 🎯 Objectif

Ce simulateur vous aide à :
- 📊 **Comprendre** les mécanismes de la retraite progressive
- 💰 **Estimer** votre pension selon différents scénarios
- 📈 **Comparer** l'impact des quotités de travail
- 📉 **Analyser** la rentabilité de la surcotisation et du rachat de trimestres
- 🎓 **Apprendre** les règles complexes du régime de retraite des fonctionnaires
- ✅ **Valider** vos données avec 31 contrôles de cohérence

---

## ⚡ Démarrage rapide

### Installation (aucune installation requise !)

1. **Téléchargez** le fichier `simulateur_retraite_V.04.2.7.html`
2. **Double-cliquez** pour l'ouvrir dans votre navigateur
3. **C'est tout !** Aucun serveur, aucune connexion internet nécessaire

### Première utilisation

1. Acceptez les conditions d'utilisation
2. Rendez-vous dans l'onglet **"Paramètres"**
3. Remplissez vos informations à partir de votre relevé de carrière SRE
4. Cliquez sur **"Calculer la simulation"**
5. Consultez vos résultats dans les différents onglets
6. Exportez vos résultats en PDF si souhaité

---

## ✨ Fonctionnalités principales

### 📋 7 onglets complets

| Onglet | Description |
|--------|-------------|
| **Paramètres** | Saisie de vos données personnelles et professionnelles + **31 validations** |
| **Résultats RP** | Simulation détaillée de la retraite progressive + **Export PDF** |
| **Retraite Définitive** | Projection de votre retraite sans période progressive + **Export PDF** |
| **Graphique** | Comparaison visuelle des revenus selon la quotité |
| **Analyse Rachat** | Évaluation de la rentabilité du rachat de trimestres + **Export PDF** |
| **Sources** | Références réglementaires et documentation |
| **Mentions Légales** | Conditions d'utilisation, confidentialité, crédits |

### 🔧 Calculs avancés

- ✅ **Méthode SRE officielle** (base 360 jours/an, arrondi ≥45 jours)
- ✅ **Décote et surcote** (3 types cumulables : classique, parentale, excédentaire)
- ✅ **Bonifications enfants** (avant/après 2004)
- ✅ **Majoration familiale** (10% dès 3 enfants)
- ✅ **Décret n°82-624** (6/7ème pour 80%, 32/35ème pour 90%)
- ✅ **Analyse actuarielle** de la surcotisation (vs placements alternatifs)
- ✅ **Surcote parentale** (Décret 2023-799)
- ✅ **Rachat de trimestres** avec coefficients Fonction Publique d'État

### 📄 Exports PDF professionnels

**3 types d'exports disponibles :**

1. **Export Résultats Retraite Progressive**
   - Paramètres de simulation complets
   - Durées et trimestres détaillés
   - Revenus pendant la progressive
   - Pension définitive estimée
   - Analyses de surcotisation et décote/surcote

2. **Export Retraite Définitive**
   - Projection jusqu'au départ
   - Impact de la quotité choisie
   - Trimestres au départ
   - Pension définitive selon scénario

3. **Export Analyse Rachat**
   - Coût du rachat détaillé
   - Impact sur la pension
   - Comparaison avec placement
   - Recommandation personnalisée

**Caractéristiques techniques :**
- Support natif des accents français par jsPDF 2.5.1
- Format A4 optimisé pour l'impression
- En-têtes et pieds de page professionnels
- Pagination automatique
- Disclaimers et avertissements inclus

### 📊 Outils d'aide à la décision

- 📈 **Graphiques interactifs** (revenus selon quotité, pensions comparées)
- 💡 **Analyses de rentabilité** (surcotisation, rachat de trimestres)
- 💾 **Export/Import** de simulations (format JSON)
- 📄 **Exports PDF** des résultats
- 🎯 **Recommandations personnalisées** selon votre profil

---

## 🆕 Nouveautés V.04.2.7

### ✅ Validation exhaustive des données (AMÉLIORATION MAJEURE)

**31 validations de cohérence implémentées :**

**Onglet Paramètres (22 validations) :**
1. **Dates (9 validations)** :
   - Messages d'erreur avec basculement automatique vers l'onglet Résultats
   - Date relevé > date départ progressif
   - Date départ progressif > date départ définitif
   - Date naissance avant 1900 (irréaliste)
   - Dates dans futur lointain (2080+)
   - Âge actuel > 80 ans (inhabituel)
   - Âge actuel < 40 ans (trop jeune pour retraite progressive)
   - Âge départ progressif > 80 ans (irréaliste)
   - Départ après 67-70 ans (prolongation/limite)

2. **Trimestres/Jours (4 validations)** :
   - Trimestres incohérents vs années de carrière (ex: 160 trim pour 12 ans)
   - Jours négatifs (assurance + liquidables)
   - Jours >= 90 (90 jours = 1 trimestre)
   - Total jours liquidables > total jours assurance

3. **Indices/Valeurs (3 validations)** :
   - Indice hors plage réaliste (350-900 pour FP État)
   - Valeur point incorrecte (4.5-5.5€, officiel : 4.92278€)
   - Trimestres requis aberrants (150-180)

4. **Enfants (4 validations + UX améliorée)** :
   - Case cochée + 0 enfants saisis
   - Enfants saisis sans case cochée
   - Total ≠ somme (avant 2004 + après 2003)
   - Champs grisés automatiquement si case non cochée

5. **Durée période progressive (2 validations)** :
   - Période < 1 mois (warning)
   - Période > 5 ans (warning)

**Onglet Retraite Définitive (9 validations) :**
- ✅ Données récupérées du simulateur
- ✅ Date départ obligatoire
- ✅ Date départ > date relevé
- ✅ Date pas dans le passé (> 1 mois)
- ✅ Date pas dans futur lointain (< 20 ans)
- ✅ Âge au départ (60-80 ans + warnings 67-70)
- ✅ Quotité valide (0-1)
- ✅ Surcotisation + 100% interdit (basé sur textes officiels)
- ✅ Durée période projection cohérente

### 🎨 Améliorations UX

**Messages d'erreur pédagogiques :**
- Affichage clair avec icônes (❌ ⚠️ ℹ️)
- Citations réglementaires quand pertinent
- Basculement automatique vers l'onglet Résultats lors d'erreurs
- Suggestions d'actions correctives

**Message informatif intelligent :**
- Si liquidables < assurance dans Retraite Définitive
- Suggère automatiquement l'onglet "Analyse Rachat"
- Calcule l'écart et informe l'utilisateur

### 🔧 Corrections techniques

**Validation quotité progressive :**
- AVANT : Erreur si quotité pendant >= quotité avant (trop restrictif)
- APRÈS : Validation supprimée (augmentation autorisée selon FAQ DGAFP)

**Bug syntaxe enfants :**
- Problème : Double accolade `});}); `empêchait l'initialisation
- Correction : Une seule accolade `});`

**Surcotisation à 100% :**
- Recherche réglementaire faite (Code des pensions, SRE, CNRACL)
- Validation ajoutée avec message pédagogique
- Distinction claire : Surcotisation = PENDANT temps partiel / Rachat = APRÈS

---

## 📚 Documentation

### Mode d'emploi complet

Consultez le fichier MODE_EMPLOI.md pour :
- Guide détaillé de chaque onglet
- Explications des calculs
- Guide des exports PDF
- Cas d'usage concrets
- FAQ complète
- Conseils stratégiques

### Sources réglementaires

Le simulateur s'appuie sur :

| Texte | Description |
|-------|-------------|
| Code des pensions civiles et militaires | Articles L11 à L18, L89 bis à L89 ter, L9 |
| Décret n°2023-799 (21/08/2023) | Surcote parentale (1,25% par trimestre, max 5%) |
| Décret n°82-624 (20/07/1982) | Temps partiel (6/7ème et 32/35ème) |
| Décret n°2007-262 (27/02/2007) | Rachat de trimestres fonction publique |
| Loi n°2023-270 (14/04/2023) | Réforme des retraites 2023 |
| Arrêté du 23/06/2023 | Valeur du point d'indice (4,92278 €) |

Sources officielles consultées :
- [Service des Retraites de l'État](https://retraitesdeletat.gouv.fr)
- [Service-Public.fr - Retraite progressive](https://www.service-public.fr/particuliers/vosdroits/F37400)
- [Service-Public.fr - Rachat](https://www.service-public.fr/particuliers/vosdroits/F13243)
- [CNRACL](https://www.cnracl.retraites.fr)
- [Code des pensions (Légifrance)](https://www.legifrance.gouv.fr/codes/id/LEGITEXT000006070302/)

---

## ⚠️ Avertissements importants

### Non-opposabilité

| ❌ Ce simulateur | ✅ Simulateur officiel SRE/ENSAP |
|------------------|----------------------------------|
| Aide à la décision | **Seul résultat opposable** |
| Transparence pédagogique | **Calcul exact mais opaque** |
| Écart possible 1-2% | **Référence légale** |

➡️ **Pour une estimation officielle définitive, consultez toujours ensap.gouv.fr**

### Écart connu - Calcul de la pension

Un écart de **1 à 2 trimestres liquidables** (~1-2% de pension) peut exister avec le calcul officiel du SRE, probablement dû à des règles d'arrondi internes non documentées publiquement.

Le simulateur applique rigoureusement la méthode SRE documentée.

### Rachat de trimestres - Coefficients indicatifs

**Important** : Les coefficients utilisés pour le rachat sont indicatifs (base 2024, catégorie sédentaire). Le coût exact dépend de nombreux paramètres :
- Votre traitement indiciaire au moment du rachat
- Votre catégorie (sédentaire, actif, insalubre)
- Les barèmes en vigueur à la date du rachat

**Pour un devis personnalisé et opposable, contactez toujours le SRE via ensap.gouv.fr**

### Règle des six mois

Une augmentation d'indice majoré doit avoir ≥ 6 mois d'ancienneté avant le départ en retraite pour être prise en compte.

---

## 🧮 Méthodologie de calcul

### Formule de base de la pension
Pension = Traitement indiciaire × 75% × (Trimestres liquidables / Trimestres requis)

### Méthode SRE (base 360 jours/an)

- 1 année = 360 jours
- 1 mois = 30 jours
- 1 trimestre = 90 jours
- Arrondi final : ≥45 jours = +1 trimestre

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

### Exports PDF - Support natif des accents

**V.04.2.6+ - Amélioration majeure :**
- jsPDF 2.5.1 supporte nativement tous les accents français
- Plus besoin de conversion ou fonction spéciale
- Accents parfaitement préservés dans les PDFs
- Compatible tous systèmes

---

## 💻 Aspects techniques

### Technologies utilisées

- **HTML5** : Structure de l'application
- **CSS3** : Interface responsive et moderne
- **JavaScript (Vanilla)** : Logique métier et calculs
- **Chart.js 4.4.1** : Visualisations graphiques
- **jsPDF 2.5.1** : Génération des exports PDF

### Compatibilité

| Navigateur | Version minimale | Support |
|------------|------------------|---------|
| Chrome | 90+ | ✅ Complet |
| Firefox | 88+ | ✅ Complet |
| Safari | 14+ | ✅ Complet |
| Edge | 90+ | ✅ Complet |

### Performances

- ⚡ Chargement instantané (fichier unique ~130 Ko)
- 🔒 100% local (aucune donnée transmise)
- 💾 Pas de base de données requise
- 📱 Responsive (mobile, tablette, desktop)

### Architecture
simulateur.html
├── Structure HTML
│   ├── 7 onglets (tabs)
│   ├── Formulaires de saisie
│   └── Zones d'affichage des résultats
├── Styles CSS
│   ├── Design moderne
│   ├── Mode responsive
│   └── Thème vert (fonctionnaire)
└── Logique JavaScript
├── Calculs SRE (base 360j/an)
├── Analyses actuarielles
├── Coefficients rachat FP (CORRIGÉ)
├── Génération de graphiques
├── Exports PDF natifs (V.04.2.6)
├── Export/Import JSON
└── Validations exhaustives (V.04.2.7) ⭐ NOUVEAU

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

// Rachat (CORRIGÉ V.04.2.5)
getCoefficientRachat(age, option) // Interpolation coefficients
getCoutRachatParTrimestre(age, option, traitement) // Coût FP

// Analyses
calculerRentabiliteSurcotisation(...)
analyserRachat()

// Validations (NOUVEAU V.04.2.7) ⭐
validerParametres() // 22 validations onglet Paramètres
validerParametresDefinitive() // 9 validations onglet Retraite Définitive

// Exports PDF (V.04.2.6 - Support natif)
exporterResultatsPDF()
exporterRetraiteDefinitivePDF()
exporterAnalyseRachatPDF()

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


📜 Historique des versions
V.04.2.7 (Octobre 2025) - Actuelle ⭐
Améliorations majeures :

✅ 31 validations de cohérence implémentées (22 Paramètres + 9 Retraite Définitive)
✅ Messages d'erreur pédagogiques avec basculement automatique
✅ Validation dates, trimestres, indices, enfants, quotités
✅ Message informatif si liquidables < assurance (suggère onglet Rachat)
✅ Bug syntaxe enfants corrigé
✅ Validation surcotisation + 100% ajoutée
✅ UX améliorée : champs grisés automatiquement

Corrections techniques :

Validation quotité progressive supprimée (trop restrictive)
Double accolade });});  corrigée en });
Distinction claire surcotisation vs rachat

V.04.2.6 (Octobre 2025)
Améliorations majeures :

✅ Support natif des accents par jsPDF 2.5.1 (plus de conversion nécessaire)
✅ Avertissements renforcés partout (bannière rouge, PDF, footer)
✅ Phase de validation en cours documentée correctement
✅ Mentions légales complètes avec développement Claude (Anthropic)
✅ Protection juridique maximale (ensap.gouv.fr répété, disclaimers clairs)
✅ Correction toutes les dates : Octobre 2025
✅ Modèle 100% gratuit confirmé

V.04.2.5 (Janvier 2025)

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

Versions antérieures

V.04.2.x (2024) : Amélioration interface utilisateur
V.04.1.x (2024) : Ajout onglet "Analyse Rachat" (barèmes erronés)
V.04.0.x (2023) : Intégration Décret 2023-799 (surcote parentale)


📋 Roadmap
Version 4.2.8 (Prévue Q4 2025)

☐ Validation onglet Graphique
☐ Tests finaux de tous les onglets
☐ Documentation complète des cas limites

Version 4.3.x (Prévue Q1 2026)

☐ Ajout de scenarios "what-if" multiples
☐ Mode sombre
☐ Comparaison côte à côte de 2 simulations
☐ Amélioration exports PDF (graphiques inclus)

Version 4.4.x (Prévue Q2 2026)

☐ Intégration des régimes spéciaux
☐ Calculateur de pension de réversion
☐ Mise à jour automatique des barèmes rachat


🤗 Remerciements
Ce projet a été rendu possible grâce à :

📚 Documentation officielle du SRE, Service-Public.fr et Légifrance
🤖 Collaboration technique avec Claude (Anthropic)
👥 Retours des utilisateurs fonctionnaires d'État
🐛 Signalements de bugs permettant les corrections majeures
💡 Suggestions d'amélioration de la communauté

Merci particulier :

Aux utilisateurs qui ont signalé l'inexactitude sur la pension provisoire (V.04.2.4)
À l'utilisateur qui a remarqué que les coûts de rachat étaient "très chers" (V.04.2.5)
Aux beta-testeurs qui ont identifié les incohérences de saisie (V.04.2.7)

Ces retours ont permis des corrections majeures qui améliorent significativement la précision et la robustesse du simulateur !

📄 Licence
Usage gratuit à des fins informatives et pédagogiques.
Clause de non-responsabilité :

Ce simulateur est fourni "tel quel" sans garantie
Les résultats sont des estimations
Seuls les calculs officiels du SRE font foi
L'éditeur ne peut être tenu responsable des décisions prises sur la base de ces estimations

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
📢 Partager avec vos collègues
💬 Laisser un commentaire
🐛 Signaler des bugs
💡 Proposer des améliorations


<p align="center">
  <strong>Simulateur de Retraite Progressive V.04.2.7</strong><br>
  Développé avec Claude (Anthropic)<br>
  Dernière mise à jour : Octobre 2025
</p>
<p align="center">
  <em>Ce simulateur ne remplace pas les outils officiels de l'État</em><br>
  <strong>Pour une estimation officielle : <a href="https://ensap.gouv.fr">ensap.gouv.fr</a></strong>
</p>
```

