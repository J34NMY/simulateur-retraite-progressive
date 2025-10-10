# 📖 Mode d'emploi du Simulateur de Retraite Progressive V.04.2.7

## 🎯 Introduction

Ce simulateur gratuit vous permet d'estimer votre pension de retraite progressive et définitive en tant que fonctionnaire d'État. Il applique la méthode officielle du Service des Retraites de l'État (SRE) avec une transparence totale sur les calculs.

**✨ NOUVEAU V.04.2.7 :** 31 validations de cohérence pour garantir la qualité de vos données et vous guider en cas d'erreur.

---

*Vous devez avant toutes choses récupérer votre relevé de carrière sur le site info retraite*

## 🚀 Démarrage rapide

### Installation
1. **Téléchargez** le fichier `simulateur_retraite_V.04.2.7.html`
2. **Double-cliquez** dessus pour l'ouvrir dans votre navigateur
3. Aucune installation, aucune connexion internet requise !

### Premier calcul en 3 étapes
1. **Acceptez** les conditions d'utilisation (bannière d'avertissement)
2. **Onglet "Paramètres"** → Remplissez vos données
3. Cliquez sur **"Calculer la simulation"**
4. **Onglet "Résultats RP"** → Consultez vos résultats
5. **Exportez en PDF** si vous souhaitez conserver les résultats

---

## 🆕 Nouveautés V.04.2.7 - Validation des données

### ✅ 31 contrôles de cohérence automatiques

Le simulateur vérifie désormais automatiquement la cohérence de vos données et vous alerte en cas d'anomalie.

**Avantages :**
- ✅ Détection immédiate des erreurs de saisie
- ✅ Messages pédagogiques avec suggestions de correction
- ✅ Basculement automatique vers l'onglet Résultats en cas d'erreur
- ✅ Meilleure qualité des simulations

### 📋 Liste des validations par catégorie

#### **1. Validations des dates (9 contrôles)**

| Validation | Exemple d'erreur | Message affiché |
|------------|------------------|-----------------|
| Date relevé < Date départ progressif | Relevé : 31/12/2024, Départ : 01/01/2024 | ❌ La date de départ progressif doit être APRÈS la date du relevé |
| Date départ progressif < Date départ définitif | Les deux dates identiques | ❌ La date de départ définitif doit être APRÈS la date de départ progressif |
| Date naissance avant 1900 | Naissance : 01/01/1890 | ❌ Date de naissance irréaliste (1890). Veuillez vérifier votre saisie. |
| Dates dans futur lointain | Départ : 01/01/2090 | ❌ Date de départ irrréaliste (2090). Vérifiez votre saisie. |
| Âge actuel > 80 ans | Naissance : 01/01/1940 | ⚠️ Âge actuel inhabituel (85 ans). La retraite progressive concerne généralement les 60-67 ans. |
| Âge actuel < 40 ans | Naissance : 01/01/2000 | ⚠️ Âge actuel très jeune (25 ans). La retraite progressive est accessible à partir de 60 ans. |
| Âge départ progressif > 80 ans | Départ à 85 ans | ❌ Âge au départ progressif irréaliste (85 ans). Maximum réglementaire : 70 ans. |
| Départ après 67 ans | Départ à 68 ans | ⚠️ Départ après 67 ans : vous devrez obtenir une prolongation d'activité |
| Départ après 70 ans | Départ à 72 ans | ❌ Départ après 70 ans impossible : limite d'âge maximale dépassée |

#### **2. Validations trimestres/jours (4 contrôles)**

| Validation | Exemple d'erreur | Message affiché |
|------------|------------------|-----------------|
| Trimestres vs années de carrière | 160 trim pour 12 ans de carrière | ❌ Incohérence : 160 trimestres d'assurance pour environ 12 ans de carrière possible |
| Jours négatifs | Jours assurance : -10 | ❌ Les jours d'assurance ne peuvent pas être négatifs |
| Jours >= 90 | Jours liquidables : 95 | ❌ Les jours liquidables doivent être < 90 (90 jours = 1 trimestre) |
| Liquidables > Assurance | Liquidables : 150, Assurance : 140 | ❌ Les trimestres liquidables ne peuvent pas être > aux trimestres d'assurance |

#### **3. Validations indices/valeurs (3 contrôles)**

| Validation | Exemple d'erreur | Message affiché |
|------------|------------------|-----------------|
| Indice hors plage | Indice : 1200 | ⚠️ Indice majoré inhabituel (1200). Plage normale FP État : 350-900 |
| Valeur point incorrecte | Valeur : 6.00€ | ⚠️ Valeur du point inhabituelle (6.00€). Valeur officielle 2025 : 4,92278€ |
| Trimestres requis aberrants | Trimestres requis : 200 | ❌ Trimestres requis incorrects (200). Plage normale : 150-180 trimestres |

#### **4. Validations enfants (4 contrôles + UX)**

| Validation | Exemple d'erreur | Message affiché |
|------------|------------------|-----------------|
| Case cochée + 0 enfants | Bonification cochée, 0 enfants saisis | ❌ Case "Bonification enfants avant 2004" cochée mais aucun enfant saisi |
| Enfants saisis sans case | 2 enfants saisis, case non cochée | ❌ Vous avez saisi des enfants avant 2004 mais la case n'est pas cochée |
| Total ≠ somme | Total : 3, Avant 2004 : 1, Après 2003 : 1 | ❌ Incohérence : total enfants (3) ≠ somme des enfants saisis (2) |
| Champs actifs/grisés | - | ✨ Les champs sont automatiquement grisés si les cases ne sont pas cochées |

#### **5. Validations durée période progressive (2 contrôles)**

