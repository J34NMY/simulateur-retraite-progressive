📖 Mode d'emploi du Simulateur de Retraite Progressive V.04.2.8

🎯 Introduction
Ce simulateur gratuit vous permet d'estimer votre pension de retraite progressive et définitive en tant que fonctionnaire d'État. Il applique la méthode officielle du Service des Retraites de l'État (SRE) avec une transparence totale sur les calculs.
✨ NOUVEAU V.04.2.8 : Corrections critiques des validations de cohérence - messages d'erreur optimisés, hiérarchisés et plus pédagogiques.

Vous devez avant toutes choses récupérer votre relevé de carrière sur le site info retraite
🚀 Démarrage rapide
Installation

Téléchargez le fichier simulateur_retraite_V.04.2.8.html
Double-cliquez dessus pour l'ouvrir dans votre navigateur
Aucune installation, aucune connexion internet requise !

Premier calcul en 3 étapes

Acceptez les conditions d'utilisation (bannière d'avertissement)
Onglet "Paramètres" → Remplissez vos données
Cliquez sur "Calculer la simulation"
Onglet "Résultats RP" → Consultez vos résultats
Exportez en PDF si vous souhaitez conserver les résultats


🆕 Nouveautés V.04.2.8 - Corrections critiques de validation
✅ Corrections majeures apportées (AMÉLIORATION CRITIQUE)
La V.04.2.8 corrige et optimise le système de validation introduit en V.04.2.7. Les 31 contrôles de cohérence sont maintenant plus intelligents, mieux hiérarchisés et plus pédagogiques.
Problèmes corrigés :

🐛 Messages d'erreur mal priorisés (erreurs mineures avant critiques)
🐛 Détection insuffisante des dates irréalistes
🐛 Validations trop permissives ou trop restrictives
🐛 Messages d'erreur peu clairs ou redondants

Améliorations apportées :
1. Validation date de naissance optimisée ⭐

✅ Hiérarchisation des messages : erreurs critiques prioritaires
✅ Détection dates irréalistes : avant 1900, après 2080
✅ Validation âge actuel : 18-80 ans avec messages adaptés
✅ Meilleure expérience utilisateur : messages plus clairs

Exemple avant V.04.2.8 :
⚠️ Âge actuel inhabituel (85 ans)
❌ Trimestres incohérents vs années de carrière
Exemple après V.04.2.8 :
❌ Date de naissance irréaliste (1940). Veuillez vérifier votre saisie.
→ Le message critique (date irréaliste) est maintenant affiché en priorité !
2. Validation dates de départ améliorée ⭐

✅ Priorisation intelligente : dates irréalistes → âges → règles réglementaires
✅ Messages plus précis : différenciation 67-70 ans (prolongation vs limite)
✅ Détection améliorée : erreurs de saisie (ex: 2090 au lieu de 2029)

Exemple de priorisation :
PrioritéType d'erreurMessage1️⃣ CRITIQUEDate irréaliste (2090)❌ Date de départ irréaliste (2090). Vérifiez votre saisie.2️⃣ CRITIQUEÂge irréaliste (> 80 ans)❌ Âge au départ irréaliste (85 ans). Maximum : 70 ans.3️⃣ WARNINGÂge 67-70 (prolongation)⚠️ Départ après 67 ans : prolongation requise4️⃣ ERREURÂge > 70❌ Départ après 70 ans impossible
3. Validation trimestres et jours renforcée ⭐

✅ Contrôle valeurs négatives : détection immédiate
✅ Vérification règle SRE : jours < 90 (90 jours = 1 trimestre)
✅ Cohérence assurance/liquidables : liquidables ≤ assurance
✅ Messages explicites : explication de la règle violée

Nouveaux messages :
❌ Les jours d'assurance ne peuvent pas être négatifs
❌ Les jours liquidables doivent être < 90 (90 jours = 1 trimestre)
❌ Les trimestres liquidables (150 trim.) ne peuvent pas être > aux trimestres d'assurance (140 trim.)
4. Validation indices et valeurs ⭐

✅ Plages réalistes : indice 350-900, point 4.5-5.5€
✅ Messages pédagogiques : référence aux valeurs officielles
✅ Détection anomalies : valeurs aberrantes signalées

Exemples :
⚠️ Indice majoré inhabituel (1200). Plage normale FP État : 350-900. Vérifiez votre saisie.
⚠️ Valeur du point inhabituelle (6.00 €). Valeur officielle 2025 : 4,92278 €. Vérifiez votre saisie.
5. Validation enfants (maintenue V.04.2.7)

✅ Cases cochées vs nombres saisis
✅ Cohérence totaux
✅ Champs grisés automatiquement
✅ Messages pédagogiques

6. Onglet Retraite Définitive : 9 validations corrigées ⭐

✅ Gestion warnings vs erreurs : calcul possible avec warnings
✅ Messages adaptés : contexte spécifique retraite définitive
✅ Validation optimisée : logique plus robuste

🎨 Nouvelle expérience utilisateur
Messages d'erreur hiérarchisés :

❌ CRITIQUE : bloque le calcul, à corriger immédiatement
⚠️ WARNING : calcul possible mais données inhabituelles
ℹ️ INFO : conseil ou suggestion

Basculement automatique :

En cas d'erreur, vous êtes automatiquement redirigé vers l'onglet Résultats
La liste complète des erreurs s'affiche avec icônes
Chaque erreur est accompagnée d'une explication

Suggestions d'actions :

Les messages indiquent la correction à apporter
Citations réglementaires quand pertinent
Liens vers les onglets pertinents


