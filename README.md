🇫🇷 Simulateur de Retraite Progressive - Fonctionnaire d'État
Afficher l'image
Afficher l'image
Afficher l'image
Afficher l'image
📋 Description
Simulateur en ligne gratuit et open source permettant aux fonctionnaires d'État français (affiliés au SRE - Service des Retraites de l'État) d'estimer leur pension de retraite progressive et définitive selon la réglementation en vigueur.
🎯 Objectif principal : Fournir un outil décisionnel transparent et pédagogique pour planifier votre fin de carrière en toute connaissance de cause.

✨ Fonctionnalités Principales
🧮 Calcul de la Pension

Simulation de retraite progressive avec calcul précis selon la méthode SRE (base 360 jours/an)
⭐ NOUVEAU V.04.2.3 : Simulateur de Retraite Définitive

Onglet dédié pour simuler directement une retraite définitive sans passer par la retraite progressive
Récupération automatique des données depuis l'onglet Paramètres
Projection simple avec une seule période et quotité fixe
Graphique comparatif en barres des différentes quotités
Analyse de surcotisation vs placement alternatif


Formule transparente :

Pension = Traitement indiciaire × 75% × (Trimestres liquidables / Trimestres requis)


Option Décret n°82-624 (6/7ème et 32/35ème)

Case à cocher pour appliquer ou non le décret du 20 juillet 1982
Quotité 80% → Rémunération à 6/7ème (≈85,71%)
Quotité 90% → Rémunération à 32/35ème (≈91,43%)
Tooltip explicative pour vérifier l'applicabilité sur votre fiche de paie
Option cochée par défaut (cas majoritaire)


Prise en compte automatique : décote, surcotes cumulables, majorations familiales
Calcul des revenus durant la période de retraite progressive (traitement + pension provisoire)

📊 Analyses Décisionnelles
1. Analyse de Surcotisation

Calcul du coût mensuel et total de la surcotisation
Comparaison avec placements alternatifs (Livret A, LEP, placements dynamiques)
Durée pour rentabiliser l'investissement calculée avec données actuarielles INSEE 2024
Recommandation personnalisée (FAVORABLE / NEUTRE / DÉFAVORABLE)
Disponible dans les deux modes : Retraite Progressive et Retraite Définitive

2. Analyse de Rachat de Trimestres

Simulation du coût selon l'âge et l'option choisie (Taux seul / Taux + Durée)
Calcul de l'économie d'impôt (déductibilité fiscale)
Impact réel sur la pension (évitement décote / augmentation liquidables)
Comparaison rachat vs placement alternatif
Récupération automatique des données du simulateur principal

🎨 Interface Utilisateur

6 onglets intuitifs : Paramètres, Résultats RP, Retraite Définitive ⭐ Nouveau, Graphique, Analyse Rachat, Sources
Graphiques comparatifs :

Graphique en ligne pour la retraite progressive (revenus pendant la période)
Graphique en barres pour la retraite définitive (pension finale selon quotité)


Tooltips informatifs sur chaque paramètre complexe (positionnement optimisé)
Import/Export JSON pour sauvegarder et partager vos simulations
Design responsive : fonctionne sur desktop, tablette et mobile

📚 Fonctionnalités Avancées

Bonifications pour enfants (avant 2004 : 4 trimestres liquidables par enfant)
Majorations de durée d'assurance (après 2003 : 2 trimestres assurance par enfant)
Trois types de surcotes cumulables :

Surcote classique : 1,25% par trimestre au-delà de l'âge légal
Surcote parentale : 1,25% par trimestre liquidable l'année précédant l'âge légal (max 5%)
Majoration excédentaire : 1,25% par trimestre excédentaire restant


Majoration familiale : 10% pour 3 enfants + 5% par enfant supplémentaire
Règle des six mois : prise en compte des augmentations d'indice


⚖️ Avertissement Important : Non-Opposabilité
⚠️ Cet outil n'est PAS OFFICIEL
AspectCe SimulateurSimulateur Officiel SRE/ENSAPValeurAide à la décision, pédagogie, vérificationRéférence légale et administrative uniqueOpposabilitéNulle - Aucune valeur juridiqueMaximale - Seul résultat opposablePrécisionÉcart potentiel de 1-2 trimestres liquidables (~1-2% pension)Calcul officiel exactTransparenceTrès élevée - Formules et barèmes explicitesOpaque ("boîte noire")
📌 Recommandation d'Usage

Utilisez ce simulateur pour :

Comprendre les mécanismes de calcul de votre pension
Comparer différents scénarios (quotités, surcotisation, rachat)
Simuler une retraite définitive directe (nouveau)
Vérifier l'applicabilité du Décret 1982 sur votre situation
Préparer vos décisions de fin de carrière
Vérifier la cohérence des calculs officiels


