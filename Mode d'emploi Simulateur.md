markdown# 📖 Mode d'emploi du Simulateur de Retraite Progressive V.04.2.3

## 🎯 Introduction

Ce simulateur vous permet d'estimer votre pension de retraite progressive et définitive en tant que fonctionnaire d'État. Il applique la méthode officielle du Service des Retraites de l'État (SRE) avec une transparence totale sur les calculs.

---
## Avant toute installation il vous faut telecharger sur le site Info Retraite votre "Relevé de Carriere"

## 🚀 Démarrage rapide

### Installation
1. **Téléchargez** le fichier `simulateur_retraite_Version_V.04.2.3.html`
2. **Double-cliquez** dessus pour l'ouvrir dans votre navigateur
3. Aucune installation, aucune connexion internet requise !

### Premier calcul en 3 étapes
1. **Onglet "Paramètres"** → Remplissez vos données
2. Cliquez sur **"Calculer la simulation"**
3. **Onglet "Résultats RP"** → Consultez vos résultats

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
- 💡 *Les trimestres d'assurance comptent pour la durée de cotisation (évitent la décote)*

**Trimestres liquidables au relevé**
- Nombre de trimestres de services effectifs selon votre relevé SRE
- Exemple : 142 trimestres + 86 jours
- 💡 *Les trimestres liquidables déterminent le montant de la pension (prorata)*

#### Section "Informations personnelles"

**Date de naissance**
- Obligatoire pour calculer l'âge légal et les trimestres requis
- Détermine automatiquement votre génération (1964 → 171 trimestres requis)

**Sexe**
- Utilisé uniquement pour l'analyse actuarielle de rentabilité
- Basé sur les tables de mortalité INSEE 2024

**Trimestres requis**
- Calculé automatiquement selon votre année de naissance
- 1964 et après → 172 trimestres
- 1963 → 171 trimestres, etc.

**Indice majoré (IM)**
- Votre indice majoré actuel
- Exemple : 478
- 💡 *Attention à la règle des six mois : une augmentation d'indice doit avoir au moins 6 mois d'ancienneté avant le départ*

**Valeur du point**
- Valeur officielle : **4,92278 €** (depuis le 1er juillet 2023)
- Mise à jour annuelle en général

#### Section "Planning de retraite progressive"

**Date de départ retraite progressive**
- Date de début de votre retraite progressive
- ⚠️ Conditions : minimum 60 ans + 150 trimestres d'assurance

**Date de départ retraite définitive**
- Date de fin de la période progressive
- Entre cette date et le départ progressif, vous cumulez traitement partiel + pension provisoire

**Quotité entre relevé et départ progressif**
- Votre quotité de travail ACTUELLE (avant la retraite progressive)
- 100% = temps plein
- 80% = 4 jours/semaine
- 💡 *Cette quotité impacte l'accumulation de trimestres liquidables*

**Quotité pendant la retraite progressive**
- Votre quotité pendant la période progressive
- Choix : 50%, 60%, 70%, 80%, 90%
- ⚠️ Attention : cette quotité impacte la surcote parentale

**☑️ Appliquer le Décret n°82-624**
- **Coché par défaut** (cas majoritaire)
- Concerne certains fonctionnaires à temps partiel :
  - **80%** → rémunération à **6/7ème** (≈85,71%)
  - **90%** → rémunération à **32/35ème** (≈91,43%)

**Comment vérifier si cela vous concerne ?**
1. Consultez votre fiche de paie actuelle si vous êtes déjà à temps partiel 80% ou 90%
2. Regardez la ligne "Traitement Brut"
3. Si vous travaillez 4j/5 (80%) et êtes payé plus de 80%, le décret s'applique
4. Si incertain, laissez coché (cas par défaut)

#### Section "Options de surcotisation"

**☑️ Surcotisation pendant la progressive**
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

#### 🎯 Pension définitive estimée
- **Montant principal** en gros caractères verts
- **Avec majoration familiale** si applicable

#### Détails décote/surcote
- **Si décote** : trimestres manquants, taux appliqué, date du taux plein
- **Si surcote** : détail des 3 types de majorations SRE
  - Surcote parentale (max 5%)
  - Surcote classique (après âge légal)
  - Majoration excédentaire (trimestres restants)

---

### 3️⃣ Onglet RETRAITE DÉFINITIVE ⭐ NOUVEAU

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
   - ☑️ **Décret n°82-624** : même principe que l'onglet Paramètres
   - ☑️ **Surcotisation** : si temps partiel, option de surcotiser pour compter les liquidables à 100%