📋 Liste complète des 31 validations
Onglet Paramètres (22 validations)
1. Dates (9 validations) - AMÉLIORÉES V.04.2.8 ⭐
ValidationExemple d'erreurMessage affichéPrioritéDate relevé < Date départ progressifIncohérence temporelle❌ La date de départ progressif doit être APRÈS la date du relevéCRITIQUEDate départ progressif < Date départ définitifDates identiques❌ La date de départ définitif doit être APRÈS la date de départ progressifCRITIQUEDate naissance avant 1900Naissance : 1890❌ Date de naissance irréaliste (1890). Veuillez vérifier votre saisie.CRITIQUE ⭐Dates futur lointainDépart : 2090❌ Date de départ irréaliste (2090). Vérifiez votre saisie.CRITIQUE ⭐Âge actuel > 80 ans85 ans aujourd'hui⚠️ Âge actuel inhabituel (85 ans). Retraite progressive concerne 60-67 ans.WARNING ⭐Âge actuel < 40 ans25 ans aujourd'hui⚠️ Âge actuel très jeune (25 ans). Retraite progressive accessible à 60 ans.WARNING ⭐Âge départ > 80 ansDépart à 85 ans❌ Âge au départ irréaliste (85 ans). Maximum réglementaire : 70 ans.CRITIQUE ⭐Départ après 67-70 ansDépart à 68 ans⚠️ Départ après 67 ans : vous devrez obtenir une prolongation d'activitéWARNING ⭐Départ après 70 ansDépart à 72 ans❌ Départ après 70 ans impossible : limite d'âge maximale dépasséeCRITIQUE ⭐
2. Trimestres/Jours (4 validations) - RENFORCÉES V.04.2.8 ⭐
ValidationExemple d'erreurMessage affichéTrimestres vs années160 trim pour 12 ans❌ Incohérence : 160 trimestres d'assurance pour 12 ans de carrière (max ~52 trim.)Jours négatifsJours : -10❌ Les jours d'assurance ne peuvent pas être négatifsJours >= 90Jours : 95❌ Les jours liquidables doivent être < 90 (90 jours = 1 trimestre)Liquidables > AssuranceLiq:150, Ass:140❌ Les trimestres liquidables ne peuvent pas être > aux trimestres d'assurance
3. Indices/Valeurs (3 validations) - AMÉLIORÉES V.04.2.8 ⭐
ValidationExemple d'erreurMessage affichéIndice hors plageIndice : 1200⚠️ Indice majoré inhabituel (1200). Plage normale FP État : 350-900. Vérifiez.Valeur point incorrecteValeur : 6.00€⚠️ Valeur du point inhabituelle (6.00€). Valeur officielle 2025 : 4,92278€.Trimestres requisTrimestres : 200❌ Trimestres requis incorrects (200). Plage normale : 150-180 trimestres.
4. Enfants (4 validations + UX) - MAINTENUES V.04.2.7
ValidationExemple d'erreurMessage affichéCase cochée + 0 enfantsBonif cochée, 0 enfants❌ Case "Bonification enfants avant 2004" cochée mais aucun enfant saisiEnfants saisis sans case2 enfants, case non cochée❌ Vous avez saisi des enfants avant 2004 mais la case n'est pas cochéeTotal ≠ sommeTotal:3, Avant:1, Après:1❌ Incohérence : total enfants (3) ≠ somme des enfants saisis (2)Champs actifs/grisés-✨ Champs automatiquement grisés si cases non cochées
5. Durée période progressive (2 validations)
ValidationExemple d'erreurMessage affichéPériode < 1 mois15 jours⚠️ Période de retraite progressive très courte (moins d'1 mois)Période > 5 ans6 ans⚠️ Période très longue (6.0 ans). Cas inhabituel.
Onglet Retraite Définitive (9 validations) - CORRIGÉES V.04.2.8 ⭐
ValidationExemple d'erreurMessage affichéPrioritéDonnées non récupéréesClic sans récupérer❌ Veuillez d'abord récupérer les données du simulateurCRITIQUEDate départ obligatoireChamp videLa date de départ en retraite est obligatoireCRITIQUEDate départ > relevéIncohérence❌ La date de départ doit être APRÈS la date du relevéCRITIQUE ⭐Date passéDate : 2020❌ Date de départ dans le passé. Vérifiez votre saisie.CRITIQUE ⭐Date futur lointainDate : 2090❌ Date de départ irréaliste (2090). Vérifiez votre saisie.CRITIQUE ⭐Âge au départ55 ou 85 ans❌ Âge au départ trop jeune/élevé. Plage : 60-70 ansCRITIQUE/WARNING ⭐Quotité invalideQuotité : 1.2La quotité doit être entre 0 et 1 (ex: 0.8 pour 80%)CRITIQUESurcotisation + 100%Surcot cochée + 100%❌ Surcotisation possible uniquement à temps partielCRITIQUEDurée projectionPériode anormale⚠️ Période de projection inhabituelleWARNING

📊 Guide des onglets
1️⃣ Onglet PARAMÈTRES
Section "Données du relevé de carrière"
Date du relevé

Date de votre dernier relevé de carrière officiel SRE
Format : JJ/MM/AAAA
Exemple : 31/12/2024

Trimestres d'assurance au relevé

Nombre total de trimestres d'assurance selon votre relevé SRE
Exemple : 160 trimestres + 84 jours
Les trimestres d'assurance comptent pour la durée de cotisation (évitent la décote)

Trimestres liquidables au relevé

Nombre de trimestres de services effectifs selon votre relevé SRE
Exemple : 142 trimestres + 86 jours
Les trimestres liquidables déterminent le montant de la pension (prorata)

Section "Informations personnelles"
Date de naissance - VALIDATION OPTIMISÉE V.04.2.8 ⭐

Obligatoire pour calculer l'âge légal et les trimestres requis
Détermine automatiquement votre génération (1964 → 171 trimestres requis)
Nouveau : détection immédiate des dates irréalistes

Sexe

Utilisé uniquement pour l'analyse actuarielle de rentabilité
Basé sur les tables de mortalité INSEE 2024

Trimestres requis

Calculé automatiquement selon votre année de naissance
1965 et après → 172 trimestres
1964 → 171 trimestres, etc.

Indice majoré (IM) - VALIDATION AMÉLIORÉE V.04.2.8 ⭐

Votre indice majoré actuel
Exemple : 478
Nouveau : vérification plage réaliste (350-900)
Attention à la règle des six mois : une augmentation d'indice doit avoir au moins 6 mois d'ancienneté avant le départ