Pour une estimation officielle définitive :

Consultez ensap.gouv.fr (simulateur officiel)
Contactez le Service des Retraites de l'État (SRE)



🔍 Écart Connu avec le SRE
Ce simulateur applique rigoureusement la méthode SRE documentée publiquement. Un écart de 1 à 2 trimestres liquidables peut exister avec le calcul officiel, probablement dû à des règles d'arrondi intermédiaires non documentées publiquement.
Impact estimé : ~1-2% sur le montant final de la pension.

🚀 Utilisation
En ligne (recommandé)
Fichier HTML autonome, aucune installation requise :

Téléchargez le fichier simulateur_retraite_Version_V.04.2.3.html
Ouvrez-le dans votre navigateur web moderne (Chrome, Firefox, Edge, Safari)
Remplissez vos paramètres dans l'onglet "Paramètres"
Vérifiez l'option Décret n°82-624 selon votre situation
Choisissez votre mode de simulation :

"Résultats RP" pour une retraite progressive
"Retraite Définitive" pour une simulation directe sans retraite progressive ⭐ Nouveau


Cliquez sur "Calculer la simulation"

Depuis le code source
bash# Cloner le dépôt
git clone https://github.com/votre-username/simulateur-retraite-progressive.git

# Ouvrir le fichier HTML
cd simulateur-retraite-progressive
open simulateur_retraite_Version_V.04.2.3.html

📖 Base Réglementaire
Textes de référence

