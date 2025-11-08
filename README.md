
README.md mis à jour pour V.04.2.8
🧮 Simulateur de Retraite Progressive - Fonctionnaire d'État
[![Version](https://img.shields.io/badge/version-4.2.8-green.svg)](https://github.com/J34NMY/simulateur-retraite-progressive/blob/main/simulateur_retraite_V.04.2.8.html)
[![License](https://img.shields.io/badge/license-Gratuit%20%C3%A9ducatif-blue.svg)](https://github.com/J34NMY/simulateur-retraite-progressive/blob/main/LICENSE)
Un simulateur pédagogique gratuit et transparent pour estimer votre retraite progressive et définitive en tant que fonctionnaire d'État, basé sur la méthode officielle du Service des Retraites de l'État (SRE).
🎓 Outil éducatif gratuit - Aucune inscription, aucun paiement, aucune donnée collectée.

🎯 Objectif
Ce simulateur vous aide à :

📊 Comprendre les mécanismes de la retraite progressive
💰 Estimer votre pension selon différents scénarios
📈 Comparer l'impact des quotités de travail
📉 Analyser la rentabilité de la surcotisation et du rachat de trimestres
🎓 Apprendre les règles complexes du régime de retraite des fonctionnaires
✅ Valider vos données avec 31 contrôles de cohérence renforcés


⚡ Démarrage rapide
Installation (aucune installation requise !)

Téléchargez le fichier simulateur_retraite_V.04.2.8.html
Double-cliquez pour l'ouvrir dans votre navigateur
C'est tout ! Aucun serveur, aucune connexion internet nécessaire

Première utilisation

Acceptez les conditions d'utilisation
Rendez-vous dans l'onglet "Paramètres"
Remplissez vos informations à partir de votre relevé de carrière SRE
Cliquez sur "Calculer la simulation"
Consultez vos résultats dans les différents onglets
Exportez vos résultats en PDF si souhaité


✨ Fonctionnalités principales
📋 7 onglets complets
OngletDescriptionParamètresSaisie de vos données personnelles et professionnelles + 31 validations renforcéesRésultats RPSimulation détaillée de la retraite progressive + Export PDFRetraite DéfinitiveProjection de votre retraite sans période progressive + Export PDFGraphiqueComparaison visuelle des revenus selon la quotitéAnalyse RachatÉvaluation de la rentabilité du rachat de trimestres + Export PDFSourcesRéférences réglementaires et documentationMentions LégalesConditions d'utilisation, confidentialité, crédits
🔧 Calculs avancés

✅ Méthode SRE officielle (base 360 jours/an, arrondi ≥45 jours)
✅ Décote et surcote (3 types cumulables : classique, parentale, excédentaire)
✅ Bonifications enfants (avant/après 2004)
✅ Majoration familiale (10% dès 3 enfants)
✅ Décret n°82-624 (6/7ème pour 80%, 32/35ème pour 90%)
✅ Analyse actuarielle de la surcotisation (vs placements alternatifs)
✅ Surcote parentale (Décret 2023-799)
✅ Rachat de trimestres avec coefficients Fonction Publique d'État

📄 Exports PDF professionnels
3 types d'exports disponibles :

Export Résultats Retraite Progressive

Paramètres de simulation complets
Durées et trimestres détaillés
Revenus pendant la progressive
Pension définitive estimée
Analyses de surcotisation et décote/surcote


Export Retraite Définitive

Projection jusqu'au départ
Impact de la quotité choisie
Trimestres au départ
Pension définitive selon scénario


Export Analyse Rachat

Coût du rachat détaillé
Impact sur la pension
Comparaison avec placement
Recommandation personnalisée



Caractéristiques techniques :

Support natif des accents français par jsPDF 2.5.1
Format A4 optimisé pour l'impression
En-têtes et pieds de page professionnels
Pagination automatique
Disclaimers et avertissements inclus

📊 Outils d'aide à la décision

📈 Graphiques interactifs (revenus selon quotité, pensions comparées)
💡 Analyses de rentabilité (surcotisation, rachat de trimestres)
💾 Export/Import de simulations (format JSON)
📄 Exports PDF des résultats
🎯 Recommandations personnalisées selon votre profil


🆕 Nouveautés V.04.2.8
✅ Améliorations de la validation des données (CORRECTIONS CRITIQUES)
Corrections majeures apportées :

Validation date de naissance optimisée :

✅ Messages d'erreur plus clairs et hiérarchisés
✅ Distinction entre erreurs critiques et warnings
✅ Détection des dates irréalistes (avant 1900, après 2080)
✅ Validation âge actuel (18-80 ans avec messages adaptés)
✅ Meilleure détection des erreurs de saisie


Validation dates de départ améliorée :

✅ Priorisation des messages d'erreur (dates irréalistes avant âges)
✅ Messages plus précis pour départs après 67-70 ans
✅ Détection des erreurs de saisie (dates futures lointaines)
✅ Validation cohérence temporelle renforcée


Validation trimestres et jours :

✅ Contrôle des valeurs négatives
✅ Vérification jours < 90 (règle SRE)
✅ Cohérence liquidables ≤ assurance
✅ Messages d'erreur plus explicites


Validation indices et valeurs :

✅ Plages réalistes pour indice majoré (350-900)
✅ Plage réaliste pour valeur du point (4.5-5.5€)
✅ Validation trimestres requis (150-180)


Validation enfants renforcée :

✅ Détection incohérence case cochée / nombre saisi
✅ Validation somme totale enfants
✅ Messages pédagogiques clairs


Onglet Retraite Définitive :

✅ 9 validations spécifiques
✅ Gestion des warnings vs erreurs bloquantes
✅ Messages adaptés au contexte



🎨 Améliorations UX
Interface utilisateur :

✅ Messages d'erreur hiérarchisés (❌ critique, ⚠️ warning, ℹ️ info)
✅ Basculement automatique vers l'onglet Résultats en cas d'erreur
✅ Affichage des warnings n'empêchant pas le calcul
✅ Suggestions d'actions correctives
✅ Messages pédagogiques avec contexte réglementaire

🔧 Corrections techniques
Optimisations du code :

✅ Fonction validerParametres() restructurée et optimisée
✅ Fonction validerParametresDefinitive() corrigée
✅ Meilleure gestion des cas limites
✅ Logique de validation plus robuste
✅ Performance améliorée


📚 Documentation
Mode d'emploi complet
Consultez le fichier MODE_EMPLOI.md pour :

Guide détaillé de chaque onglet
Explications des calculs
Guide des exports PDF
Cas d'usage concrets
FAQ complète
Conseils stratégiques

Sources réglementaires
Le simulateur s'appuie sur :
TexteDescriptionCode des pensions civiles et militairesArticles L11 à L18, L89 bis à L89 ter, L9Décret n°2023-799 (21/08/2023)Surcote parentale (1,25% par trimestre, max 5%)Décret n°82-624 (20/07/1982)Temps partiel (6/7ème et 32/35ème)Décret n°2007-262 (27/02/2007)Rachat de trimestres fonction publiqueLoi n°2023-270 (14/04/2023)Réforme des retraites 2023Arrêté du 23/06/2023Valeur du point d'indice (4,92278 €)
Sources officielles consultées :

Service des Retraites de l'État
Service-Public.fr - Retraite progressive
Service-Public.fr - Rachat
CNRACL
Code des pensions (Légifrance)


⚠️ Avertissements importants
Non-opposabilité
❌ Ce simulateur✅ Simulateur officiel SRE/ENSAPAide à la décisionSeul résultat opposableTransparence pédagogiqueCalcul exact mais opaqueÉcart possible 1-2%Référence légale
➡️ Pour une estimation officielle définitive, consultez toujours ensap.gouv.fr
Écart connu - Calcul de la pension
Un écart de 1 à 2 trimestres liquidables (~1-2% de pension) peut exister avec le calcul officiel du SRE, probablement dû à des règles d'arrondi internes non documentées publiquement.
Le simulateur applique rigoureusement la méthode SRE documentée.
Rachat de trimestres - Coefficients indicatifs
Les coefficients de rachat sont indicatifs (base 2024, catégorie sédentaire). Demandez toujours un devis officiel au SRE via ensap.gouv.fr avant de prendre une décision.

💻 Technologies utilisées
Stack technique

HTML5 - Structure sémantique
CSS3 - Design moderne et responsive
JavaScript Vanilla - Aucune dépendance framework
Chart.js 4.4.1 - Graphiques interactifs
jsPDF 2.5.1 - Export PDF natif avec support accents

Performance

⚡ Chargement instantané (fichier unique ~158 Ko)
🔒 100% local (aucune donnée transmise)
💾 Pas de base de données requise
📱 Responsive (mobile, tablette, desktop)

Architecture
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
    └── Validations exhaustives (V.04.2.8) ⭐ AMÉLIORÉES

🔧 Développement
Structure du code
Fonctions principales :
javascript// Calculs de base
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

// Validations (AMÉLIORÉES V.04.2.8) ⭐
validerParametres() // 22 validations onglet Paramètres - OPTIMISÉES
validerParametresDefinitive() // 9 validations onglet Retraite Définitive - CORRIGÉES

// Exports PDF (V.04.2.6 - Support natif)
exporterResultatsPDF()
exporterRetraiteDefinitivePDF()
exporterAnalyseRachatPDF()

// Interface
switchTab(tabName)
updateChart(...)
exporterParams()
importerParams()
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
V.04.2.8 (Novembre 2025) - Actuelle ⭐
Corrections critiques de la validation :
✅ Validation date de naissance optimisée :

Messages d'erreur hiérarchisés (critiques vs warnings)
Détection dates irréalistes (avant 1900, après 2080)
Validation âge actuel améliorée
Meilleure expérience utilisateur

✅ Validation dates de départ améliorée :

Priorisation des erreurs (dates irréalistes → âges → règles)
Messages plus précis et pédagogiques
Détection améliorée des erreurs de saisie

✅ Validations trimestres et indices :

Contrôles renforcés (négatifs, plages réalistes)
Messages d'erreur plus explicites
Cohérence assurance/liquidables vérifiée

✅ Onglet Retraite Définitive :

9 validations corrigées et optimisées
Gestion warnings vs erreurs bloquantes
Messages adaptés au contexte

Améliorations techniques :

Code de validation restructuré et optimisé
Performance améliorée
Gestion robuste des cas limites

V.04.2.7 (Octobre 2025)
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
Double accolade });}); corrigée en });
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
Version 4.2.9 (Prévue Q1 2026)
☐ Tests approfondis de tous les scénarios de validation
☐ Amélioration messages d'erreur encore plus pédagogiques
☐ Documentation complète des cas limites
Version 4.3.x (Prévue Q2 2026)
☐ Ajout de scenarios "what-if" multiples
☐ Mode sombre
☐ Comparaison côte à côte de 2 simulations
☐ Amélioration exports PDF (graphiques inclus)
Version 4.4.x (Prévue Q3 2026)
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
Aux testeurs qui ont remonté les problèmes de validation (V.04.2.8)

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
  <strong>Simulateur de Retraite Progressive V.04.2.8</strong><br>
  Développé avec Claude (Anthropic)<br>
  Dernière mise à jour : Novembre 2025
</p>
<p align="center">
  <em>Ce simulateur ne remplace pas les outils officiels de l'État</em><br>
  <strong>Pour une estimation officielle : <a href="https://ensap.gouv.fr">ensap.gouv.fr</a></strong>
</p>

