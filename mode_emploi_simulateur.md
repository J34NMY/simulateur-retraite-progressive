# 📖 Mode d'emploi du Simulateur de Retraite Progressive V.04.2.4

## 🎯 Introduction

Ce simulateur vous permet d'estimer votre pension de retraite progressive et définitive en tant que fonctionnaire d'État. Il applique la méthode officielle du Service des Retraites de l'État (SRE) avec une transparence totale sur les calculs.

---

## 🚀 Démarrage rapide


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
- 1965 et après → 172 trimestres
- 1964 → 171 trimestres, etc.

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
- Concerne certains fonctionnaires en temps partiel de droit commun :
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

#### Section "Information pension provisoire" ⭐ NOUVEAU

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

### 3️⃣ Onglet RETRAITE DÉFINITIVE ⭐

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
- **Section mise à jour** sur la pension provisoire avec l'explication correcte
- Avertissement sur la précision du simulateur

---

## 🔧 Fonctionnalités avancées

### Import/Export de simulations

**Exporter vos paramètres**
1. Remplissez l'onglet Paramètres
2. Cliquez sur **"Exporter"**
3. Un fichier JSON est téléchargé : `parametres_simulateur_retraite_v04_2_4.json`
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

### 6. Pension provisoire pendant la retraite progressive ⭐ NOUVEAU

**Important à comprendre :**

**✅ CE QUI EST VRAI :**
- La pension provisoire est calculée à la date du départ progressif
- Elle est basée sur les droits acquis AVANT le départ progressif
- **SI vous changez de quotité**, la part versée s'ajuste automatiquement
  - Exemple : passage de 80% → 70% de travail
  - Pension provisoire passe de 20% → 30%
- Les trimestres acquis pendant la progressive sont comptabilisés pour la retraite définitive

**❌ CE QUI EST FAUX :**
- La pension provisoire ne se recalcule PAS en fonction des nouveaux trimestres acquis pendant la progressive
- Le montant de référence de la pension reste celui calculé au départ progressif
- Seul le **pourcentage** de cette pension peut varier si la quotité change

**Exemple concret :**
- Départ progressif : 142 trimestres liquidables
- Pension de référence calculée : 1 457 €
- Quotité 80% → pension provisoire : 20% × 1 457 € = **291 €**
- **Si passage à 70%** → pension provisoire : 30% × 1 457 € = **437 €**
- ✅ Le montant de référence (1 457 €) reste identique
- ✅ Seul le pourcentage versé change (20% → 30%)

---

## 🧮 Comprendre les calculs

### Formule de base de la pensiontemps partiel)
- [ ] Analyse du rachat de trimestres (si pertinent)
- [ ] Constitution du dossier de demande (6 mois avant)
- [ ] Validation de l'indice majoré (règle des 6 mois)
- [ ] Anticipation des impacts fiscaux
- [ ] Préparation des justificatifs (enfants, études, etc.)
- [ ] Compréhension du mécanisme de la pension provisoire
- [ ] Anticipation d'éventuels changements de quotité pendant la progressive

---

## 📝 Historique des versions

### V.04.2.4 - Janvier 2025
- ✅ **Correction majeure** : Documentation sur l'évolution de la pension provisoire
- ✅ Ajout d'un encadré informatif dans l'onglet Paramètres
- ✅ Mise à jour de l'onglet Sources avec les explications correctes
- ✅ Ajout de notes dans les résultats de la retraite progressive

### V.04.2.3 - Janvier 2025
- Ajout de l'onglet Retraite Définitive
- Option Décret 1982 (6/7ème et 32/35ème)
- Optimisation des graphiques (aspectRatio: 3, max-width: 800px)

### Versions antérieures
- V.04.2.x : Amélioration de l'interface utilisateur
- V.04.1.x : Ajout de l'analyse de rachat
- V.04.0.x : Intégration de la surcote parentale (Décret 2023-799)

---

## ❓ FAQ - Foire Aux Questions

### Q1 : Pourquoi mon résultat diffère-t-il du simulateur ENSAP ?
**R :** Un écart de 1 à 2 trimestres liquidables (~1-2% de pension) peut exister en raison de règles d'arrondi internes au SRE non documentées publiquement. Ce simulateur applique la méthode officielle documentée. Pour une estimation définitive, consultez toujours ensap.gouv.fr.

### Q2 : Puis-je changer de quotité pendant ma retraite progressive ?
**R :** Oui ! Et c'est une **correction importante** apportée dans cette version V.04.2.4. Si vous changez de quotité, votre pension provisoire s'ajustera automatiquement (exemple : passer de 80% à 70% augmente la pension de 20% à 30% du montant de référence). Par contre, le montant de référence lui-même ne change pas pendant la progressive.

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
**R :** Oui ! Utilisez le bouton "Exporter" pour sauvegarder vos paramètres au format JSON. Vous pouvez ensuite les réimporter avec le bouton "Importer" pour comparer différents scénarios.