4. **Cliquez sur "Calculer la simulation"**

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

### 5️⃣ Onglet ANALYSE RACHAT

Cet onglet analyse la **rentabilité du rachat de trimestres**.

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

⚠️ **Important** : Les barèmes affichés sont indicatifs (basés sur 2024). Demandez toujours un devis officiel au SRE.

---

### 6️⃣ Onglet SOURCES

Références réglementaires complètes :
- Code des pensions civiles et militaires
- Décrets applicables
- Liens vers sites officiels
- Méthode de calcul SRE détaillée
- Avertissement sur la précision du simulateur

---

## 🔧 Fonctionnalités avancées

### Import/Export de simulations

**Exporter vos paramètres**
1. Remplissez l'onglet Paramètres
2. Cliquez sur **"Exporter"**
3. Un fichier JSON est téléchargé : `parametres_simulateur_retraite_v04_2_3.json`
4. Conservez ce fichier pour le réutiliser plus tard

**Importer des paramètres**
1. Cliquez sur **"Importer"**
2. Sélectionnez un fichier JSON précédemment exporté
3. Tous les champs sont automatiquement remplis

💡 *Utile pour comparer plusieurs scénarios ou partager avec un conseiller*

### Bouton "Valeurs par défaut"
- Réinitialise tous les champs avec l'exemple par défaut
- Utile pour tester le simulateur ou repartir de zéro

---

## ⚠️ Points d'attention importants

### 1. Non-opposabilité des résultats

| Ce simulateur | Simulateur officiel SRE |
|:--------------|:------------------------|
| Aide à la décision | **Référence légale** |
| Transparence totale | Calcul exact mais opaque |
| Écart possible 1-2% | **Seul résultat opposable** |