Valeur du point - VALIDATION AMÉLIORÉE V.04.2.8 ⭐

Valeur officielle : 4,92278 € (depuis le 1er juillet 2023)
Nouveau : vérification plage réaliste (4.5-5.5€)
Mise à jour annuelle en général

Section "Planning de retraite progressive"
Date de départ retraite progressive - VALIDATION OPTIMISÉE V.04.2.8 ⭐

Date de début de votre retraite progressive
Conditions : minimum 60 ans + 150 trimestres d'assurance
Nouveau : priorisation des messages d'erreur (dates irréalistes d'abord)

Date de départ retraite définitive - VALIDATION OPTIMISÉE V.04.2.8 ⭐

Date de fin de la période progressive
Entre cette date et le départ progressif, vous cumulez traitement partiel + pension provisoire
Nouveau : détection améliorée des erreurs de saisie

Quotité entre relevé et départ progressif

Votre quotité de travail ACTUELLE (avant la retraite progressive)
100% = temps plein
80% = 4 jours/semaine
Cette quotité impacte l'accumulation de trimestres liquidables

Quotité pendant la retraite progressive

Votre quotité pendant la période progressive
Choix : 50%, 60%, 70%, 80%, 90%
Attention : cette quotité impacte la surcote parentale

Appliquer le Décret n°82-624

Coché par défaut (cas majoritaire)
Concerne certains fonctionnaires en temps partiel de droit commun :

80% → rémunération à 6/7ème (≈85,71%)
90% → rémunération à 32/35ème (≈91,43%)



Comment vérifier si cela vous concerne ?

Consultez votre fiche de paie actuelle si vous êtes déjà à temps partiel 80% ou 90%
Regardez la ligne "Traitement Brut"
Si vous travaillez 4j/5 (80%) et êtes payé plus de 80%, le décret s'applique
Si incertain, laissez coché (cas par défaut)

Section "Options de surcotisation"
Surcotisation pendant la progressive

Si coché : vos trimestres liquidables comptent à 100% (même à temps partiel)
Coût supplémentaire selon barème 2024 (ex: 16,2% pour 80%)
Une analyse de rentabilité complète sera affichée

Taux de surcotisation

Calculé automatiquement selon votre quotité
Barème 2024 :

50% → 23,85%
60% → 21,30%
70% → 18,75%
80% → 16,20%
90% → 13,65%



Taux de placement alternatif

Pour comparer la surcotisation avec un placement financier
Options : Livret A (3%), LEP (4%), placements dynamiques (4,5-5%)

Section "Droits liés aux enfants"
Gestion automatique des champs (V.04.2.7) - MAINTENUE V.04.2.8
Les champs sont automatiquement grisés si les cases ne sont pas cochées, pour éviter toute confusion.
Bonification enfants nés/adoptés avant 2004

Conditions strictes :

Enfant né ou adopté avant le 1er janvier 2004
Interruption ou réduction d'activité ≥ 2 mois consécutifs
Enfant élevé pendant ≥ 9 ans avant ses 16 ans


Gain : 4 trimestres liquidables + 4 trimestres assurance PAR ENFANT
Validation lors de la demande de retraite avec justificatifs

Majoration enfants nés/adoptés à partir de 2004

Conditions :

Enfant né ou adopté à partir du 1er janvier 2004
Après recrutement dans la fonction publique


Gain : 2 trimestres d'assurance PAR ENFANT (pas de liquidables)
Attribution automatique

Total enfants (majoration familiale)

Calculé automatiquement
Majoration de pension :

3 enfants → +10%
4 enfants → +15%
5 enfants → +20%, etc.


Condition : enfants élevés 9 ans avant leurs 16 ans

Section "Information pension provisoire"
Un encadré informatif explique le fonctionnement de la pension provisoire :
Calculée au départ : basée sur les droits acquis AVANT le départ progressif
Évolution possible : si vous changez de quotité pendant la progressive, la part versée s'ajuste automatiquement

Exemple : passage de 80% → 70% de travail
Pension provisoire passe de 20% → 30% du montant de référence

Trimestres pendant la progressive : ne modifient PAS le montant provisoire

Les nouveaux trimestres acquis sont comptabilisés
Mais le montant de référence reste fixe

Recalcul à la retraite définitive : tous les droits acquis pendant la progressive seront pris en compte dans le calcul final

2️⃣ Onglet RÉSULTATS RP (Retraite Progressive)
Durées et trimestres

Affiche les périodes calculées avec la méthode SRE (base 360 jours/an)
Décomposition : années, mois, jours

Compteurs au départ progressif

État de vos compteurs à la date de départ en retraite progressive
Assurance vs Liquidables
Bonifications prises en compte

Revenus pendant la retraite progressive

Traitement à la quotité : votre salaire partiel
Pension provisoire : (1 - quotité) × pension de référence
Note importante : une mention indique que si vous changez de quotité, la pension s'ajustera
Total brut mensuel : traitement + pension
Si surcotisation : affichage du coût mensuel et du net après surcotisation

Analyse de surcotisation (si activée)
Comparaison détaillée :

Coût total de la surcotisation
Gain mensuel de pension (surcotisation vs sans)
Durée de rentabilisation (combien d'années de retraite pour récupérer l'investissement)
Alternative placement :

Capital après période progressive
Rente mensuelle générée
Capital préservé et transmissible


Recommandation : FAVORABLE / NEUTRE / DÉFAVORABLE

Situation en fin de période

Assurance et liquidables finaux
Taux de liquidation estimé
Traitement de référence

Pension définitive estimée

Montant principal en gros caractères verts
Avec majoration familiale si applicable

Détails décote/surcote

Si décote : trimestres manquants, taux appliqué, date du taux plein
Si surcote : détail des 3 types de majorations SRE

Surcote parentale (max 5%)
Surcote classique (après âge légal)
Majoration excédentaire (trimestres restants)



Export PDF des résultats