| Validation | Exemple d'erreur | Message affiché |
|------------|------------------|-----------------|
| Période < 1 mois | 15 jours entre départ progressif et définitif | ⚠️ Attention : période de retraite progressive très courte (moins d'1 mois) |
| Période > 5 ans | 6 ans entre départ progressif et définitif | ⚠️ Période de retraite progressive très longue (6.0 ans). Cas inhabituel. |

#### **6. Validations Retraite Définitive (9 contrôles)**

| Validation | Exemple d'erreur | Message affiché |
|------------|------------------|-----------------|
| Données non récupérées | Clic sur "Calculer" sans récupérer | ❌ Veuillez d'abord récupérer les données du simulateur |
| Date départ obligatoire | Champ vide | La date de départ en retraite est obligatoire |
| Date départ > date relevé | Date incohérente | ❌ La date de départ doit être APRÈS la date du relevé |
| Date dans le passé | Date : 01/01/2020 | ❌ Date de départ dans le passé. Vérifiez votre saisie. |
| Date futur lointain | Date : 01/01/2090 | ❌ Date de départ irréaliste (2090). Vérifiez votre saisie. |
| Âge au départ | Âge : 55 ans ou 85 ans | ❌ Âge au départ trop jeune (55 ans). Minimum : 60 ans |
| Quotité invalide | Quotité : 1.2 | La quotité doit être entre 0 et 1 (ex: 0.8 pour 80%) |
| Surcotisation + 100% | Surcotisation cochée + Quotité 100% | ❌ La surcotisation n'est possible que pendant les périodes à temps partiel |
| Durée projection | Période négative ou très longue | ⚠️ Période de projection très longue (6.2 ans). Cas inhabituel. |

### 🎨 Comment utiliser les validations

**1. Remplissez vos données normalement**

**2. Cliquez sur "Calculer la simulation"**

**3. Si des erreurs sont détectées :**
- Le simulateur bascule automatiquement vers l'onglet "Résultats RP"
- Un encadré orange liste toutes les erreurs détectées
- Chaque erreur est accompagnée d'une icône :
  - ❌ = Erreur critique (bloque le calcul)
  - ⚠️ = Avertissement (calcul possible mais cas inhabituel)
  - ℹ️ = Information (suggestion)

**4. Corrigez les erreurs signalées**

**5. Re-cliquez sur "Calculer la simulation"**

### 💡 Messages informatifs intelligents

**Message "Liquidables < Assurance" (Retraite Définitive)**

Si vos trimestres liquidables sont inférieurs à vos trimestres d'assurance, le simulateur affiche automatiquement :
ℹ️ Trimestres liquidables inférieurs à l'assurance
Écart détecté : 18.5 trimestres.
Cela indique des périodes de temps partiel dans votre passé.
💡 Pour rattraper ces trimestres, consultez l'onglet "Analyse Rachat".

Ce message vous oriente directement vers la solution !

---

## 📊 Guide des onglets

### 1️⃣ Onglet PARAMÈTRES

#### Section "Données du relevé de carrière"

**Date du relevé**
- Date de votre dernier relevé de carrière officiel SRE
- Format : JJ/MM/AAAA
- Exemple : 31/12/2024

**Trimestres d'assurance au relevé**
- Nombre total de trimestres d'assurance selon votre relevé SRE
- Exemple : 160 trimestres + 84 jours
- Les trimestres d'assurance comptent pour la durée de cotisation (évitent la décote)

**Trimestres liquidables au relevé**
- Nombre de trimestres de services effectifs selon votre relevé SRE
- Exemple : 142 trimestres + 86 jours
- Les trimestres liquidables déterminent le montant de la pension (prorata)

#### Section "Informations personnelles"

**Date de naissance**
- Obligatoire pour calculer l'âge légal et les trimestres requis
- Détermine automatiquement votre génération (1964 → 171 trimestres requis)

**Sexe**
- Utilisé uniquement pour l'analyse actuarielle de rentabilité
- Basé sur les tables de mortalité INSEE 2024

**Trimestres requis**
- Calculé automatiquement selon votre année de naissance
- 1965 et après → 172 trimestres
- 1964 → 171 trimestres, etc.

**Indice majoré (IM)**
- Votre indice majoré actuel
- Exemple : 478
- Attention à la règle des six mois : une augmentation d'indice doit avoir au moins 6 mois d'ancienneté avant le départ

**Valeur du point**
- Valeur officielle : **4,92278 €** (depuis le 1er juillet 2023)
- Mise à jour annuelle en général

#### Section "Planning de retraite progressive"

**Date de départ retraite progressive**
- Date de début de votre retraite progressive
- Conditions : minimum 60 ans + 150 trimestres d'assurance

**Date de départ retraite définitive**
- Date de fin de la période progressive
- Entre cette date et le départ progressif, vous cumulez traitement partiel + pension provisoire

**Quotité entre relevé et départ progressif**
- Votre quotité de travail ACTUELLE (avant la retraite progressive)
- 100% = temps plein
- 80% = 4 jours/semaine
- Cette quotité impacte l'accumulation de trimestres liquidables

**Quotité pendant la retraite progressive**
- Votre quotité pendant la période progressive
- Choix : 50%, 60%, 70%, 80%, 90%
- Attention : cette quotité impacte la surcote parentale

**Appliquer le Décret n°82-624**
- **Coché par défaut** (cas majoritaire)
- Concerne certains fonctionnaires en temps partiel de droit commun :
  - **80%** → rémunération à **6/7ème** (≈85,71%)
  - **90%** → rémunération à **32/35ème** (≈91,43%)

**Comment vérifier si cela vous concerne ?**
1. Consultez votre fiche de paie actuelle si vous êtes déjà à temps partiel 80% ou 90%
2. Regardez la ligne "Traitement Brut"
3. Si vous travaillez 4j/5 (80%) et êtes payé plus de 80%, le décret s'applique
4. Si incertain, laissez coché (cas par défaut)

#### Section "Options de surcotisation"

**Surcotisation pendant la progressive**
- Si coché : vos trimestres liquidables comptent à 100% (même à temps partiel)
- Coût supplémentaire selon barème 2024 (ex: 16,2% pour 80%)
- Une analyse de rentabilité complète sera affichée

**Taux de surcotisation**
- Calculé automatiquement selon votre quotité
- Barème 2024 :
  - 50% → 23,85%
  - 60% → 21,30%
  - 70% → 18,75%
  - 80% → 16,20%
  - 90% → 13,65%

**Taux de placement alternatif**
- Pour comparer la surcotisation avec un placement financier
- Options : Livret A (3%), LEP (4%), placements dynamiques (4,5-5%)

#### Section "Droits liés aux enfants"

**✨ NOUVEAU V.04.2.7 : Gestion automatique des champs**

Les champs sont maintenant **automatiquement grisés** si les cases ne sont pas cochées, pour éviter toute confusion.

**Bonification enfants nés/adoptés avant 2004**
- **Conditions strictes** :
  - Enfant né ou adopté avant le 1er janvier 2004
  - Interruption ou réduction d'activité ≥ 2 mois consécutifs
  - Enfant élevé pendant ≥ 9 ans avant ses 16 ans
- **Gain** : 4 trimestres liquidables + 4 trimestres assurance PAR ENFANT
- Validation lors de la demande de retraite avec justificatifs

**Majoration enfants nés/adoptés à partir de 2004**
- **Conditions** :
  - Enfant né ou adopté à partir du 1er janvier 2004
  - Après recrutement dans la fonction publique
- **Gain** : 2 trimestres d'assurance PAR ENFANT (pas de liquidables)
- Attribution automatique

**Total enfants (majoration familiale)**
- Calculé automatiquement
- **Majoration de pension** :
  - 3 enfants → +10%
  - 4 enfants → +15%
  - 5 enfants → +20%, etc.
- Condition : enfants élevés 9 ans avant leurs 16 ans

#### Section "Information pension provisoire"

Un encadré informatif explique le fonctionnement de la pension provisoire :

**Calculée au départ** : basée sur les droits acquis AVANT le départ progressif

**Évolution possible** : si vous changez de quotité pendant la progressive, la part versée s'ajuste automatiquement
- Exemple : passage de 80% → 70% de travail
- Pension provisoire passe de 20% → 30% du montant de référence

**Trimestres pendant la progressive** : ne modifient PAS le montant provisoire
- Les nouveaux trimestres acquis sont comptabilisés
- Mais le montant de référence reste fixe

**Recalcul à la retraite définitive** : tous les droits acquis pendant la progressive seront pris en compte dans le calcul final

---

### 2️⃣ Onglet RÉSULTATS RP (Retraite Progressive)

#### Durées et trimestres
- Affiche les périodes calculées avec la méthode SRE (base 360 jours/an)
- Décomposition : années, mois, jours

#### Compteurs au départ progressif
- État de vos compteurs à la date de départ en retraite progressive
- Assurance vs Liquidables
- Bonifications prises en compte

#### Revenus pendant la retraite progressive
- **Traitement à la quotité** : votre salaire partiel
- **Pension provisoire** : (1 - quotité) × pension de référence
- **Note importante** : une mention indique que si vous changez de quotité, la pension s'ajustera
- **Total brut mensuel** : traitement + pension
- Si surcotisation : affichage du coût mensuel et du net après surcotisation

#### Analyse de surcotisation (si activée)
Comparaison détaillée :
- **Coût total** de la surcotisation
- **Gain mensuel** de pension (surcotisation vs sans)
- **Durée de rentabilisation** (combien d'années de retraite pour récupérer l'investissement)
- **Alternative placement** :
  - Capital après période progressive
  - Rente mensuelle générée
  - Capital préservé et transmissible
- **Recommandation** : FAVORABLE / NEUTRE / DÉFAVORABLE

#### Situation en fin de période
- Assurance et liquidables finaux
- Taux de liquidation estimé
- Traitement de référence

#### Pension définitive estimée
- **Montant principal** en gros caractères verts
- **Avec majoration familiale** si applicable

#### Détails décote/surcote
- **Si décote** : trimestres manquants, taux appliqué, date du taux plein
- **Si surcote** : détail des 3 types de majorations SRE
  - Surcote parentale (max 5%)
  - Surcote classique (après âge légal)
  - Majoration excédentaire (trimestres restants)

#### Export PDF des résultats
- **Bouton "Télécharger les résultats en PDF"** en bas de page
- Génère un document professionnel avec :
  - En-tête avec version et date
  - **Avertissement NON OFFICIEL** en première page
  - Tous les paramètres de simulation
  - Résultats détaillés
  - Analyses de rentabilité
  - Avertissements et disclaimers
  - Mention **ensap.gouv.fr** pour estimation officielle
- Format A4 optimisé pour impression
- **Accents français parfaitement préservés** (support natif jsPDF 2.5.1)
- Nom du fichier : `simulation_retraite_progressive_YYYY-MM-DD.pdf`

---

### 3️⃣ Onglet RETRAITE DÉFINITIVE

Cet onglet permet de simuler une retraite définitive **sans période de retraite progressive**.

#### Mode d'emploi

1. **Cliquez sur "Récupérer les données"**
   - Importe automatiquement vos paramètres depuis l'onglet Paramètres
   - Affiche votre situation actuelle

2. **Définissez votre projection**
   - **Date de départ en retraite** : quand souhaitez-vous partir ?
   - **Quotité envisagée** : à quel temps travaillerez-vous jusqu'au départ ?
     - 100% = temps plein jusqu'à la retraite
     - 80% = 4j/5 jusqu'à la retraite
     - etc.

3. **Options**
   - **Décret n°82-624** : même principe que l'onglet Paramètres
   - **Surcotisation** : si temps partiel, option de surcotiser pour compter les liquidables à 100%

4. **Cliquez sur "Calculer la simulation"**

#### **✨ NOUVEAU V.04.2.7 : 9 validations automatiques**

Le simulateur vérifie automatiquement :
- ✅ Données récupérées du simulateur
- ✅ Date de départ obligatoire et cohérente
- ✅ Âge au départ valide (60-80 ans)
- ✅ Quotité valide
- ✅ Surcotisation + 100% interdite
- ✅ Durée de projection cohérente

**Message informatif intelligent :**

Si vos trimestres liquidables sont < à vos trimestres d'assurance, un message s'affiche :
ℹ️ Trimestres liquidables inférieurs à l'assurance
Écart détecté : 18.5 trimestres.
Cela indique des périodes de temps partiel dans votre passé.
💡 Pour rattraper ces trimestres, consultez l'onglet "Analyse Rachat".

#### Résultats affichés

**Projection de carrière**
- Période entre aujourd'hui et le départ
- Trimestres acquis pendant cette période
- Impact de la quotité choisie

**Trimestres au départ**
- Assurance totale / Liquidables totaux
- Bonifications enfants prises en compte
- Âge au départ

**Analyse de surcotisation** (si activée)
- Même analyse que pour la retraite progressive
- Coût sur toute la période jusqu'au départ
- Comparaison avec placement alternatif

**Pension définitive**
- Montant estimé selon le scénario choisi
- Avec/sans majoration familiale

**Graphique comparatif en barres**
- Compare automatiquement 6 scénarios de quotité (50%, 60%, 70%, 80%, 90%, 100%)
- La barre rouge = votre quotité sélectionnée
- Permet de visualiser l'impact d'un changement de quotité

#### Export PDF de la simulation
- **Bouton "Télécharger les résultats en PDF"** en bas de page
- Document avec :
  - **Avertissement NON OFFICIEL** en première page
  - Données récupérées du simulateur
  - Projection jusqu'au départ
  - Trimestres au départ
  - Pension définitive estimée
  - Analyses de surcotisation si applicable
  - Mention **ensap.gouv.fr** répétée
- **Accents français parfaitement préservés**
- Nom du fichier : `simulation_retraite_definitive_YYYY-MM-DD.pdf`

---

### 4️⃣ Onglet GRAPHIQUE

**Graphique en ligne** : Revenus pendant la retraite progressive

- Compare vos **revenus totaux bruts** selon différentes quotités (50% à 90%)
- Le point rouge indique votre quotité sélectionnée
- Permet de voir rapidement l'impact financier d'un changement de quotité

**Comment l'interpréter ?**
- Plus la quotité est basse → plus le revenu total est faible (logique)
- Mais le gain en temps libre peut compenser
- À utiliser pour trouver votre équilibre vie/revenus

---

### 5️⃣ Onglet ANALYSE RACHAT - CORRIGÉ V.04.2.5

Cet onglet analyse la **rentabilité du rachat de trimestres** avec les **coefficients corrects de la Fonction Publique d'État**.

#### CHANGEMENT MAJEUR V.04.2.5

**Ancienne version (V.04.2.4 et antérieures) :**
- Utilisait les barèmes du secteur privé
- Coûts 2 à 3 fois trop élevés
- Exemple : 4 trim. à 40 ans = 15 200 € (FAUX)

**Nouvelle version (V.04.2.5+) :**
- Utilise les coefficients Fonction Publique d'État
- Calcul basé sur votre traitement indiciaire
- Exemple : 4 trim. à 40 ans = 5 836 € (CORRECT)

#### Mode d'emploi

1. **Cliquez sur "Récupérer les données"**
   - Importe votre situation depuis l'onglet Paramètres

2. **Paramétrez votre rachat**
   - **Nombre de trimestres** : entre 1 et 12
   - **Type de rachat** :
     - Années d'études supérieures
     - Années civiles incomplètes
   - **Option de rachat** :
     - **Option 1 - Taux seul** : moins cher, évite la décote uniquement
     - **Option 2 - Taux + Durée** : plus cher, augmente aussi la pension
   - **Âge au rachat** : votre âge actuel ou prévu
   - **TMI** : votre tranche marginale d'imposition (pour calculer l'économie fiscale)