Code des pensions civiles et militaires de retraite (Articles L9, L11, L12, L12 bis, L13, L14, L15, L18, L89 bis à L89 ter)
Décret n°82-624 du 20 juillet 1982 (Temps partiel : 6/7ème et 32/35ème)
Décret n°2003-1306 du 26 décembre 2003 (Bonifications enfants)
Décret n°2011-620 du 31 mai 2011 (Institution retraite progressive)
Loi n°2023-270 du 14 avril 2023 (Réforme des retraites)
Décret n°2023-799 du 21 août 2023 (Surcote parentale)
Arrêté du 23 juin 2023 (Valeur du point d'indice : 4,92278 €)

Conditions d'accès à la retraite progressive

Âge minimum : 60 ans
Durée d'assurance minimale : 150 trimestres
Quotités autorisées : 50%, 60%, 70%, 80%, 90%
Application optionnelle du Décret 1982 pour les quotités 80% et 90%


🛠️ Maintenance et Évolution
Contrôles Périodiques Recommandés
🗓️ Annuels (chaque janvier)

Mettre à jour la valeur du point d'indice
Vérifier le minimum garanti (MG)
Actualiser les barèmes de surcotisation
Mettre à jour les tables de mortalité INSEE (analyse actuarielle)

📜 Événementiels

Surveiller les publications de nouveaux décrets sur la retraite progressive
Vérifier les modifications des durées de cotisation requises
Intégrer les changements de règles de bonification
Actualiser les barèmes de rachat de trimestres

Ressources Officielles à Surveiller

Légifrance - Textes législatifs et réglementaires
retraitesdeletat.gouv.fr - Site du SRE
INSEE - Données démographiques et actuarielles


🔧 Technologies Utilisées

HTML5 - Structure de la page
CSS3 - Design responsive et moderne
JavaScript Vanilla - Logique de calcul (aucune dépendance)
Chart.js - Visualisation graphique (graphiques en ligne et en barres)
Base de calcul : Méthode SRE (360 jours/an, 30 jours/mois)

Compatibilité Navigateurs

✅ Chrome/Edge (v90+)
✅ Firefox (v88+)
✅ Safari (v14+)
✅ Opera (v76+)


📝 Structure du Code
simulateur_retraite_Version_V.04.2.3.html
├── <head>
│   ├── Styles CSS (design responsive)
│   └── Métadonnées
├── <body>
│   ├── Navigation (6 onglets)
│   ├── Onglet Paramètres (saisie données + option Décret 1982)
│   ├── Onglet Résultats RP (retraite progressive)
│   ├── Onglet Retraite Définitive ⭐ NOUVEAU
│   ├── Onglet Graphique (comparaison quotités RP)
│   ├── Onglet Analyse Rachat
│   └── Onglet Sources (références légales)
└── <script>
    ├── Fonctions de calcul SRE
    ├── Gestion Décret n°82-624
    ├── Analyse surcotisation (RP + Définitive)
    ├── Calcul retraite définitive ⭐ NOUVEAU
    ├── Analyse rachat trimestres
    ├── Gestion événements
    └── Import/Export JSON

🤝 Contribution
Les contributions sont les bienvenues pour améliorer cet outil !
Comment contribuer

Fork le projet
Créez une branche pour votre fonctionnalité (git checkout -b feature/amelioration)
Testez soigneusement vos modifications
Committez vos changements (git commit -m 'Ajout fonctionnalité X')
Push vers la branche (git push origin feature/amelioration)
Ouvrez une Pull Request

Priorités de développement

Intégration calcul RAFP (Retraite Additionnelle de la Fonction Publique)
Export PDF des résultats
Historique des simulations (LocalStorage)
Mode sombre
Support multilingue (anglais)
API REST pour intégration externe
Simulation multi-périodes (plusieurs changements de quotité) 🔮


📄 Licence
Ce projet est sous licence MIT - voir le fichier LICENSE pour plus de détails.
Copyright (c) 2025 [Votre Nom]
Permission est accordée, gratuitement, à toute personne obtenant une copie de ce logiciel et des fichiers de documentation associés, de traiter le logiciel sans restriction, y compris sans limitation les droits d'utiliser, copier, modifier, fusionner, publier, distribuer, sous-licencier et/ou vendre des copies du logiciel.

📞 Support et Contact
🐛 Signaler un Bug
Ouvrez une issue GitHub avec :

Description détaillée du problème
Paramètres de simulation utilisés
Résultat obtenu vs attendu
Navigateur et version

💬 Questions et Discussions
Utilisez la section Discussions GitHub
⚠️ Avertissement Support
Ce projet est fourni "tel quel" sans garantie. Pour des conseils personnalisés sur votre situation retraite, consultez un conseiller retraite officiel ou le SRE.

🙏 Remerciements

Service des Retraites de l'État (SRE) pour la documentation publique de la méthode de calcul
INSEE pour les données démographiques et actuarielles
Légifrance pour l'accès aux textes réglementaires
Tous les contributeurs et testeurs du projet


📊 Statistiques du Projet

Première version : Août 2024
Version actuelle : V.04.2.3
Lignes de code : ~3200 lignes (HTML + CSS + JS)
Taille du fichier : ~180 Ko
Temps de chargement : < 1 seconde


🗺️ Roadmap
Version 0.5 (Q2 2025)

Calcul RAFP (Retraite Additionnelle)
Export PDF des simulations
Historique des calculs

Version 1.0 (Q3 2025)

Interface multilingue
Mode hors-ligne (PWA)
Comparaison avant/après réforme

À long terme

API REST documentée
Application mobile native
Extension navigateur


📅 Historique des Versions
V.04.2.3 (Janvier 2025)

➕ Ajout onglet "Retraite Définitive" - Simulateur complet pour retraite sans période progressive
📊 Graphique comparatif en barres des quotités pour la retraite définitive
🔄 Récupération automatique des données depuis l'onglet Paramètres
💰 Analyse de surcotisation vs placement alternatif dans l'onglet Retraite Définitive
🎯 Projection simple avec quotité fixe jusqu'au départ en retraite
✨ Interface à 6 onglets (ajout du 6ème onglet)

V.04.2.2 (Janvier 2025)

➕ Ajout option Décret n°82-624 (6/7ème pour 80%, 32/35ème pour 90%)
🔧 Correction positionnement tooltips (alignement droit)
📄 Mise à jour documentation et sources réglementaires
✨ Affichage explicite de la fraction appliquée dans les résultats

V.04.2.1 (Janvier 2025)

➕ Ajout onglet "Analyse Rachat de trimestres"
📊 Comparaison rachat vs placement alternatif
🎯 Recommandations personnalisées

V.04.2.0 (Décembre 2024)

✅ Validation calcul + disclaimer écart SRE
📈 Analyse actuarielle surcotisation
🔄 Amélioration interface utilisateur


⭐ Soutenir le Projet
Si ce simulateur vous est utile :

⭐ Star le projet sur GitHub
🐦 Partagez avec vos collègues fonctionnaires
🐛 Signalez les bugs rencontrés
💡 Proposez de nouvelles fonctionnalités
🤝 Contribuez au code


Disclaimer : Cet outil est un projet indépendant et n'est affilié à aucune administration publique française. Pour toute décision officielle concernant votre retraite, référez-vous aux services officiels (SRE, ENSAP).
Dernière mise à jour du README : Janvier 2025 - Version V.04.2.3

Modifications apportées pour V.04.2.3 :

✅ Version mise à jour en V.04.2.3 dans les badges et partout dans le document
✅ Ajout section détaillée "Simulateur de Retraite Définitive" dans les fonctionnalités principales
✅ Mise à jour de "5 onglets" vers "6 onglets"
✅ Ajout du nouvel onglet "Retraite Définitive" dans la structure du code
✅ Historique des versions avec V.04.2.3 en premier
✅ Statistiques mises à jour (~3200 lignes, ~180 Ko)
✅ Nom de fichier HTML mis à jour partout en V.04.2.3
✅ Mention de la simulation multi-périodes dans les priorités de développement
✅ Ajout des deux types de graphiques (ligne et barres)