**➡️ Pour une estimation officielle définitive, consultez toujours [ensap.gouv.fr](https://ensap.gouv.fr)**

### 2. Écart connu avec le SRE

- Écart estimé : **1 à 2 trimestres liquidables** (~1-2% de pension)
- Cause probable : règles d'arrondi internes non documentées publiquement
- Ce simulateur applique rigoureusement la méthode SRE documentée

### 3. Règle des six mois

Une augmentation d'indice majoré doit avoir au moins **6 mois d'ancienneté** avant le départ en retraite pour être prise en compte.

**Exemple** :
- Départ prévu : 1er décembre 2025
- Nouvelle augmentation d'indice : 1er novembre 2025
- ❌ Cette augmentation ne compte PAS (seulement 1 mois)

### 4. Décret n°82-624

Ce décret s'applique à **certains** fonctionnaires en temps partiel de droit commun :
- Pas applicable aux temps partiels thérapeutiques
- Pas applicable à tous les statuts
- Vérifiez sur votre fiche de paie actuelle

**En cas de doute** : laissez la case cochée (cas majoritaire)

### 5. Surcotisation

La surcotisation est **rentable** si :
- Vous partez longtemps en retraite (espérance de vie élevée)
- Le taux de placement alternatif est faible
- Vous valorisez la sécurité viagère

Elle est **moins intéressante** si :
- Vous avez une épargne bien rémunérée
- Vous souhaitez conserver la liquidité des fonds
- Vous voulez transmettre un capital

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

### Impact du temps partiel

**Assurance** : toujours comptée à 100%
- 1 an à 80% = 4 trimestres d'assurance (pas de prorata)

**Liquidables** : proratisés selon quotité (sauf si surcotisation)
- 1 an à 80% = 3,2 trimestres liquidables
- Avec surcotisation : 4 trimestres liquidables

### Décote

Si **assurance < trimestres requis** :
- Génération ≥ 1964 : **1,09%** par trimestre manquant
- Génération < 1964 : **1,25%** par trimestre manquant
- **Maximum** : -25% (soit 20-23 trimestres manquants)
- **Annulation automatique à 67 ans**

**Exemple** :
- Génération 1964, trimestres requis : 172
- Assurance finale : 165 trimestres
- Manquants : 172 - 165 = 7 trimestres
- Décote : 7 × 1,09% = **-7,63%**

### Surcotes (3 types cumulables)

#### 1. Surcote classique
- **Condition** : Assurance ≥ trimestres requis + âge ≥ âge légal
- **Taux** : 1,25% par trimestre au-delà de l'âge légal
- **Plafond** : 67 ans

#### 2. Surcote parentale (Décret 2023-799)
- **Condition** : 
  - Génération ≥ 1964
  - Au moins 1 enfant (bonification ou majoration)
  - L'année précédant l'âge légal
- **Taux** : 1,25% par trimestre liquidable coté cette année-là
- **Maximum** : 5% (4 trimestres max)
- **Impact quotité** : quotité 80% = 3,2 trimestres → 3 retenus

#### 3. Majoration excédentaire
- **Condition** : Trimestres d'assurance excédentaires restants
- **Taux** : 1,25% par trimestre
- **Calcul** : Excédentaires - surcote parentale - surcote classique

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

### Cas 2 : "Retraite progressive ou définitive directe ?"

1. **Simulation retraite progressive** :
   - Onglet Paramètres → définissez période progressive
   - Calculez → onglet Résultats RP

2. **Simulation retraite définitive** :
   - Onglet Retraite Définitive
   - Récupérez les données
   - Date de départ = même date que la fin de la progressive
   - Quotité = 100%
   - Calculez

3. **Comparez les deux pensions finales**

### Cas 3 : "La surcotisation est-elle rentable pour moi ?"

1. Onglet Paramètres → cochez "Surcotisation"
2. Choisissez le taux de placement alternatif
3. Calculez
4. Dans les résultats, consultez **l'analyse de rentabilité**
5. Regardez la recommandation et la durée de rentabilisation

### Cas 4 : "Dois-je racheter des trimestres ?"

1. Onglet **Analyse Rachat**
2. Récupérez vos données
3. Simulez le nombre de trimestres à racheter
4. Choisissez l'option (taux seul ou taux+durée)
5. Comparez avec un placement alternatif
6. Décidez selon la recommandation

### Cas 5 : "Comparer plusieurs scénarios"

1. Remplissez vos paramètres
2. Cliquez sur **Exporter** → sauvegardez `scenario_1.json`
3. Modifiez les paramètres (ex: quotité différente)
4. **Exporter** → sauvegardez `scenario_2.json`
5. Pour revenir à un scénario : **Importer** le fichier correspondant

---

## 🐛 Dépannage

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

### Le graphique ne s'affiche pas
- Vérifiez que vous avez bien cliqué sur "Calculer la simulation"
- Actualisez la page (F5)
- Essayez un autre navigateur (Chrome, Firefox, Edge)

### Les résultats semblent bizarres
1. Cliquez sur "Valeurs par défaut"
2. Testez avec l'exemple fourni
3. Si l'exemple fonctionne, revérifiez vos données personnelles

---

## 📞 Besoin d'aide ?

### Pour des questions techniques sur le simulateur
- Ouvrez une **Issue** sur GitHub
- Décrivez précisément votre problème
- Joignez une capture d'écran si possible

### Pour des questions sur votre retraite
- ⚠️ Ce simulateur n'est pas un service de conseil officiel
- Consultez :
  - [ensap.gouv.fr](https://ensap.gouv.fr) - Simulateur officiel
  - [retraitesdeletat.gouv.fr](https://retraitesdeletat.gouv.fr) - Service des Retraites de l'État
  - Votre service RH
  - Un conseiller retraite

---

## 📚 Pour aller plus loin

### Documentation officielle
- [Code des pensions (Légifrance)](https://www.legifrance.gouv.fr/codes/id/LEGITEXT000006070302/)
- [Service-Public.fr - Retraite progressive](https://www.service-public.fr/particuliers/vosdroits/F37400)
- [INSEE - Tables de mortalité](https://www.insee.fr/fr/statistiques/8327319)

### Mises à jour du simulateur
- Vérifiez régulièrement les nouvelles versions sur GitHub
- Changements réglementaires intégrés dès publication officielle
- Mise à jour annuelle de la valeur du point d'indice

---

## ✅ Checklist avant de partir en retraite

- [ ] Simulation sur ce simulateur ✓
- [ ] Simulation sur [ensap.gouv.fr](https://ensap.gouv.fr) (obligatoire)
- [ ] Vérification du relevé de carrière SRE
- [ ] Validation des bonifications enfants (si applicable)
- [ ] Décision sur la surcotisation (si temps partiel)
- [ ] Analyse du rachat de trimestres (si pertinent)
- [ ] Constitution du dossier de demande (6 mois avant)
- [ ] Validation de l'indice majoré (règle des 6 mois)
- [ ] Anticipation des impacts fiscaux
- [ ] Préparation des justificatifs (enfants, études, etc.)

---

**Version du mode d'emploi :** V.04.2.3 - Octobre 2025

**Dernière mise à jour :** Conforme au Décret n°2023-799 du 21 août 2023