3. **Taux de placement alternatif**
   - Pour comparer avec un placement financier
   - Ex: Livret A 3%, LEP 4%, placements dynamiques 5%

4. **Cliquez sur "Analyser la rentabilité"**

#### Résultats affichés

**Coût du rachat**
- **Coefficient appliqué** : pourcentage de votre traitement (CORRIGÉ V.04.2.5)
- Coût par trimestre (basé sur votre traitement indiciaire)
- Coût nominal (brut)
- Économie d'impôt (le rachat est déductible)
- **Coût réel** après déduction fiscale

**Impact sur la pension**
- Gain mensuel de pension
- Gain annuel
- **Durée de rentabilisation** : combien d'années de retraite pour récupérer l'investissement

**Comparaison avec placement**
- **Rachat** : gain viager, non transmissible
- **Placement** : capital préservé, transmissible, rente mensuelle

**Recommandation**
- FAVORABLE : le rachat est rentable
- NEUTRE : les deux se valent
- DÉFAVORABLE : le placement est préférable

**Points d'attention**
- Espérance de vie
- Liquidité des fonds
- Transmission patrimoniale
- Protection contre l'inflation

**Important** : Les coefficients affichés sont indicatifs (basés sur 2024, catégorie sédentaire). Demandez toujours un devis officiel au SRE via [ensap.gouv.fr](https://ensap.gouv.fr).

#### Export PDF de l'analyse
- **Bouton "Télécharger l'analyse en PDF"** en bas de page
- Document complet avec :
  - **Avertissement COÛTS INDICATIFS** en première page
  - Données récupérées
  - Paramètres du rachat
  - Coût détaillé du rachat
  - Impact sur la pension
  - Comparaison avec placement
  - Recommandation personnalisée
  - Points d'attention
  - Mention **ensap.gouv.fr** pour devis officiel
- **Accents français parfaitement préservés**
- Nom du fichier : `analyse_rachat_trimestres_YYYY-MM-DD.pdf`

#### Comprendre les coefficients Fonction Publique

**Formule de calcul :**
Coût par trimestre = Traitement indiciaire × Coefficient d'âge

**Coefficients indicatifs (base 2024) :**

| Âge | Option 1 (Taux seul) | Option 2 (Taux + Durée) |
|-----|---------------------|------------------------|
| 30 ans | ~28% | ~50% |
| 40 ans | ~35% | ~62% |
| 50 ans | ~48% | ~85% |
| 60 ans | ~85% | ~150% |

**Exemple concret :**
- Vous avez 42 ans
- Traitement indiciaire : 2 353 €
- Option 2 (Taux + Durée)
- Coefficient interpolé : ~64%

**Calcul :**
- Coût par trimestre : 2 353 × 0,64 = **1 506 €**
- Pour 4 trimestres : 1 506 × 4 = **6 024 €**
- Économie d'impôt (TMI 30%) : 6 024 × 0,30 = 1 807 €
- **Coût réel** : 6 024 - 1 807 = **4 217 €**

**Comparaison V.04.2.4 vs V.04.2.5 :**
- V.04.2.4 (FAUX) : 15 200 € → 10 640 € après impôt
- V.04.2.5 (CORRECT) : 6 024 € → 4 217 € après impôt
- **Économie : 6 423 €** (division par 2,5)

---

### 6️⃣ Onglet SOURCES

Références réglementaires complètes :
- Code des pensions civiles et militaires
- Décrets applicables (dont Décret 2007-262 sur le rachat)
- Liens vers sites officiels
- Méthode de calcul SRE détaillée
- **Tableau des coefficients rachat Fonction Publique** (V.04.2.5)
- **Section mise à jour** sur la pension provisoire avec l'explication correcte
- Avertissement sur la précision du simulateur

---

### 7️⃣ Onglet MENTIONS LÉGALES

#### Nature de l'outil
- Simulateur **gratuit** et **pédagogique**
- **NON OFFICIEL** - ne remplace pas ENSAP
- Ne constitue pas un conseil financier
- Outil éducatif pour comprendre les mécanismes

#### Développement et responsabilité

**Éditeur du simulateur**
- Développé par : Jean-Michel DI PACO
- Avec l'assistance technique de : **Claude (Anthropic)** - Intelligence artificielle conversationnelle
- Version : V.04.2.7
- Dernière mise à jour : Octobre 2025
- Contact : maviclearn@gmail.com

**Collaboration avec Claude (Anthropic)**

Ce simulateur a été développé en collaboration avec Claude, l'assistant IA d'Anthropic, pour les aspects :

- **Algorithmiques** : Implémentation rigoureuse des calculs SRE conformes aux textes réglementaires
- **Techniques** : Architecture du code, gestion des exports PDF, optimisation, système de validation
- **Réglementaires** : Interprétation et application des décrets et du Code des pensions
- **Légaux** : Rédaction des mentions légales, CGU, disclaimers adaptés au modèle gratuit
- **Documentaires** : Rédaction du mode d'emploi et de la documentation technique

**L'éditeur assume l'entière responsabilité** du contenu, de l'exactitude des calculs et de la conformité réglementaire.

#### Conditions d'utilisation
- Utilisation gratuite
- Limitation de responsabilité
- Non-opposabilité des résultats
- Recommandation forte de consulter **ensap.gouv.fr**

#### Avertissement important

**Écart technique documenté :**
- Ce simulateur applique rigoureusement la méthodologie de calcul SRE documentée publiquement (base 360 jours/an, règles d'arrondi standard)
- Un écart de **1 à 2 trimestres liquidables** peut exister avec le calcul officiel du SRE/ENSAP
- **Cause probable** : Règles d'arrondi intermédiaires ou modalités de calcul spécifiques non documentées publiquement par le SRE
- **Impact estimé** : Environ 1 à 2% du montant final de la pension

**⚠️ CE SIMULATEUR NE REMPLACE EN AUCUN CAS LES OUTILS OFFICIELS DE L'ÉTAT**

Seules les simulations effectuées sur **ensap.gouv.fr** ont valeur légale.

**Pour votre estimation officielle définitive :** Consultez obligatoirement [ensap.gouv.fr](https://ensap.gouv.fr) ou contactez directement le Service des Retraites de l'État.

#### Données personnelles
- **Aucune donnée collectée**
- Calculs 100% locaux dans le navigateur
- Pas de transmission de données
- Pas de cookies (sauf hébergement)

#### Propriété intellectuelle
- Code protégé par droit d'auteur
- Usage personnel autorisé
- Usage commercial interdit sans autorisation

#### Validation et démarche qualité

**Phase de validation en cours**
- Ce simulateur est actuellement en phase de beta test auprès de fonctionnaires d'État
- Comparaison systématique avec simulations ENSAP officielles
- Documentation des écarts observés
- Amélioration continue basée sur les retours

**Démarche qualité**
- Application stricte des textes réglementaires
- Corrections rapides suite aux retours utilisateurs
- Documentation exhaustive des sources
- Transparence sur les limitations
- Disclaimers clairs et visibles
- Aucune collecte de données personnelles
- **31 validations de cohérence** (V.04.2.7) ⭐

---

## 📄 Fonctionnalités des exports PDF - V.04.2.6+

### Amélioration majeure V.04.2.6

**Support natif des accents français**
- **jsPDF 2.5.1** supporte nativement tous les caractères accentués français
- Plus besoin de fonction de conversion
- Accents parfaitement préservés dans les PDFs : é, è, à, ç, ù, etc.
- Compatible tous systèmes (Windows, Mac, Linux, mobile)
- Garantit une lisibilité universelle

**Différence avec V.04.2.5.1 :**
- V.04.2.5.1 : Fonction `nettoyerPourPDF()` pour convertir les accents
- V.04.2.6+ : Support natif, plus besoin de conversion

### Format des documents

**Caractéristiques techniques**
- Format A4 (210 × 297 mm)
- Marges optimisées (20mm)
- Pagination automatique
- En-têtes et pieds de page professionnels
- **Accents français natifs** (pas de conversion)

**Contenu des exports**

1. **Export Résultats RP** (Retraite Progressive)
   - En-tête avec titre, version, date
   - **Avertissement NON OFFICIEL** en première page (encadré orange)
   - Mention **ensap.gouv.fr** pour estimation officielle
   - Section Paramètres de simulation
   - Section Résultats détaillés
   - Analyses de rentabilité si applicable
   - Avertissements et disclaimers
   - Mention "Simulation non contractuelle"

2. **Export Retraite Définitive**
   - **Avertissement NON OFFICIEL** en première page
   - Données récupérées du simulateur
   - Projection jusqu'au départ
   - Trimestres au départ
   - Pension définitive estimée
   - Analyses de surcotisation si applicable
   - Mention **ensap.gouv.fr** répétée

3. **Export Analyse Rachat**
   - **Avertissement COÛTS INDICATIFS** en première page (encadré orange)
   - Coût du rachat avec coefficients
   - Impact sur la pension
   - Comparaison avec placement
   - Recommandation
   - Avertissement sur caractère indicatif
   - Mention **ensap.gouv.fr** pour devis officiel

**Génération du PDF**
- Bibliothèque : jsPDF 2.5.1
- Génération instantanée côté client
- **Accents français parfaitement préservés**
- Nom de fichier automatique avec date : `simulation_type_YYYY-MM-DD.pdf`
- Téléchargement direct dans votre dossier de téléchargements

**Utilisation recommandée**
- Conserver vos simulations pour comparaison
- Partager avec un conseiller retraite
- Documenter votre réflexion
- Imprimer pour consultation papier
- **Les PDFs sont maintenant parfaitement lisibles partout**

---

## 🔧 Fonctionnalités avancées

### Import/Export de simulations

**Exporter vos paramètres**
1. Remplissez l'onglet Paramètres
2. Cliquez sur **"Exporter"**
3. Un fichier JSON est téléchargé : `parametres_simulateur_retraite_v04_2_7.json`
4. Conservez ce fichier pour le réutiliser plus tard

**Importer des paramètres**
1. Cliquez sur **"Importer"**
2. Sélectionnez un fichier JSON précédemment exporté
3. Tous les champs sont automatiquement remplis

Utile pour comparer plusieurs scénarios ou partager avec un conseiller

### Bouton "Valeurs par défaut"
- Réinitialise tous les champs avec l'exemple par défaut
- Utile pour tester le simulateur ou repartir de zéro

---

## 🤝 Développement et validation

### Collaboration avec Claude (Anthropic)

Ce simulateur a été développé en **collaboration avec Claude**, l'assistant IA d'Anthropic, pour les aspects suivants :

**Aspects algorithmiques**
- Implémentation rigoureuse de la méthode SRE (base 360 jours/an)
- Calculs conformes aux textes réglementaires
- Gestion des arrondis et cas particuliers
- Algorithmes d'interpolation pour les coefficients de rachat
- **Système de validation exhaustif** (V.04.2.7) ⭐

**Aspects techniques**
- Structure et architecture du code JavaScript
- Gestion des exports PDF avec jsPDF 2.5.1
- Support natif des accents français (V.04.2.6)
- Optimisation des performances
- Compatibilité multi-navigateurs
- **31 validations de cohérence** (V.04.2.7) ⭐

**Aspects réglementaires**
- Interprétation des textes de loi (Code des pensions, décrets)
- Application correcte des règles de calcul SRE
- Identification des coefficients Fonction Publique d'État
- Documentation des sources réglementaires

**Aspects légaux**
- Rédaction des mentions légales complètes
- Conditions d'utilisation adaptées au modèle gratuit
- Disclaimers appropriés et visibles partout
- Politique de confidentialité
- Avertissements renforcés (V.04.2.6)

**Documentation**
- Rédaction du mode d'emploi complet
- Création du README.md technique
- Explications pédagogiques des calculs
- FAQ et cas d'usage
- **Documentation des validations** (V.04.2.7) ⭐

**L'éditeur assume l'entière responsabilité** du contenu, de l'exactitude des calculs et du respect de la réglementation.

### Approche de validation

**Modèle gratuit et éducatif**
- Outil mis à disposition **gratuitement** sans contrepartie
- Vocation **pédagogique** : comprendre les mécanismes
- Ne remplace pas les outils officiels (ENSAP)
- Transparence totale sur la méthode de calcul

**Phase de validation en cours** (V.04.2.7)
- Recrutement de 10-15 fonctionnaires testant leurs cas réels
- Comparaison systématique avec simulations ENSAP officielles
- Documentation des écarts constatés
- Amélioration continue basée sur les retours
- Mention correcte : "Phase de validation en cours" (et non "testé par X fonctionnaires")

**Écart documenté avec le SRE**
- Écart connu : **1-2 trimestres liquidables** (~1-2% de pension)
- Cause probable : règles d'arrondi internes non documentées publiquement
- Le simulateur applique la méthode SRE documentée publiquement
- Pour une estimation officielle : **toujours consulter ensap.gouv.fr**
- **Cet avertissement est présent partout** : bannière, résultats, PDFs, footer

**Corrections majeures grâce aux utilisateurs**
- V.04.2.4 : Correction pension provisoire (évolution quotité)
- V.04.2.5 : Correction barèmes rachat (division coûts par 2,5)
- V.04.2.6 : Support natif accents PDF + avertissements renforcés
- V.04.2.7 : 31 validations de cohérence + UX améliorée ⭐

### Démarche qualité

- Application stricte des textes réglementaires
- Corrections rapides suite aux signalements
- Documentation exhaustive des sources
- **Transparence maximale = protection juridique** (V.04.2.6)
- **Avertissements renforcés partout** (V.04.2.6)
- **Validations exhaustives** (V.04.2.7) ⭐
- Disclaimers clairs et visibles
- Aucune collecte de données personnelles
- Code maintenu et mis à jour

---

## ⚠️ Points d'attention importants

### 1. Non-opposabilité des résultats - RAPPEL RENFORCÉ V.04.2.6

| Ce simulateur | Simulateur officiel SRE |
|:--------------|:------------------------|
| Aide à la décision | **Référence légale** |
| Transparence totale | Calcul exact mais opaque |
| Écart possible 1-2% | **Seul résultat opposable** |
| **GRATUIT et ÉDUCATIF** | **OFFICIEL** |

**⚠️ CE SIMULATEUR NE REMPLACE EN AUCUN CAS LES OUTILS OFFICIELS DE L'ÉTAT**

**Pour une estimation officielle définitive, consultez toujours [ensap.gouv.fr](https://ensap.gouv.fr)**

### 2. Écart connu avec le SRE

- Écart estimé : **1 à 2 trimestres liquidables** (~1-2% de pension)
- Cause probable : règles d'arrondi internes non documentées publiquement
- Ce simulateur applique rigoureusement la méthode SRE documentée
- **Cet avertissement est présent partout dans le simulateur** (V.04.2.6)

### 3. Rachat de trimestres - Coefficients indicatifs

**Important V.04.2.5 (toujours d'actualité en V.04.2.7) :**
- Les coefficients utilisés sont indicatifs (base 2024, catégorie sédentaire)
- Le coût exact dépend de nombreux paramètres :
  - Votre traitement indiciaire au moment du rachat
  - Votre catégorie (sédentaire, actif, insalubre)
  - Les barèmes en vigueur à la date du rachat
  
**Pour un devis personnalisé et opposable, contactez toujours le SRE via [ensap.gouv.fr](https://ensap.gouv.fr)**

### 4. Règle des six mois

Une augmentation d'indice majoré doit avoir au moins **6 mois d'ancienneté** avant le départ en retraite pour être prise en compte.

**Exemple** :
- Départ prévu : 1er décembre 2025
- Nouvelle augmentation d'indice : 1er novembre 2025
- Cette augmentation ne compte PAS (seulement 1 mois)

### 5. Décret n°82-624

Ce décret s'applique à **certains** fonctionnaires en temps partiel de droit commun :
- Pas applicable aux temps partiels thérapeutiques
- Pas applicable à tous les statuts
- Vérifiez sur votre fiche de paie actuelle

**En cas de doute** : laissez la case cochée (cas majoritaire)

### 6. Surcotisation

La surcotisation est **rentable** si :
- Vous partez longtemps en retraite (espérance de vie élevée)
- Le taux de placement alternatif est faible
- Vous valorisez la sécurité viagère

Elle est **moins intéressante** si :
- Vous avez une épargne bien rémunérée
- Vous souhaitez conserver la liquidité des fonds
- Vous voulez transmettre un capital

### 7. Pension provisoire pendant la retraite progressive

**Important à comprendre :**

**CE QUI EST VRAI :**
- La pension provisoire est calculée à la date du départ progressif
- Elle est basée sur les droits acquis AVANT le départ progressif
- **SI vous changez de quotité**, la part versée s'ajuste automatiquement
  - Exemple : passage de 80% → 70% de travail
  - Pension provisoire passe de 20% → 30%
- Les trimestres acquis pendant la progressive sont comptabilisés pour la retraite définitive

**CE QUI EST FAUX :**
- La pension provisoire ne se recalcule PAS en fonction des nouveaux trimestres acquis pendant la progressive
- Le montant de référence de la pension reste celui calculé au départ progressif
- Seul le **pourcentage** de cette pension peut varier si la quotité change

**Exemple concret :**
- Départ progressif : 142 trimestres liquidables
- Pension de référence calculée : 1 457 €
- Quotité 80% → pension provisoire : 20% × 1 457 € = **291 €**
- **Si passage à 70%** → pension provisoire : 30% × 1 457 € = **437 €**
- Le montant de référence (1 457 €) reste identique
- Seul le pourcentage versé change (20% → 30%)

### 8. **✨ NOUVEAU V.04.2.7 : Utiliser les validations intelligemment**

**Le simulateur vous aide à éviter les erreurs courantes :**

✅ **Faites confiance aux validations** : si le simulateur détecte une incohérence, prenez le temps de vérifier vos données

✅ **Lisez les messages d'erreur** : ils contiennent souvent la solution

✅ **Utilisez les warnings** : les avertissements (⚠️) ne bloquent pas le calcul mais signalent des cas inhabituels

✅ **Message informatif liquidables < assurance** : suivez la suggestion d'aller voir l'onglet Rachat

❌ **N'ignorez jamais les erreurs critiques** (❌) : elles empêchent le calcul pour une bonne raison

---

## 🧮 Comprendre les calculs

### Formule de base de la pension
Pension = Traitement indiciaire × 75% × (Trimestres liquidables / Trimestres requis)

### Méthode de calcul SRE (base 360 jours/an)

- **1 année = 360 jours**
- **1 mois = 30 jours**
- **1 trimestre = 90 jours**

**Exemple** :
- Période : 1 an, 3 mois, 15 jours
- Total jours SRE : (1 × 360) + (3 × 30) + 15 = **465 jours**
- Trimestres complets : 465 ÷ 90 = 5 trimestres + 15 jours
- **Arrondi final** : 15 jours < 45 → **5 trimestres**

### Rachat de trimestres (Fonction Publique) - CORRIGÉ V.04.2.5

**Formule officielle :**
Coût par trimestre = Traitement indiciaire × Coefficient d'âge
Coût total = Coût par trimestre × Nombre de trimestres

**Coefficients indicatifs (catégorie sédentaire, base 2024) :**

| Tranche d'âge | Option 1 (Taux seul) | Option 2 (Taux + Durée) |
|---------------|---------------------|------------------------|
| 20-29 ans | 25-28% du traitement | 45-50% du traitement |
| 30-39 ans | 28-35% du traitement | 50-62% du traitement |
| 40-49 ans | 35-48% du traitement | 62-85% du traitement |
| 50-54 ans | 48-65% du traitement | 85-115% du traitement |
| 55-59 ans | 65-85% du traitement | 115-150% du traitement |
| 60+ ans | 85-90% du traitement | 150-160% du traitement |

**Interpolation :**
Le simulateur calcule le coefficient exact pour votre âge par interpolation linéaire.

**Exemple détaillé :**
- Âge : 42 ans
- Traitement indiciaire : 2 353 € (indice 478 × 4,92278 €)
- Option 2 (Taux + Durée)

**Étape 1** : Interpolation du coefficient
- 40 ans → 62%
- 45 ans → 74%
- 42 ans → 62% + (2/5) × (74% - 62%) = 62% + 4,8% = **66,8%**

**Étape 2** : Calcul du coût
- Coût par trimestre : 2 353 × 0,668 = **1 572 €**
- Pour 4 trimestres : 1 572 × 4 = **6 288 €**

**Étape 3** : Déduction fiscale
- TMI 30% : 6 288 × 0,30 = 1 886 €
- **Coût réel** : 6 288 - 1 886 = **4 402 €**

**Comparaison avec V.04.2.4 (FAUX) :**
- V.04.2.4 : 15 200 € brut → 10 640 € net
- V.04.2.5 : 6 288 € brut → 4 402 € net
- **Économie : 6 238 €**

### Impact du temps partiel

**Assurance** : toujours comptée à 100%
- 1 an à 80% = 4 trimestres d'assurance (pas de prorata)

**Liquidables** : proratisés selon quotité (sauf si surcotisation)
- 1 an à 80% = 3,2 trimestres liquidables
- Avec surcotisation : 4 trimestres liquidables

### Pension provisoire (retraite progressive) - CORRIGÉ V.04.2.4

**Calcul initial (au départ progressif) :**
Pension de référence = Traitement × 75% × (Liquidables au départ / Trimestres requis)
Pension provisoire = Pension de référence × (1 - quotité)

**Si changement de quotité pendant la progressive :**
Nouvelle pension provisoire = Pension de référence × (1 - nouvelle quotité)

**Exemple :**
- Pension de référence : 1 457 €
- Quotité initiale 80% → pension provisoire : 1 457 × 20% = 291 €
- Changement à 70% → nouvelle pension provisoire : 1 457 × 30% = 437 €
- La pension de référence (1 457 €) ne change pas
- Seul le pourcentage versé évolue

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
2. **Surcote parentale** : 1,25% par trimestre liquidable l'année précédant l'âge légal (max 5%)
3. **Majoration excédentaire** : 1,25% par trimestre excédentaire restant

### Majoration familiale

- **3 enfants** → +10%
- **4 enfants** → +15%
- **5 enfants** → +20%
- etc.

**Condition** : enfants élevés pendant 9 ans avant leurs 16 ans

**Plafond** : 100% du traitement indiciaire (mais peut être dépassé avec surcote)

---

## 🎓 Cas d'usage typiques

### Cas 1 : "Je veux comprendre l'impact de ma quotité"

1. Remplissez l'onglet **Paramètres** avec vos vraies données
2. Lancez le calcul
3. Allez dans l'onglet **Graphique**
4. Comparez visuellement les revenus selon les quotités
5. Exportez les résultats en PDF pour les conserver

### Cas 2 : "Retraite progressive ou définitive directe ?"

1. **Simulation retraite progressive** :
   - Onglet Paramètres → définissez période progressive
   - Calculez → onglet Résultats RP
   - Exportez en PDF

2. **Simulation retraite définitive** :
   - Onglet Retraite Définitive
   - Récupérez les données
   - Date de départ = même date que la fin de la progressive
   - Quotité = 100%
   - Calculez et exportez en PDF

3. **Comparez les deux pensions finales** avec vos PDFs

### Cas 3 : "La surcotisation est-elle rentable pour moi ?"

1. Onglet Paramètres → cochez "Surcotisation"
2. Choisissez le taux de placement alternatif
3. Calculez
4. Dans les résultats, consultez **l'analyse de rentabilité**
5. Regardez la recommandation et la durée de rentabilisation
6. Exportez l'analyse en PDF pour la conserver

### Cas 4 : "Dois-je racheter des trimestres ?" - NOUVEAU V.04.2.5

**Contexte :** Avec la correction des barèmes, le rachat est devenu beaucoup plus accessible !

**Exemple concret :**
- Vous avez 42 ans
- Traitement : 2 353 €
- Il vous manque 4 trimestres pour le taux plein
- TMI : 30%

**Simulation V.04.2.4 (ANCIEN - FAUX) :**
1. Onglet Analyse Rachat
2. 4 trimestres, Option 2 (Taux + Durée)
3. **Résultat** : 10 640 € après impôt
4. Gain : +125 €/mois
5. Rentabilisation : 15 ans
6. **Conclusion** : "Trop cher, je préfère épargner"

**Simulation V.04.2.5+ (NOUVEAU - CORRECT) :**
1. Onglet Analyse Rachat
2. 4 trimestres, Option 2 (Taux + Durée)
3. **Résultat** : 4 402 € après impôt
4. Gain : +125 €/mois
5. Rentabilisation : 7,7 ans
6. **Conclusion** : "Rentable si je vis 8+ ans en retraite"
7. Exportez l'analyse en PDF

**Impact de la correction :**
- **Division du coût par 2,4**
- **Rentabilisation 2× plus rapide**
- **Décision complètement différente !**

### Cas 5 : "Comparer plusieurs scénarios"

1. Remplissez vos paramètres
2. Cliquez sur **Exporter** → sauvegardez `scenario_1.json`
3. Calculez et exportez le résultat en PDF
4. Modifiez les paramètres (ex: quotité différente)
5. **Exporter** → sauvegardez `scenario_2.json`
6. Calculez et exportez en PDF
7. Comparez vos PDFs côte à côte
8. Pour revenir à un scénario : **Importer** le fichier JSON correspondant

### Cas 6 : **✨ NOUVEAU V.04.2.7 : "J'ai fait une erreur de saisie"**

**Scénario :** Vous avez saisi 160 trimestres d'assurance mais seulement 12 ans de carrière

**Ce qui se passe :**
1. Vous cliquez sur "Calculer la simulation"
2. Le simulateur détecte l'incohérence
3. Il bascule automatiquement vers l'onglet "Résultats RP"
4. Un message s'affiche :
❌ Incohérence : 160 trimestres d'assurance pour environ 12 ans
de carrière possible (maximum théorique : ~48 trimestres)
5. Vous corrigez votre saisie dans l'onglet Paramètres
6. Vous re-calculez → tout fonctionne ! ✅

**Avantage :** Vous êtes guidé immédiatement, pas besoin de chercher l'erreur !

---

## 🛠 Dépannage

### "Vérifiez les dates"
- La date de relevé doit être < date départ progressif < date départ définitif
- Vérifiez le format des dates

### "Conditions non remplies"
- Retraite progressive nécessite :
  - Âge minimum : 60 ans
  - Assurance minimum : 150 trimestres
- Vérifiez votre date de naissance et vos trimestres d'assurance

### "Données incohérentes détectées"
- Les liquidables ne peuvent pas être supérieurs à l'assurance
- Revérifiez votre relevé de carrière officiel

### **✨ NOUVEAU V.04.2.7 : Messages d'erreur détaillés**

Le simulateur affiche maintenant des messages d'erreur **précis et pédagogiques** :

**Exemple 1 :**
❌ La date de départ progressif doit être APRÈS la date du relevé de carrière
→ **Solution** : Corrigez la date de départ

**Exemple 2 :**
⚠️ Indice majoré inhabituel (1200). Plage normale FP État : 350-900.
Vérifiez votre saisie.
→ **Solution** : Vérifiez que vous n'avez pas fait d'erreur de frappe

**Exemple 3 :**
❌ Case "Bonification enfants avant 2004" cochée mais aucun enfant saisi
→ **Solution** : Saisissez le nombre d'enfants OU décochez la case

### Le graphique ne s'affiche pas
- Vérifiez que vous avez bien cliqué sur "Calculer la simulation"
- Actualisez la page (F5)
- Essayez un autre navigateur (Chrome, Firefox, Edge)

### Les résultats semblent bizarres
1. Cliquez sur "Valeurs par défaut"
2. Testez avec l'exemple fourni
3. Si l'exemple fonctionne, revérifiez vos données personnelles
4. **✨ NOUVEAU V.04.2.7 :** Lisez attentivement les messages d'erreur, ils vous guident !

### Les coûts de rachat me semblent trop élevés - NOUVEAU

**Si vous utilisez une version antérieure à V.04.2.5 :**
- Les barèmes étaient ceux du secteur privé (2-3× trop cher)
- Téléchargez la version V.04.2.5 ou supérieure avec les coefficients corrects

**Si vous utilisez V.04.2.5+ :**
- Les coefficients sont indicatifs (base 2024, catégorie sédentaire)
- Pour un devis précis, contactez le SRE via [ensap.gouv.fr](https://ensap.gouv.fr)

### Le PDF ne se génère pas
- Vérifiez que vous avez calculé une simulation avant d'exporter
- Essayez un autre navigateur
- Vérifiez que les pop-ups ne sont pas bloquées
- Actualisez la page et recommencez

### Le PDF contient des caractères étranges - RÉSOLU V.04.2.6

**Ce problème a été résolu en V.04.2.6 :**
- jsPDF 2.5.1 supporte nativement tous les accents français
- Plus de conversion nécessaire
- Les PDFs sont maintenant parfaitement lisibles partout

**Si vous utilisez V.04.2.5.1 ou antérieure :**
- Téléchargez la version V.04.2.6 ou V.04.2.7 pour bénéficier du support natif des accents

---

## 📚 Pour aller plus loin

### Documentation officielle
- [Code des pensions (Légifrance)](https://www.legifrance.gouv.fr/codes/id/LEGITEXT000006070302/)
- [Service-Public.fr - Retraite progressive](https://www.service-public.fr/particuliers/vosdroits/F37400)
- [Service-Public.fr - Rachat de trimestres](https://www.service-public.fr/particuliers/vosdroits/F13243)
- [SRE - La retraite progressive](https://retraitesdeletat.gouv.fr/actif/lage-de-depart/la-retraite-progressive)
- [Décret 2007-262 - Rachat FP](https://www.legifrance.gouv.fr/loda/id/JORFTEXT000000465931/)
- [INSEE - Tables de mortalité](https://www.insee.fr/fr/statistiques/8327319)

### Mises à jour du simulateur
- Vérifiez régulièrement les nouvelles versions sur GitHub
- Changements réglementaires intégrés dès publication officielle
- Mise à jour annuelle de la valeur du point d'indice
- **V.04.2.7** : 31 validations de cohérence + UX améliorée ⭐

---

## ✅ Checklist avant de partir en retraite

- ☑ Simulation sur ce simulateur
- ☑ Simulation sur [ensap.gouv.fr](https://ensap.gouv.fr) (obligatoire)
- ☑ Vérification du relevé de carrière SRE
- ☑ Validation des bonifications enfants (si applicable)
- ☑ Décision sur la surcotisation (si temps partiel)
- ☑ Analyse du rachat de trimestres (si pertinent) avec V.04.2.5+
- ☑ Demande de devis officiel rachat au SRE (si intéressé)
- ☑ Constitution du dossier de demande (6 mois avant)
- ☑ Validation de l'indice majoré (règle des 6 mois)
- ☑ Anticipation des impacts fiscaux
- ☑ Préparation des justificatifs (enfants, études, etc.)
- ☑ Compréhension du mécanisme de la pension provisoire
- ☑ Anticipation d'éventuels changements de quotité pendant la progressive
- ☑ **Conservation des PDFs** de toutes vos simulations
- ☑ **✨ NOUVEAU V.04.2.7 :** Vérification de la cohérence de toutes vos données avec les validations

---

## 📜 Historique des versions

### V.04.2.7 (Octobre 2025) - ACTUELLE ⭐

**Améliorations majeures :**
- ✅ **31 validations de cohérence** implémentées (22 Paramètres + 9 Retraite Définitive)
- ✅ Messages d'erreur pédagogiques avec icônes (❌ ⚠️ ℹ️)
- ✅ Basculement automatique vers l'onglet Résultats en cas d'erreur
- ✅ Message informatif intelligent si liquidables < assurance
- ✅ UX améliorée : champs enfants grisés automatiquement
- ✅ Bug syntaxe enfants corrigé (`});}); ` → `});`)
- ✅ Validation quotité progressive supprimée (trop restrictive)
- ✅ Validation surcotisation + 100% ajoutée (basée sur textes officiels)

**Validations par catégorie :**
- 9 validations dates (naissance, relevé, départs, âges)
- 4 validations trimestres/jours (cohérence, valeurs négatives)
- 3 validations indices/valeurs (plages réalistes)
- 4 validations enfants + UX (cases cochées, totaux)
- 2 validations durée période progressive
- 9 validations Retraite Définitive (dates, âge, quotité, surcotisation)

### V.04.2.6 (Octobre 2025)

**Améliorations majeures :**
- ✅ Support natif des accents par jsPDF 2.5.1 (plus de conversion nécessaire)
- ✅ Avertissements renforcés partout (bannière rouge, PDF, footer)
- ✅ Phase de validation en cours documentée correctement
- ✅ Mentions légales complètes avec développement Claude (Anthropic)
- ✅ Protection juridique maximale (ensap.gouv.fr répété, disclaimers clairs)
- ✅ Correction toutes les dates : Octobre 2025
- ✅ Modèle 100% gratuit confirmé

**Différences techniques avec V.04.2.5.1 :**
- V.04.2.5.1 : Fonction `nettoyerPourPDF()` pour convertir les accents
- V.04.2.6 : Support natif jsPDF 2.5.1, plus besoin de conversion

### V.04.2.5 (Janvier 2025)

- 🔴 CORRECTION MAJEURE : Remplacement barèmes secteur privé → coefficients Fonction Publique d'État
- ✅ Calcul rachat basé sur traitement indiciaire × coefficient d'âge
- ✅ Interpolation linéaire des coefficients selon l'âge précis
- ✅ Division du coût par ~2,5 (exemple : 15 200 € → 5 836 €)
- ✅ Tableau des coefficients dans l'onglet Sources
- ✅ Avertissements renforcés sur le caractère indicatif

### V.04.2.4 (Janvier 2025)

- ✅ CORRECTION MAJEURE : Documentation pension provisoire (évolution quotité)
- ✅ Ajout encadré informatif dans Paramètres
- ✅ Mise à jour onglet Sources
- ❌ Erreur corrigée en V.04.2.5 : Barèmes rachat incorrects

### V.04.2.3 (Janvier 2025)

- ✨ Nouvel onglet "Retraite Définitive"
- ✨ Option Décret 1982 (6/7ème et 32/35ème)
- 📊 Graphiques optimisés (aspectRatio: 3, max-width: 800px)

### Versions antérieures

- V.04.2.x (2024) : Amélioration interface utilisateur
- V.04.1.x (2024) : Ajout onglet "Analyse Rachat" (barèmes erronés)
- V.04.0.x (2023) : Intégration Décret 2023-799 (surcote parentale)

---

## ❓ FAQ - Foire Aux Questions

### Q1 : Pourquoi mon résultat diffère-t-il du simulateur ENSAP ?
**R :** Un écart de 1 à 2 trimestres liquidables (~1-2% de pension) peut exister en raison de règles d'arrondi internes au SRE non documentées publiquement. Ce simulateur applique la méthode officielle documentée. Pour une estimation définitive, consultez toujours ensap.gouv.fr.

### Q2 : Puis-je changer de quotité pendant ma retraite progressive ?
**R :** Oui ! Et c'est une **correction importante** apportée dans la V.04.2.4. Si vous changez de quotité, votre pension provisoire s'ajustera automatiquement (exemple : passer de 80% à 70% augmente la pension de 20% à 30% du montant de référence). Par contre, le montant de référence lui-même ne change pas pendant la progressive.

### Q3 : Le décret 1982 s'applique-t-il à moi ?
**R :** Consultez votre fiche de paie actuelle si vous êtes déjà à temps partiel 80% ou 90%. Si vous travaillez 4j/5 (80%) et êtes payé plus que 80% de votre traitement plein temps, le décret s'applique. En cas de doute, laissez la case cochée (cas majoritaire).

### Q4 : La surcotisation est-elle toujours rentable ?
**R :** Non, cela dépend de plusieurs facteurs : votre espérance de vie, les taux de placement alternatifs disponibles, et votre besoin de liquidité. Le simulateur vous fournit une analyse actuarielle détaillée pour vous aider à décider.

### Q5 : Quelle différence entre "trimestres d'assurance" et "trimestres liquidables" ?
**R :** 
- **Trimestres d'assurance** : comptent pour éviter la décote (durée de cotisation)
- **Trimestres liquidables** : déterminent le montant de la pension (prorata)
- À temps partiel sans surcotisation : assurance = 100%, liquidables = proratisés

### Q6 : Comment fonctionne la surcote parentale ?
**R :** Pour les générations ≥ 1964, si vous avez au moins 1 enfant et que vous travaillez l'année précédant votre âge légal, vous gagnez 1,25% de surcote par trimestre liquidable cotisé (max 4 trimestres = 5%). Attention : la quotité impacte le nombre de trimestres retenus.

### Q7 : Puis-je exporter mes simulations ?
**R :** Oui ! Deux types d'exports :
- **Format JSON** (bouton "Exporter") : pour sauvegarder et réimporter vos paramètres
- **Format PDF** (bouton dans chaque onglet de résultats) : pour conserver, imprimer ou partager vos résultats avec **accents parfaitement préservés** (V.04.2.6+)

### Q8 : Les bonifications enfants sont-elles automatiques ?
**R :** 
- **Enfants après 2004** : oui, attribution automatique (2 trimestres d'assurance)
- **Enfants avant 2004** : non, vous devez remplir les conditions strictes et fournir des justificatifs lors de votre demande de retraite

### Q9 : Que signifie la "règle des six mois" ?
**R :** Une augmentation d'indice majoré doit avoir au moins 6 mois d'ancienneté avant votre départ en retraite pour être prise en compte dans le calcul de votre pension.

### Q10 : Le simulateur fonctionne-t-il hors ligne ?
**R :** Oui ! Une fois le fichier HTML téléchargé, vous pouvez l'utiliser sans connexion internet. Toutes les données restent sur votre ordinateur.

### Q11 : Mes données sont-elles sécurisées ?
**R :** Absolument. Le simulateur fonctionne entièrement en local dans votre navigateur. Aucune donnée n'est envoyée sur internet ou stockée ailleurs que sur votre ordinateur. Même les PDFs sont générés localement.

### Q12 : Que se passe-t-il si je cumule plusieurs types de surcote ?
**R :** Les 3 types de surcote SRE sont **cumulables** :
- Surcote parentale (max 5%)
- Surcote classique (trimestres au-delà de l'âge légal)
- Majoration excédentaire (trimestres restants)

Le simulateur calcule automatiquement le cumul selon la méthode SRE.

### Q13 : Pourquoi les coûts de rachat sont-ils différents de la V.04.2.4 ? - NOUVEAU
**R :** La V.04.2.5 corrige une **erreur majeure** : les versions précédentes utilisaient les barèmes du secteur privé, donnant des coûts 2 à 3 fois trop élevés. La V.04.2.5+ utilise les coefficients corrects de la Fonction Publique d'État, basés sur votre traitement indiciaire.

**Exemple :**
- V.04.2.4 : 4 trim. à 40 ans = 15 200 € (FAUX)
- V.04.2.5+ : 4 trim. à 40 ans = 5 836 € (CORRECT)

### Q14 : Comment obtenir un devis officiel pour le rachat ?
**R :** Connectez-vous sur [ensap.gouv.fr](https://ensap.gouv.fr) et suivez la procédure de demande de devis. Le SRE vous fournira un devis personnalisé et opposable, tenant compte de tous vos paramètres spécifiques.

### Q15 : Le rachat de trimestres est-il déductible des impôts ?
**R :** Oui ! Les sommes versées pour le rachat de trimestres sont déductibles de votre revenu imposable, selon votre tranche marginale d'imposition (TMI). Cela réduit significativement le coût réel du rachat.

**Exemple :**
- Coût brut : 6 000 €
- TMI 30% : économie de 1 800 €
- **Coût réel : 4 200 €**

### Q16 : Les accents sont-ils bien gérés dans les PDFs ? - NOUVEAU V.04.2.6
**R :** Oui ! La V.04.2.6+ utilise **jsPDF 2.5.1** qui supporte nativement tous les accents français (é, è, à, ç, ù, etc.). Plus besoin de conversion, les PDFs sont parfaitement lisibles partout, sur tous les systèmes (Windows, Mac, Linux, mobile).

**Différence avec les versions précédentes :**
- V.04.2.5.1 et antérieures : Conversion des accents nécessaire
- V.04.2.6+ : Support natif, aucune conversion

### Q17 : **✨ NOUVEAU V.04.2.7 : Que signifient les icônes dans les messages d'erreur ?**
**R :** Le simulateur utilise 3 types d'icônes pour vous guider :
- ❌ **Erreur critique** : bloque le calcul, vous devez corriger
- ⚠️ **Avertissement** : calcul possible mais cas inhabituel, vérifiez vos données
- ℹ️ **Information** : conseil ou suggestion pour améliorer votre simulation

### Q18 : **✨ NOUVEAU V.04.2.7 : Pourquoi les champs enfants sont-ils grisés ?**
**R :** C'est une amélioration UX de la V.04.2.7 ! Les champs sont automatiquement désactivés (grisés) si les cases "Bonification enfants" ou "Majoration enfants" ne sont pas cochées. Cela évite toute confusion et garantit la cohérence de vos données.

**Pour activer les champs :**
1. Cochez la case correspondante
2. Les champs se dégrisent automatiquement
3. Saisissez le nombre d'enfants

### Q19 : **✨ NOUVEAU V.04.2.7 : J'ai un message "Incohérence trimestres vs années de carrière", que faire ?**
**R :** Ce message apparaît quand le nombre de trimestres saisi semble incompatible avec votre durée de carrière.

**Exemple :**
- Vous avez 35 ans aujourd'hui et êtes né en 1990
- Vous avez commencé à travailler à 22 ans (en 2012)
- Durée maximale de carrière : 13 ans = ~52 trimestres maximum
- Si vous saisissez 160 trimestres : ❌ incohérence détectée !

**Solution :** Vérifiez votre relevé de carrière officiel et corrigez la saisie.

### Q20 : **✨ NOUVEAU V.04.2.7 : Le message dit que je peux consulter l'onglet "Analyse Rachat", pourquoi ?**
**R :** Si vos trimestres liquidables sont inférieurs à vos trimestres d'assurance (écart de plusieurs trimestres), cela indique généralement des périodes de temps partiel dans votre passé.

**Le simulateur vous suggère intelligemment :**
- D'aller voir l'onglet "Analyse Rachat"
- Pour évaluer s'il est rentable de **racheter** ces trimestres manquants
- Cela augmentera votre pension définitive

**Note importante :** Rachat ≠ Surcotisation
- **Surcotisation** : pour le temps partiel FUTUR (pendant la progressive)
- **Rachat** : pour rattraper le temps partiel PASSÉ

---

## 🎯 Conseils d'utilisation avancés

### Optimiser votre stratégie de retraite progressive

1. **Testez plusieurs quotités** : utilisez le graphique pour visualiser l'impact
2. **Évaluez la surcotisation** : selon votre situation fiscale et patrimoniale
3. **Anticipez les changements** : vous pouvez modifier votre quotité en cours de route
4. **Planifiez avec la majoration familiale** : 3 enfants = +10% de pension
5. **Considérez la surcote parentale** : travaillez l'année avant votre âge légal
6. **Analysez le rachat** : avec V.04.2.5+, les coûts corrects le rendent plus attractif
7. **Exportez régulièrement** : conservez vos simulations en PDF pour comparaison
8. **✨ NOUVEAU V.04.2.7 : Faites confiance aux validations** : elles vous évitent des erreurs coûteuses

### Stratégies selon votre profil

**Si vous avez une longue carrière :**
- Privilégiez un départ plus tôt avec quotité basse
- La surcotisation est moins intéressante (taux plein déjà atteint)
- Le rachat est probablement inutile
- Exportez plusieurs scénarios de quotité en PDF

**Si vous avez une carrière incomplète :**
- Envisagez le rachat de trimestres pour éviter la décote
- La surcotisation peut être très rentable
- Utilisez V.04.2.5+ pour calculer le vrai coût du rachat
- Exportez l'analyse rachat en PDF avant de décider
- **✨ NOUVEAU V.04.2.7 :** Si le message informatif s'affiche, suivez la suggestion !

**Si vous avez des enfants :**
- Vérifiez vos droits aux bonifications
- Optimisez la surcote parentale en travaillant l'année avant l'âge légal
- Simulez avec et sans bonifications pour voir l'impact
- **✨ NOUVEAU V.04.2.7 :** Les champs sont automatiquement grisés, plus d'erreurs !

**Si vous approchez de l'âge légal :**
- Calculez l'intérêt de poursuivre pour bénéficier de la surcote classique
- Comparez avec un départ immédiat
- Exportez les deux scénarios en PDF

**Si vous envisagez le rachat :** - NOUVEAU
- Utilisez **impérativement V.04.2.5+** (barèmes corrects)
- Simulez différentes options (taux seul vs taux+durée)
- Comparez avec l'épargne selon votre TMI
- Exportez l'analyse en PDF
- Demandez un devis officiel au SRE
- Considérez l'avantage fiscal (déductibilité)

**✨ NOUVEAU V.04.2.7 : Si vous avez des doutes sur vos données :**
- Cliquez sur "Calculer" même avec des données approximatives
- Lisez attentivement les messages d'erreur
- Corrigez une par une les incohérences détectées
- Les validations vous guident vers des données cohérentes

---

## 🔗 Liens utiles

### Sites officiels
- [ensap.gouv.fr](https://ensap.gouv.fr) - Simulation officielle + devis rachat
- [retraitesdeletat.gouv.fr](https://retraitesdeletat.gouv.fr) - SRE
- [service-public.fr](https://www.service-public.fr/particuliers/vosdroits/F37400) - Retraite progressive
- [service-public.fr](https://www.service-public.fr/particuliers/vosdroits/F13243) - Rachat de trimestres
- [info-retraite.fr](https://www.info-retraite.fr) - Portail commun

### Documentation technique
- [Légifrance - Code des pensions](https://www.legifrance.gouv.fr/codes/id/LEGITEXT000006070302/)
- [Décret 2023-799](https://www.legifrance.gouv.fr/jorf/id/JORFTEXT000047970226)
- [Décret 2007-262 - Rachat FP](https://www.legifrance.gouv.fr/loda/id/JORFTEXT000000465931/)
- [INSEE - Tables de mortalité](https://www.insee.fr/fr/statistiques/8327319)

### Ressources complémentaires
- [info-retraite.fr](https://www.info-retraite.fr) - Portail commun des régimes de retraite
- [INSEE](https://www.insee.fr/fr/statistiques/8327319) - Tables de mortalité

---

## 🙏 Remerciements

Ce simulateur gratuit a été développé pour aider les fonctionnaires d'État à mieux comprendre les mécanismes complexes de la retraite progressive et du rachat de trimestres. Il s'appuie sur :
- Les textes réglementaires officiels
- Les guides du Service des Retraites de l'État
- Les retours d'expérience des utilisateurs
- Les corrections apportées suite aux vérifications des sources officielles
- La collaboration technique avec **Claude (Anthropic)**

**Un merci particulier** :
- Aux utilisateurs qui ont signalé les inexactitudes concernant l'évolution de la pension provisoire (V.04.2.4)
- À l'utilisateur qui a remarqué que les coûts de rachat étaient "très chers", permettant la découverte et la correction de l'erreur majeure sur les barèmes (V.04.2.5)
- Aux beta-testeurs qui ont identifié les incohérences de saisie et permis l'ajout des validations (V.04.2.7) ⭐
- À **Claude (Anthropic)** pour l'assistance technique, algorithmique, réglementaire, légale et documentaire dans le développement de ce simulateur

**Ces retours ont permis des améliorations majeures qui changent significativement les résultats et les décisions !**

---

## 📄 Licence et utilisation

Ce simulateur gratuit est fourni à titre **informatif et pédagogique**. Il ne remplace pas une consultation officielle auprès du SRE ou d'ENSAP.

**Utilisation libre** pour un usage personnel. La redistribution ou l'utilisation commerciale nécessite une autorisation.

**Clause de non-responsabilité** : Les résultats fournis sont des estimations. Seuls les calculs officiels du SRE font foi.

**⚠️ CE SIMULATEUR NE REMPLACE EN AUCUN CAS LES OUTILS OFFICIELS DE L'ÉTAT**

**Pour une estimation officielle définitive, consultez toujours [ensap.gouv.fr](https://ensap.gouv.fr)**

---

**Version du mode d'emploi :** V.04.2.7 - Octobre 2025

**Dernière mise à jour :** 31 validations de cohérence + UX améliorée

**Prochaine mise à jour prévue :** Mise à jour de la valeur du point d'indice (juillet 2026)

---

**Développé par Jean-Michel DI PACO avec l'assistance de Claude (Anthropic)**

**Contact :** maviclearn@gmail.com