Bouton "Télécharger les résultats en PDF" en bas de page
Génère un document professionnel avec :

En-tête avec version et date
Avertissement NON OFFICIEL en première page
Tous les paramètres de simulation
Résultats détaillés
Analyses de rentabilité
Avertissements et disclaimers
Mention ensap.gouv.fr pour estimation officielle


Format A4 optimisé pour impression
Accents français parfaitement préservés (support natif jsPDF 2.5.1)
Nom du fichier : simulation_retraite_progressive_YYYY-MM-DD.pdf


3️⃣ Onglet RETRAITE DÉFINITIVE
Cet onglet permet de simuler une retraite définitive sans période de retraite progressive.
Mode d'emploi

Cliquez sur "Récupérer les données"

Importe automatiquement vos paramètres depuis l'onglet Paramètres
Affiche votre situation actuelle


Définissez votre projection

Date de départ en retraite : quand souhaitez-vous partir ?
Quotité envisagée : à quel temps travaillerez-vous jusqu'au départ ?

100% = temps plein jusqu'à la retraite
80% = 4j/5 jusqu'à la retraite
etc.




Options

Décret n°82-624 : même principe que l'onglet Paramètres
Surcotisation : si temps partiel, option de surcotiser pour compter les liquidables à 100%


Cliquez sur "Calculer la simulation"

9 validations automatiques - CORRIGÉES V.04.2.8 ⭐
Le simulateur vérifie automatiquement :

✅ Données récupérées du simulateur
✅ Date de départ obligatoire et cohérente
✅ Âge au départ valide avec messages optimisés ⭐
✅ Quotité valide
✅ Surcotisation + 100% interdite
✅ Durée de projection cohérente
✅ Gestion warnings vs erreurs bloquantes ⭐
✅ Messages adaptés au contexte ⭐

Message informatif intelligent :
Si vos trimestres liquidables sont < à vos trimestres d'assurance, un message s'affiche :
ℹ️ Trimestres liquidables inférieurs à l'assurance
Écart détecté : 18.5 trimestres.
Cela indique des périodes de temps partiel dans votre passé.
💡 Pour rattraper ces trimestres, consultez l'onglet "Analyse Rachat".
Résultats affichés
Projection de carrière

Période entre aujourd'hui et le départ
Trimestres acquis pendant cette période
Impact de la quotité choisie

Trimestres au départ

Assurance totale / Liquidables totaux
Bonifications enfants prises en compte
Âge au départ

Analyse de surcotisation (si activée)

Même analyse que pour la retraite progressive
Coût sur toute la période jusqu'au départ
Comparaison avec placement alternatif

Pension définitive

Montant estimé selon le scénario choisi
Avec/sans majoration familiale

Graphique comparatif en barres

Compare automatiquement 6 scénarios de quotité (50%, 60%, 70%, 80%, 90%, 100%)
La barre rouge = votre quotité sélectionnée
Permet de visualiser l'impact d'un changement de quotité

Export PDF de la simulation

Bouton "Télécharger les résultats en PDF" en bas de page
Document avec :

Avertissement NON OFFICIEL en première page
Données récupérées du simulateur
Projection jusqu'au départ
Trimestres au départ
Pension définitive estimée
Analyses de surcotisation si applicable
Mention ensap.gouv.fr répétée


Accents français parfaitement préservés
Nom du fichier : simulation_retraite_definitive_YYYY-MM-DD.pdf


4️⃣ Onglet GRAPHIQUE
Graphique en ligne : Revenus pendant la retraite progressive

Compare vos revenus totaux bruts selon différentes quotités (50% à 90%)
Le point rouge indique votre quotité sélectionnée
Permet de voir rapidement l'impact financier d'un changement de quotité

Comment l'interpréter ?

Plus la quotité est basse → plus le revenu total est faible (logique)
Mais le gain en temps libre peut compenser
À utiliser pour trouver votre équilibre vie/revenus


5️⃣ Onglet ANALYSE RACHAT - CORRIGÉ V.04.2.5
Cet onglet analyse la rentabilité du rachat de trimestres avec les coefficients corrects de la Fonction Publique d'État.
CHANGEMENT MAJEUR V.04.2.5
Ancienne version (V.04.2.4 et antérieures) :

Utilisait les barèmes du secteur privé
Coûts 2 à 3 fois trop élevés
Exemple : 4 trim. à 40 ans = 15 200 € (FAUX)

Nouvelle version (V.04.2.5+) :

Utilise les coefficients Fonction Publique d'État
Calcul basé sur votre traitement indiciaire
Exemple : 4 trim. à 40 ans = 5 836 € (CORRECT)

Mode d'emploi

Cliquez sur "Récupérer les données"

Importe votre situation depuis l'onglet Paramètres


Paramétrez votre rachat

Nombre de trimestres : entre 1 et 12
Type de rachat :

Années d'études supérieures
Années civiles incomplètes


Option de rachat :

Option 1 - Taux seul : moins cher, évite la décote uniquement
Option 2 - Taux + Durée : plus cher, augmente aussi la pension


Âge au rachat : votre âge actuel ou prévu
TMI : votre tranche marginale d'imposition (pour calculer l'économie fiscale)


Taux de placement alternatif

Pour comparer avec un placement financier
Ex: Livret A 3%, LEP 4%, placements dynamiques 5%


Cliquez sur "Analyser la rentabilité"

Résultats affichés
Coût du rachat

Coefficient appliqué : pourcentage de votre traitement (CORRIGÉ V.04.2.5)
Coût par trimestre (basé sur votre traitement indiciaire)
Coût nominal (brut)
Économie d'impôt (le rachat est déductible)
Coût réel après déduction fiscale

Impact sur la pension

Gain mensuel de pension
Gain annuel
Durée de rentabilisation : combien d'années de retraite pour récupérer l'investissement

Comparaison avec placement

Rachat : gain viager, non transmissible
Placement : capital préservé, transmissible, rente mensuelle

Recommandation

FAVORABLE : le rachat est rentable
NEUTRE : les deux se valent
DÉFAVORABLE : le placement est préférable