### Q8 : Les bonifications enfants sont-elles automatiques ?
**R :** 
- **Enfants après 2004** : oui, attribution automatique (2 trimestres d'assurance)
- **Enfants avant 2004** : non, vous devez remplir les conditions strictes et fournir des justificatifs lors de votre demande de retraite

### Q9 : Que signifie la "règle des six mois" ?
**R :** Une augmentation d'indice majoré doit avoir au moins 6 mois d'ancienneté avant votre départ en retraite pour être prise en compte dans le calcul de votre pension.

### Q10 : Le simulateur fonctionne-t-il hors ligne ?
**R :** Oui ! Une fois le fichier HTML téléchargé, vous pouvez l'utiliser sans connexion internet. Toutes les données restent sur votre ordinateur.

### Q11 : Mes données sont-elles sécurisées ?
**R :** Absolument. Le simulateur fonctionne entièrement en local dans votre navigateur. Aucune donnée n'est envoyée sur internet ou stockée ailleurs que sur votre ordinateur.

### Q12 : Que se passe-t-il si je cumule plusieurs types de surcote ?
**R :** Les 3 types de surcote SRE sont **cumulables** :
- Surcote parentale (max 5%)
- Surcote classique (trimestres au-delà de l'âge légal)
- Majoration excédentaire (trimestres restants)

Le simulateur calcule automatiquement le cumul selon la méthode SRE.

---

## 🎯 Conseils d'utilisation avancés

### Optimiser votre stratégie de retraite progressive

1. **Testez plusieurs quotités** : utilisez le graphique pour visualiser l'impact
2. **Évaluez la surcotisation** : selon votre situation fiscale et patrimoniale
3. **Anticipez les changements** : vous pouvez modifier votre quotité en cours de route
4. **Planifiez avec la majoration familiale** : 3 enfants = +10% de pension
5. **Considérez la surcote parentale** : travaillez l'année avant votre âge légal

### Stratégies selon votre profil

**Si vous avez une longue carrière :**
- Privilégiez un départ plus tôt avec quotité basse
- La surcotisation est moins intéressante (taux plein déjà atteint)

**Si vous avez une carrière incomplète :**
- Envisagez le rachat de trimestres pour éviter la décote
- La surcotisation peut être très rentable

**Si vous avez des enfants :**
- Vérifiez vos droits aux bonifications
- Optimisez la surcote parentale en travaillant l'année avant l'âge légal

**Si vous approchez de l'âge légal :**
- Calculez l'intérêt de poursuivre pour bénéficier de la surcote classique
- Comparez avec un départ immédiat

---

## 🔗 Liens utiles

### Sites officiels
- [ensap.gouv.fr](https://ensap.gouv.fr) - Espace numérique sécurisé de l'agent public
- [retraitesdeletat.gouv.fr](https://retraitesdeletat.gouv.fr) - Service des Retraites de l'État
- [service-public.fr](https://www.service-public.fr/particuliers/vosdroits/F37400) - Retraite progressive
- [legifrance.gouv.fr](https://www.legifrance.gouv.fr/codes/id/LEGITEXT000006070302/) - Code des pensions

### Documentation technique
- [Décret n° 2023-799](https://www.legifrance.gouv.fr/jorf/id/JORFTEXT000047970226) - Surcote parentale
- [Décret n° 82-624](https://www.legifrance.gouv.fr/loda/id/LEGITEXT000006065164/) - Temps partiel
- [Loi n° 2023-270](https://www.legifrance.gouv.fr/jorf/id/JORFTEXT000047392200) - Réforme des retraites

### Ressources complémentaires
- [info-retraite.fr](https://www.info-retraite.fr) - Portail commun des régimes de retraite
- [INSEE](https://www.insee.fr/fr/statistiques/8327319) - Tables de mortalité

---

## 🙏 Remerciements

Ce simulateur a été développé pour aider les fonctionnaires d'État à mieux comprendre les mécanismes complexes de la retraite progressive. Il s'appuie sur :
- Les textes réglementaires officiels
- Les guides du Service des Retraites de l'État
- Les retours d'expérience des utilisateurs
- Les corrections apportées suite aux vérifications des sources officielles

**Un merci particulier** aux utilisateurs qui ont signalé les inexactitudes concernant l'évolution de la pension provisoire, permettant ainsi la correction majeure de la V.04.2.4.

---

## 📄 Licence et utilisation

Ce simulateur est fourni à titre **informatif et pédagogique**. Il ne remplace pas une consultation officielle auprès du SRE ou d'ENSAP.

**Utilisation libre** pour un usage personnel. La redistribution ou l'utilisation commerciale nécessite une autorisation.

**Clause de non-responsabilité** : Les résultats fournis sont des estimations. Seuls les calculs officiels du SRE font foi.

---

**Version du mode d'emploi :** V.04.2.4 - Janvier 2025

**Dernière mise à jour :** Correction documentation pension provisoire (conforme sources officielles SRE)

**Prochaine mise à jour prévue :** Mise à jour de la valeur du point d'indice (juillet 2025)

