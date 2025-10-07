# 🧮 Simulateur de Retraite Progressive - Fonctionnaire d'État

---

📌 **Informations clés**

- 🔢 Version actuelle : V.04.2.6 (Octobre 2025)
- 📚 Réglementation : Décrets 2023-799, 82-624, 2007-262 + Code des pensions

---
[![Version](https://img.shields.io/badge/version-V.04.2.6-blue)](COMMITS.md)
[![Licence](https://img.shields.io/badge/licence-CC--BY--NC--SA%204.0-lightgrey)](LICENCE.txt)



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

---

## ⚡ Démarrage rapide

### Installation (aucune installation requise !)

1. **Téléchargez** le fichier `simulateur_retraite_V.04.2.6.html`
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
| **Paramètres** | Saisie de vos données personnelles et professionnelles |
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

## 🆕 Nouveautés V.04.2.6

### 📄 Exports PDF natifs (AMÉLIORATION MAJEURE)

**Support natif des accents français :**
- jsPDF 2.5.1 gère nativement tous les caractères accentués
- Plus besoin de fonction de conversion
- PDFs parfaitement lisibles avec accents préservés
- Compatible tous systèmes (Windows, Mac, Linux, mobile)

**Intégration :**
- 3 boutons d'export dans les onglets Résultats, Retraite Définitive et Analyse Rachat
- Génération automatique avec jsPDF 2.5.1
- Avertissements renforcés en première page de chaque PDF

### 🛡️ Protection juridique renforcée

**Avertissements présents partout :**
- ✅ Bannière de consentement avec encadré rouge
- ✅ "Ne remplace pas les outils officiels" explicite
- ✅ Mention ensap.gouv.fr répétée minimum 2× par page
- ✅ Première page de chaque export PDF
- ✅ Footer du site
- ✅ Onglet Mentions Légales complet

**Stratégie adoptée :**
- Transparence maximale = protection juridique
- Toujours rediriger vers les sites officiels
- Documenter l'écart 1-2 trimestres partout
- Déclaration claire de responsabilité limitée

### 🧪 Phase de validation en cours

**Approche beta test :**
- Recrutement de 10-15 fonctionnaires testeurs
- Comparaison systématique avec ENSAP
- Documentation des écarts observés
- Amélioration continue basée sur les retours

**Mention correcte :**
- "Phase de validation en cours" (véridique)
- Au lieu de "testé par X fonctionnaires" (prématuré)

---

## 🔴 CORRECTION MAJEURE - Rachat de trimestres (V.04.2.5)

### ✅ Remplacement complet des barèmes de rachat

Les barèmes utilisés dans les versions précédentes étaient ceux du régime général (secteur privé), ce qui donnait des coûts 2 à 3 fois trop élevés pour les fonctionnaires d'État !

### ❌ Ancienne méthode (V.04.2.4 et antérieures)

Barèmes fixes secteur privé :
- 40 ans, Option 2 : 7 600 € par trimestre
- 50 ans, Option 2 : 11 200 € par trimestre
- Exemple : 4 trimestres à 40 ans = **15 200 €** (FAUX)

### ✅ Nouvelle méthode (V.04.2.5+)

Coefficient Fonction Publique × Traitement indiciaire :
- 40 ans, Option 2 : ~62% du traitement
- Traitement 2 353 € × 0,62 = 1 459 € par trimestre
- Exemple : 4 trimestres à 40 ans = **5 836 €** (CORRECT)

### 📊 Comparaison des résultats

| Critère | V.04.2.4 (FAUX) | V.04.2.5+ (CORRECT) | Différence |
|---------|-----------------|---------------------|------------|
| Coût 4 trim. (40 ans, Opt. 2) | 15 200 € | 5 836 € | **-9 364 € (-62%)** |
| Coût réel (TMI 30%) | 10 640 € | 4 085 € | **-6 555 € (-62%)** |
| Durée rentabilisation | 15-20 ans | 7-10 ans | **÷ 2** |

---

## 🤝 Développement et validation

### Collaboration avec Claude (Anthropic)

Ce simulateur a été développé en collaboration avec Claude, l'assistant IA d'Anthropic, pour les aspects :

- **Algorithmiques** : Implémentation rigoureuse des calculs SRE conformes aux textes réglementaires
- **Techniques** : Architecture du code, gestion des exports PDF, optimisation
- **Réglementaires** : Interprétation et application des décrets et du Code des pensions
- **Légaux** : Rédaction des mentions légales, CGU, disclaimers adaptés au modèle gratuit
- **Documentaires** : Rédaction du mode d'emploi et de la documentation technique

L'éditeur assume l'entière responsabilité du contenu, de l'exactitude des calculs et de la conformité réglementaire.

### Approche de validation

**Modèle gratuit et éducatif :**
- Outil mis à disposition gratuitement sans aucune contrepartie
- Vocation pédagogique : comprendre les mécanismes, pas remplacer les outils officiels
- Transparence totale sur les calculs et les limitations

**Validation par beta testeurs :**
- 10-15 fonctionnaires testant leurs cas réels
- Comparaison systématique avec simulations ENSAP officielles
- Documentation des écarts et amélioration continue

🧠 Origine du code

Ce simulateur a été conçu par Jean-Michel, avec l’assistance de l’intelligence artificielle Claude (Anthropic) pour la génération du code source. Toutes les directives, validations, structures, calculs et contenus réglementaires ont été définis par l’auteur humain, qui assume l’entière responsabilité du projet.

📄 Licence

🔹 **Résumé rapide** : usage libre à des fins pédagogiques, attribution requise, usage commercial interdit sans autorisation.

Ce simulateur est mis à disposition sous la licence Creative Commons BY-NC-SA 4.0.

Vous êtes libre de :
- Partager — copier, distribuer et transmettre l’œuvre
- Adapter — remixer, transformer et créer à partir de l’œuvre

Sous les conditions suivantes :
- Attribution — vous devez créditer l’auteur (Jean-Michel), fournir un lien vers la licence, et indiquer si des modifications ont été effectuées.
- Pas d’utilisation commerciale — vous ne pouvez pas utiliser cette œuvre à des fins commerciales sans autorisation écrite.
- Partage dans les mêmes conditions — si vous modifiez l’œuvre, vous devez la distribuer sous la même licence.

🔗 [Texte officiel de la licence](https://creativecommons.org/licenses/by-nc-sa/4.0/deed.fr)

[![Licence CC BY-NC-SA 4.0](https://licensebuttons.net/l/by-nc-sa/4.0/88x31.png)](https://creativecommons.org/licenses/by-nc-sa/4.0/)
---

📘 **Journal technique des versions**

Ce simulateur évolue régulièrement pour intégrer les dernières règles et améliorer la lisibilité.

🔹 Consultez le fichier [`COMMITS.md`](COMMITS.md) pour découvrir les ajouts, corrections et évolutions par version.

---

[![Journal technique des versions](https://img.shields.io/badge/COMMITS.md-Historique%20structur%C3%A9-blue)](COMMITS.md)


**Écart documenté avec le SRE :**
- Écart connu de 1-2 trimestres liquidables (~1-2% de pension)
- Cause probable : règles d'arrondi internes non documentées publiquement
- Le simulateur applique rigoureusement la méthode SRE documentée
- Pour une estimation officielle définitive : toujours consulter ensap.gouv.fr

### Démarche qualité

- ✅ Application stricte des textes réglementaires
- ✅ Corrections rapides suite aux retours utilisateurs
- ✅ Documentation exhaustive des sources
- ✅ Transparence sur les limitations
- ✅ Disclaimers clairs et visibles
- ✅ Aucune collecte de données personnelles

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

**V.04.2.6 - Amélioration majeure :**
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

- ⚡ Chargement instantané (fichier unique ~120 Ko)
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

// Rachat (CORRIGÉ V.04.2.5)
getCoefficientRachat(age, option) // Interpolation coefficients
getCoutRachatParTrimestre(age, option, traitement) // Coût FP

// Analyses
calculerRentabiliteSurcotisation(...)
analyserRachat()

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


## 📘 Changelog pédagogique

Ce changelog résume les évolutions majeures du simulateur par version. Pour le journal technique complet, voir [`COMMITS.md`](COMMITS.md).

V.04.2.6 (Octobre 2025) - Actuelle ⭐

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
Version 4.3.x (Prévue Q1 2026)

☐ Ajout de scenarios "what-if" multiples
☐ Mode sombre
☐ Comparaison côte à côte de 2 simulations
☐ Amélioration exports PDF (graphiques inclus)

Version 4.4.x (Prévue Q2 2026)

☐ Intégration des régimes spéciaux
☐ Calculateur de pension de réversion
☐ Mise à jour automatique des barèmes rachat

## 🗂️ Structure documentaire

Ce dépôt contient plusieurs fichiers complémentaires, chacun avec un rôle précis :

| Fichier          | Rôle principal                                                  | Public cible               |
|------------------|------------------------------------------------------------------|----------------------------|
| `README.md`       | Présentation générale, guide rapide, changelog pédagogique      | Utilisateurs               |
| `COMMITS.md`      | Journal technique structuré des commits par version             | Développeurs, auditeurs    |
| `MODE_EMPLOI.md`  | Guide détaillé de chaque onglet, calculs et exports             | Utilisateurs avancés       |
| `LICENCE.txt`     | Texte officiel de la licence Creative Commons BY-NC-SA 4.0      | Tous publics               |
| `simulateur_retraite_V.04.2.6.html` | Version actuelle du simulateur, en usage local ou web | Utilisateurs               |

🔹 Pour comprendre les évolutions du simulateur, consultez le changelog pédagogique dans le README.  
🔹 Pour une traçabilité technique complète, voir [`COMMITS.md`](COMMITS.md).  
🔹 Pour les calculs et paramètres détaillés, voir [`MODE_EMPLOI.md`](MODE_EMPLOI.md).


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

Ces retours ont permis des corrections majeures qui améliorent significativement la précision du simulateur !

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
  <strong>Simulateur de Retraite Progressive V.04.2.6</strong><br>
  Développé avec Claude (Anthropic)<br>
  Dernière mise à jour : Octobre 2025
</p>
<p align="center">
  <em>Ce simulateur ne remplace pas les outils officiels de l'État</em><br>
  <strong>Pour une estimation officielle : <a href="https://ensap.gouv.fr">ensap.gouv.fr</a></strong>
</p>
```


FIN DU README.md V.04.2.6