Points d'attention

Espérance de vie
Liquidité des fonds
Transmission patrimoniale
Protection contre l'inflation

Important : Les coefficients affichés sont indicatifs (basés sur 2024, catégorie sédentaire). Demandez toujours un devis officiel au SRE via ensap.gouv.fr.
Export PDF de l'analyse

Bouton "Télécharger l'analyse en PDF" en bas de page
Document complet avec :

Avertissement COÛTS INDICATIFS en première page
Données récupérées
Paramètres du rachat
Coût détaillé du rachat
Impact sur la pension
Comparaison avec placement
Recommandation personnalisée
Points d'attention
Mention ensap.gouv.fr pour devis officiel


Accents français parfaitement préservés
Nom du fichier : analyse_rachat_trimestres_YYYY-MM-DD.pdf

Comprendre les coefficients Fonction Publique
Formule de calcul :
Coût par trimestre = Traitement indiciaire × Coefficient d'âge
Coefficients indicatifs (base 2024) :
ÂgeOption 1 (Taux seul)Option 2 (Taux + Durée)30 ans~28%~50%40 ans~35%~62%50 ans~48%~85%60 ans~85%~150%
Exemple concret :

Vous avez 42 ans
Traitement indiciaire : 2 353 €
Option 2 (Taux + Durée)
Coefficient interpolé : ~64%

Calcul :

Coût par trimestre : 2 353 × 0,64 = 1 506 €
Pour 4 trimestres : 1 506 × 4 = 6 024 €
Économie d'impôt (TMI 30%) : 6 024 × 0,30 = 1 807 €
Coût réel : 6 024 - 1 807 = 4 217 €

Comparaison V.04.2.4 vs V.04.2.5 :

V.04.2.4 (FAUX) : 15 200 € → 10 640 € après impôt
V.04.2.5 (CORRECT) : 6 024 € → 4 217 € après impôt
Économie : 6 423 € (division par 2,5)


6️⃣ Onglet SOURCES
Références réglementaires complètes :

Code des pensions civiles et militaires
Décrets applicables (dont Décret 2007-262 sur le rachat)
Liens vers sites officiels
Méthode de calcul SRE détaillée
Tableau des coefficients rachat Fonction Publique (V.04.2.5)
Section mise à jour sur la pension provisoire avec l'explication correcte
Avertissement sur la précision du simulateur


7️⃣ Onglet MENTIONS LÉGALES
Nature de l'outil

Simulateur gratuit et pédagogique
NON OFFICIEL - ne remplace pas ENSAP
Ne constitue pas un conseil financier
Outil éducatif pour comprendre les mécanismes

Développement et responsabilité
Éditeur du simulateur

Développé par : Jean-Michel DI PACO
Avec l'assistance technique de : Claude (Anthropic) - Intelligence artificielle conversationnelle
Version : V.04.2.8
Dernière mise à jour : Novembre 2025
Contact : maviclearn@gmail.com

Collaboration avec Claude (Anthropic)
Ce simulateur a été développé en collaboration avec Claude, l'assistant IA d'Anthropic, pour les aspects :

Algorithmiques : Implémentation rigoureuse des calculs SRE conformes aux textes réglementaires
Techniques : Architecture du code, gestion des exports PDF, optimisation, système de validation
Réglementaires : Interprétation et application des décrets et du Code des pensions
Légaux : Rédaction des mentions légales, CGU, disclaimers adaptés au modèle gratuit
Documentaires : Rédaction du mode d'emploi et de la documentation technique

L'éditeur assume l'entière responsabilité du contenu, de l'exactitude des calculs et de la conformité réglementaire.
Conditions d'utilisation

Utilisation gratuite
Limitation de responsabilité
Non-opposabilité des résultats
Recommandation forte de consulter ensap.gouv.fr

Avertissement important
Écart technique documenté :

Ce simulateur applique rigoureusement la méthodologie de calcul SRE documentée publiquement (base 360 jours/an, règles d'arrondi standard)
Un écart de 1 à 2 trimestres liquidables peut exister avec le calcul officiel du SRE/ENSAP
Cause probable : Règles d'arrondi intermédiaires ou modalités de calcul spécifiques non documentées publiquement par le SRE
Impact estimé : Environ 1 à 2% du montant final de la pension

⚠️ CE SIMULATEUR NE REMPLACE EN AUCUN CAS LES OUTILS OFFICIELS DE L'ÉTAT
Seules les simulations effectuées sur ensap.gouv.fr ont valeur légale.
Pour votre estimation officielle définitive : Consultez obligatoirement ensap.gouv.fr ou contactez directement le Service des Retraites de l'État.
Données personnelles

Aucune donnée collectée
Calculs 100% locaux dans le navigateur
Pas de transmission de données
Pas de cookies (sauf hébergement)

Propriété intellectuelle

Code protégé par droit d'auteur
Usage personnel autorisé
Usage commercial interdit sans autorisation

Validation et démarche qualité
Phase de validation en cours

Ce simulateur est actuellement en phase de beta test auprès de fonctionnaires d'État
Comparaison systématique avec simulations ENSAP officielles
Documentation des écarts observés
Amélioration continue basée sur les retours

Démarche qualité

Application stricte des textes réglementaires
Corrections rapides suite aux retours utilisateurs
Documentation exhaustive des sources
Transparence sur les limitations
Disclaimers clairs et visibles
Aucune collecte de données personnelles
31 validations de cohérence optimisées (V.04.2.8) ⭐


📄 Fonctionnalités des exports PDF - V.04.2.6+
Amélioration majeure V.04.2.6
Support natif des accents français

jsPDF 2.5.1 supporte nativement tous les caractères accentués français
Plus besoin de fonction de conversion
Accents parfaitement préservés dans les PDFs : é, è, à, ç, ù, etc.
Compatible tous systèmes (Windows, Mac, Linux, mobile)
Garantit une lisibilité universelle

Différence avec V.04.2.5.1 :

V.04.2.5.1 : Fonction nettoyerPourPDF() pour convertir les accents
V.04.2.6+ : Support natif, plus besoin de conversion

Format des documents
Caractéristiques techniques

Format A4 (210 × 297 mm)
Marges optimisées (20mm)
Pagination automatique
En-têtes et pieds de page professionnels
Accents français natifs (pas de conversion)

Contenu des exports

Export Résultats RP (Retraite Progressive)

En-tête avec titre, version, date
Avertissement NON OFFICIEL en première page (encadré orange)
Mention ensap.gouv.fr pour estimation officielle
Section Paramètres de simulation
Section Résultats détaillés
Analyses de rentabilité si applicable
Avertissements et disclaimers
Mention "Simulation non contractuelle"


Export Retraite Définitive

Avertissement NON OFFICIEL en première page
Données récupérées du simulateur
Projection jusqu'au départ
Trimestres au départ
Pension définitive estimée
Analyses de surcotisation si applicable
Mention ensap.gouv.fr répétée


Export Analyse Rachat

Avertissement COÛTS INDICATIFS en première page (encadré orange)
Coût du rachat avec coefficients
Impact sur la pension
Comparaison avec placement
Recommandation
Avertissement sur caractère indicatif
Mention ensap.gouv.fr pour devis officiel



Génération du PDF

Bibliothèque : jsPDF 2.5.1
Génération instantanée côté client
Accents français parfaitement préservés
Nom de fichier automatique avec date : simulation_type_YYYY-MM-DD.pdf
Téléchargement direct dans votre dossier de téléchargements

Utilisation recommandée

Conserver vos simulations pour comparaison
Partager avec un conseiller retraite
Documenter votre réflexion
Imprimer pour consultation papier
Les PDFs sont maintenant parfaitement lisibles partout


🔧 Fonctionnalités avancées
Import/Export de simulations
Exporter vos paramètres

Remplissez l'onglet Paramètres
Cliquez sur "Exporter"
Un fichier JSON est téléchargé : parametres_simulateur_retraite_v04_2_8.json
Conservez ce fichier pour le réutiliser plus tard

Importer des paramètres

Cliquez sur "Importer"
Sélectionnez un fichier JSON précédemment exporté
Tous les champs sont automatiquement remplis

Utile pour comparer plusieurs scénarios ou partager avec un conseiller
Bouton "Valeurs par défaut"

Réinitialise tous les champs avec l'exemple par défaut
Utile pour tester le simulateur ou repartir de zéro


🤝 Développement et validation
Collaboration avec Claude (Anthropic)
Ce simulateur a été développé en collaboration avec Claude, l'assistant IA d'Anthropic, pour les aspects suivants :
Aspects algorithmiques

Implémentation rigoureuse de la méthode SRE (base 360 jours/an)
Calculs conformes aux textes réglementaires
Gestion des arrondis et cas particuliers
Algorithmes d'interpolation pour les coefficients de rachat
Système de validation exhaustif optimisé (V.04.2.8) ⭐

Aspects techniques

Structure et architecture du code JavaScript
Gestion des exports PDF avec jsPDF 2.5.1
Support natif des accents français (V.04.2.6)
Optimisation des performances
Compatibilité multi-navigateurs
31 validations de cohérence améliorées (V.04.2.8) ⭐

Aspects réglementaires

Interprétation des textes de loi (Code des pensions, décrets)
Application correcte des règles de calcul SRE
Identification des coefficients Fonction Publique d'État
Documentation des sources réglementaires

Aspects légaux

Rédaction des mentions légales complètes
Conditions d'utilisation adaptées au modèle gratuit
Disclaimers appropriés et visibles partout
Politique de confidentialité
Avertissements renforcés (V.04.2.6)

Documentation

Rédaction du mode d'emploi complet
Création du README.md technique
Explications pédagogiques des calculs
FAQ et cas d'usage
Documentation des validations optimisées (V.04.2.8) ⭐

L'éditeur assume l'entière responsabilité du contenu, de l'exactitude des calculs et du respect de la réglementation.

❓ FAQ - Foire Aux Questions
Questions générales
Q1 : Ce simulateur est-il officiel ?
R : Non. Ce simulateur est un outil pédagogique gratuit NON OFFICIEL. Seuls les calculs effectués sur ensap.gouv.fr ont valeur légale et sont opposables.
Q2 : Mes données personnelles sont-elles collectées ?
R : Absolument pas. Tous les calculs sont effectués localement dans votre navigateur. Aucune donnée n'est transmise à un serveur externe. Vous pouvez même utiliser le simulateur hors ligne après l'avoir téléchargé.
Q3 : Le simulateur est-il vraiment gratuit ?
R : Oui, totalement gratuit. Aucun paiement, aucune inscription, aucune publicité. C'est un outil éducatif développé pour aider la communauté des fonctionnaires d'État.
Q4 : Quelle est la précision du simulateur ?
R : Le simulateur applique rigoureusement la méthode SRE documentée. Un écart de 1 à 2 trimestres liquidables (~1-2% de pension) peut exister avec le calcul officiel, dû à des règles d'arrondi internes non documentées publiquement.
Questions sur la retraite progressive
Q5 : Quelles sont les conditions pour bénéficier de la retraite progressive ?
R :

Âge minimum : 60 ans (depuis le 1er septembre 2025)
Trimestres d'assurance : minimum 150 trimestres
Quotité de travail : entre 50% et 90%
Employeur : Accord de votre employeur requis

Q6 : Puis-je modifier ma quotité en cours de retraite progressive ?
R : Oui ! Vous pouvez demander à changer de quotité pendant la période progressive. Important : si vous modifiez votre quotité, la pension provisoire s'ajustera automatiquement. Par exemple, si vous passez de 80% de travail à 70%, votre pension provisoire passera de 20% à 30% du montant de référence.
Q7 : La pension provisoire est-elle définitive ?
R : Non, elle est provisoire et sera recalculée lors de votre départ en retraite définitive. Tous les trimestres acquis pendant la période progressive seront pris en compte dans le calcul final.
Q8 : Dois-je obligatoirement passer par la retraite progressive ?
R : Non, c'est un dispositif optionnel. Vous pouvez directement partir en retraite définitive. Utilisez l'onglet "Retraite Définitive" pour comparer les deux options.
Questions sur la surcotisation
Q9 : C'est quoi la surcotisation ?
R : La surcotisation permet de comptabiliser vos périodes à temps partiel comme du temps plein pour le calcul des trimestres liquidables. Vous payez un surcoût pendant la période progressive, mais vos trimestres comptent à 100%.
Q10 : La surcotisation est-elle rentable ?
R : Ça dépend ! Le simulateur calcule automatiquement la rentabilité en comparant avec un placement alternatif (Livret A, LEP, etc.). Consultez l'analyse actuarielle affichée dans les résultats.
Q11 : ✨ NOUVEAU V.04.2.8 : Pourquoi je ne peux pas cocher "Surcotisation" si je suis à 100% ?
R : C'est une validation ajoutée en V.04.2.7 et maintenue en V.04.2.8. La surcotisation n'est possible que pendant les périodes à temps partiel (quotité < 100%).
Distinction importante :

Surcotisation : pour le temps partiel FUTUR (pendant la progressive)
Rachat : pour rattraper le temps partiel PASSÉ (consultez l'onglet "Analyse Rachat")

Si vous travaillez à temps plein et souhaitez racheter des périodes passées à temps partiel, utilisez l'onglet "Analyse Rachat".
Questions sur le rachat de trimestres
Q12 : Quelle version utiliser pour l'analyse de rachat ?
R : Utilisez impérativement la V.04.2.5 ou supérieure (dont V.04.2.8). Les versions V.04.2.4 et antérieures contenaient une erreur majeure sur les barèmes (coûts 2,5 fois trop élevés).
Q13 : Pourquoi les coûts de rachat ont-ils changé entre les versions ?
R : CORRECTION MAJEURE V.04.2.5 : Les anciennes versions utilisaient à tort les barèmes du secteur privé. La V.04.2.5+ utilise les coefficients corrects de la Fonction Publique d'État, basés sur votre traitement indiciaire.
Exemple :

V.04.2.4 : 4 trim. à 40 ans = 15 200 € (FAUX)
V.04.2.5+ : 4 trim. à 40 ans = 5 836 € (CORRECT)

Q14 : Comment obtenir un devis officiel pour le rachat ?
R : Connectez-vous sur ensap.gouv.fr et suivez la procédure de demande de devis. Le SRE vous fournira un devis personnalisé et opposable, tenant compte de tous vos paramètres spécifiques.
Q15 : Le rachat de trimestres est-il déductible des impôts ?
R : Oui ! Les sommes versées pour le rachat de trimestres sont déductibles de votre revenu imposable, selon votre tranche marginale d'imposition (TMI). Cela réduit significativement le coût réel du rachat.
Exemple :

Coût brut : 6 000 €
TMI 30% : économie de 1 800 €
Coût réel : 4 200 €

Questions sur les exports PDF
Q16 : Les accents sont-ils bien gérés dans les PDFs ? - V.04.2.6+
R : Oui ! La V.04.2.6+ utilise jsPDF 2.5.1 qui supporte nativement tous les accents français (é, è, à, ç, ù, etc.). Plus besoin de conversion, les PDFs sont parfaitement lisibles partout, sur tous les systèmes (Windows, Mac, Linux, mobile).
Différence avec les versions précédentes :

V.04.2.5.1 et antérieures : Conversion des accents nécessaire
V.04.2.6+ : Support natif, aucune conversion

Questions sur les validations - AMÉLIORÉES V.04.2.8 ⭐
Q17 : Que signifient les icônes dans les messages d'erreur ?
R : Le simulateur utilise 3 types d'icônes pour vous guider :

❌ Erreur critique : bloque le calcul, vous devez corriger
⚠️ Avertissement : calcul possible mais cas inhabituel, vérifiez vos données
ℹ️ Information : conseil ou suggestion pour améliorer votre simulation

Q18 : Pourquoi les champs enfants sont-ils grisés ?
R : C'est une amélioration UX de la V.04.2.7 maintenue en V.04.2.8 ! Les champs sont automatiquement désactivés (grisés) si les cases "Bonification enfants" ou "Majoration enfants" ne sont pas cochées. Cela évite toute confusion et garantit la cohérence de vos données.
Pour activer les champs :

Cochez la case correspondante
Les champs se dégrisent automatiquement
Saisissez le nombre d'enfants

Q19 : J'ai un message "Incohérence trimestres vs années de carrière", que faire ?
R : Ce message apparaît quand le nombre de trimestres saisi semble incompatible avec votre durée de carrière.
Exemple :

Vous avez 35 ans aujourd'hui et êtes né en 1990
Vous avez commencé à travailler à 22 ans (en 2012)
Durée maximale de carrière : 13 ans = ~52 trimestres maximum
Si vous saisissez 160 trimestres : ❌ incohérence détectée !

Solution : Vérifiez votre relevé de carrière officiel et corrigez la saisie.
Q20 : Le message dit que je peux consulter l'onglet "Analyse Rachat", pourquoi ?
R : Si vos trimestres liquidables sont inférieurs à vos trimestres d'assurance (écart de plusieurs trimestres), cela indique généralement des périodes de temps partiel dans votre passé.
Le simulateur vous suggère intelligemment :

D'aller voir l'onglet "Analyse Rachat"
Pour évaluer s'il est rentable de racheter ces trimestres manquants
Cela augmentera votre pension définitive

Note importante : Rachat ≠ Surcotisation

Surcotisation : pour le temps partiel FUTUR (pendant la progressive)
Rachat : pour rattraper le temps partiel PASSÉ

Q21 : ✨ NOUVEAU V.04.2.8 : Les messages d'erreur sont différents, pourquoi ?
R : La V.04.2.8 a optimisé et hiérarchisé tous les messages d'erreur pour une meilleure expérience utilisateur :
Améliorations :

✅ Priorisation intelligente : les erreurs critiques s'affichent en premier
✅ Messages plus clairs : explication de ce qu'il faut corriger
✅ Détection améliorée : erreurs de saisie détectées plus tôt
✅ Warnings vs erreurs : distinction entre erreurs bloquantes et cas inhabituels

Exemple :

Avant : Plusieurs messages redondants ou mal ordonnés
Après : Message critique prioritaire avec explication claire

Q22 : ✨ NOUVEAU V.04.2.8 : J'ai un warning mais le calcul fonctionne, c'est normal ?
R : Oui ! La V.04.2.8 fait la distinction entre :

❌ Erreurs critiques : bloquent le calcul (ex: date irréaliste)
⚠️ Warnings : cas inhabituel mais calcul possible (ex: âge élevé)

Exemple de warning :
⚠️ Âge actuel inhabituel (75 ans). La retraite progressive concerne généralement les 60-67 ans.
→ Le calcul est effectué, mais vous êtes alerté que votre cas est atypique.

🎯 Conseils d'utilisation avancés
Optimiser votre stratégie de retraite progressive

Testez plusieurs quotités : utilisez le graphique pour visualiser l'impact
Évaluez la surcotisation : selon votre situation fiscale et patrimoniale
Anticipez les changements : vous pouvez modifier votre quotité en cours de route
Planifiez avec la majoration familiale : 3 enfants = +10% de pension
Considérez la surcote parentale : travaillez l'année avant votre âge légal
Analysez le rachat : avec V.04.2.5+, les coûts corrects le rendent plus attractif
Exportez régulièrement : conservez vos simulations en PDF pour comparaison
Faites confiance aux validations : elles vous évitent des erreurs coûteuses (V.04.2.7)
✨ NOUVEAU V.04.2.8 : Lisez attentivement les messages : ils sont hiérarchisés et pédagogiques

Stratégies selon votre profil
Si vous avez une longue carrière :

Privilégiez un départ plus tôt avec quotité basse
La surcotisation est moins intéressante (taux plein déjà atteint)
Le rachat est probablement inutile
Exportez plusieurs scénarios de quotité en PDF

Si vous avez une carrière incomplète :

Envisagez le rachat de trimestres pour éviter la décote
La surcotisation peut être très rentable
Utilisez V.04.2.5+ pour calculer le vrai coût du rachat
Exportez l'analyse rachat en PDF avant de décider
Si le message informatif s'affiche, suivez la suggestion !

Si vous avez des enfants :

Vérifiez vos droits aux bonifications
Optimisez la surcote parentale en travaillant l'année avant l'âge légal
Simulez avec et sans bonifications pour voir l'impact
Les champs sont automatiquement grisés, plus d'erreurs !

Si vous approchez de l'âge légal :

Calculez l'intérêt de poursuivre pour bénéficier de la surcote classique
Comparez avec un départ immédiat
Exportez les deux scénarios en PDF

Si vous envisagez le rachat :

Utilisez impérativement V.04.2.5+ (barèmes corrects)
Simulez différentes options (taux seul vs taux+durée)
Comparez avec l'épargne selon votre TMI
Exportez l'analyse en PDF
Demandez un devis officiel au SRE
Considérez l'avantage fiscal (déductibilité)

✨ NOUVEAU V.04.2.8 : Si vous avez des doutes sur vos données :

Cliquez sur "Calculer" même avec des données approximatives
Lisez attentivement les messages d'erreur hiérarchisés
Les erreurs critiques s'affichent en priorité
Les warnings vous alertent sur des cas inhabituels
Corrigez une par une les incohérences détectées
Les validations optimisées vous guident vers des données cohérentes


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

Ressources complémentaires

info-retraite.fr - Portail commun des régimes de retraite
INSEE - Tables de mortalité


🙏 Remerciements
Ce simulateur gratuit a été développé pour aider les fonctionnaires d'État à mieux comprendre les mécanismes complexes de la retraite progressive et du rachat de trimestres. Il s'appuie sur :

Les textes réglementaires officiels
Les guides du Service des Retraites de l'État
Les retours d'expérience des utilisateurs
Les corrections apportées suite aux vérifications des sources officielles
La collaboration technique avec Claude (Anthropic)

Un merci particulier :

Aux utilisateurs qui ont signalé les inexactitudes concernant l'évolution de la pension provisoire (V.04.2.4)
À l'utilisateur qui a remarqué que les coûts de rachat étaient "très chers", permettant la découverte et la correction de l'erreur majeure sur les barèmes (V.04.2.5)
Aux beta-testeurs qui ont identifié les incohérences de saisie et permis l'ajout des validations (V.04.2.7)
✨ Aux testeurs qui ont remonté les problèmes de validation et permis les corrections critiques (V.04.2.8) ⭐
À Claude (Anthropic) pour l'assistance technique, algorithmique, réglementaire, légale et documentaire dans le développement de ce simulateur

Ces retours ont permis des améliorations majeures qui changent significativement les résultats et les décisions !

📄 Licence et utilisation
Ce simulateur gratuit est fourni à titre informatif et pédagogique. Il ne remplace pas une consultation officielle auprès du SRE ou d'ENSAP.
Utilisation libre pour un usage personnel. La redistribution ou l'utilisation commerciale nécessite une autorisation.
Clause de non-responsabilité : Les résultats fournis sont des estimations. Seuls les calculs officiels du SRE font foi.
⚠️ CE SIMULATEUR NE REMPLACE EN AUCUN CAS LES OUTILS OFFICIELS DE L'ÉTAT
Pour une estimation officielle définitive, consultez toujours ensap.gouv.fr

Version du mode d'emploi : V.04.2.8 - Novembre 2025
Dernière mise à jour : Corrections critiques des validations + messages optimisés et hiérarchisés
Prochaine mise à jour prévue : Tests approfondis et documentation des cas limites (Q1 2026)

Développé par Jean-Michel DI PACO avec l'assistance de Claude (Anthropic)

Contact : maviclearn@gmail.com
