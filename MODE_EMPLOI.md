# 📖 Mode d'emploi – Simulateur de Retraite Progressive

**Fonctionnaire d'État – Catégorie sédentaire**

> ⚠️ Outil éducatif non officiel. Pour votre estimation officielle, consultez le simulateur M@rel sur [info-retraite.fr](https://www.info-retraite.fr) et le SRE via [ensap.gouv.fr](https://ensap.gouv.fr).

---

## 🚀 Démarrage rapide

1. Accédez directement au simulateur en ligne : **[https://j34nmy.github.io/simulateur-retraite-progressive/](https://j34nmy.github.io/simulateur-retraite-progressive/)**
2. Choisissez la version adaptée à votre situation (voir tableau ci-dessous)
3. Munissez-vous de votre **Relevé Individuel de Situation (RIS)** disponible sur [info-retraite.fr](https://www.info-retraite.fr)
4. Remplissez les étapes ou l'onglet **Paramètres** puis cliquez sur **"Calculer la simulation"**

> 💡 Aucune installation requise. Aucune donnée n'est transmise — tout reste dans votre navigateur.

---

## 📂 Quelle version utiliser ?

| Version | Cadre réglementaire | Public cible |
|---|---|---|
| **V04.2.8** | Réforme 2023 — Décret n°2023-799 du 21 août 2023 | Départ prévu à partir de 2028 |
| **V06 — Mode Expert** ⭐ | Suspension réforme 2023 — LFSS 2026, art. 105 | Utilisateurs à l'aise avec les formulaires |
| **V06 — Assistant Guidé** ✨ | Suspension réforme 2023 — LFSS 2026, art. 105 | Découverte · Première utilisation |

### 🧭 Expert ou Guidé ?

| | Assistant Guidé | Mode Expert |
|---|---|---|
| **Saisie** | Pas à pas, 6 étapes | Formulaire complet |
| **Résultats** | Retraite Progressive + tableau comparatif | RP + Définitive + Rachat + Graphiques + PDF |
| **Validation** | Immédiate à chaque étape | À la soumission |
| **Pour qui ?** | Première utilisation | Simulation avancée |

> 💡 L'Assistant Guidé dispose d'un bouton **"Mode Expert"** pour basculer vers la version complète à tout moment.

---

## 1️⃣ Onglet Paramètres

⚠️ Les valeurs qui s'affichent a l'ouverture sont des valeurs d'exemples a modifier selon vos données.

### Données du relevé de carrière

**Date du relevé**
Date de votre dernier relevé de carrière officiel SRE. Disponible sur [info-retraite.fr](https://www.info-retraite.fr).

**Trimestres d'assurance au relevé + jours résiduels**
Nombre de trimestres d'assurance selon votre relevé, plus les jours au-delà des trimestres complets.
- Exemple : 160 trimestres + 84 jours
- Les trimestres d'assurance permettent d'éviter la décote

> 📋 **Où les trouver sur votre relevé info-retraite.fr ?**
> En haut du relevé, section **"Durée d'assurance en trimestres"** — c'est le total tous régimes confondus affiché en grand (ex : *"164 trimestres et 84 jours enregistrés"*).

**Trimestres liquidables au relevé + jours résiduels**
Nombre de trimestres de services effectifs selon votre relevé, plus les jours résiduels.
- Exemple : 142 trimestres + 86 jours
- Les trimestres liquidables déterminent le montant de la pension (prorata)

> 📋 **Où les trouver sur votre relevé info-retraite.fr ?**
> Dans la section **"Mes régimes"**, cherchez la ligne **SRE** (Service des Retraites de l'État / Finances Publiques). La colonne **"Total des trimestres"** affiche vos trimestres liquidables (ex : *"146 et 14 jours"*). Le mot "Liquidable" apparaît parfois en marge — c'est bien cette ligne qu'il faut utiliser, et non le total d'assurance affiché en haut.

> ⚠️ Les trimestres et jours sont toujours saisis séparément. 90 jours = 1 trimestre (méthode SRE base 360 j/an).

---

### Informations personnelles

**Date de naissance**
Obligatoire — détermine l'âge légal et les trimestres requis selon votre génération.

**Sexe**
Utilisé uniquement pour l'analyse actuarielle de rentabilité (tables de mortalité INSEE 2024).

**Trimestres requis**
Calculé automatiquement selon votre année de naissance.

| Génération | Réforme 2023 (V04.2.8) | Gel 2026 (V06) |
|---|---|---|
| 1958-1960 | 168 | 168 |
| 1961-1962 | 168-169 | 168-169 |
| 1963 | 170 | 170 |
| **1964** | **171** | **170** |
| **1965** | **172** | **170-171** |
| 1966-1967 | 171-172 | 171 |
| 1968+ | 172 | 172 |

**Indice majoré (IM)**
Votre indice majoré actuel, visible sur votre bulletin de paie (ligne traitement brut).
> ⚠️ Règle des 6 mois : une augmentation d'indice doit avoir au moins 6 mois d'ancienneté avant le départ pour être prise en compte.

**Valeur du point**
Valeur officielle : **4,92278 €** (depuis le 1er juillet 2023).

---

### Planning de retraite progressive

**Date de départ retraite progressive**
Date de début de votre temps partiel. Conditions minimales : 60 ans + 150 trimestres d'assurance.

**Date de départ retraite définitive**
Date de fin de la période progressive et de liquidation complète de votre pension.

**Quotité entre relevé et départ progressif**
Votre quotité de travail entre la date du relevé et le début de la retraite progressive.
- Si vous travaillez à **temps plein** : saisissez 100%
- Si vous étiez déjà à **temps partiel** (80%, 90%...) avant la retraite progressive : saisissez votre quotité réelle

> Cette valeur impacte l'accumulation de trimestres liquidables sur la période entre le relevé et le départ progressif. Un fonctionnaire à 80% depuis plusieurs années accumule des liquidables au prorata de sa quotité.

**Quotité pendant la retraite progressive**
Votre quotité pendant la période progressive : 50%, 60%, 70%, 80% ou 90%.
> Cette quotité impacte le calcul de la pension provisoire et, le cas échéant, la surcote parentale.

**Décret n°82-624 (coché par défaut)**
Pour certains fonctionnaires en temps partiel de droit commun :
- 80% → rémunération réelle à **6/7ème** (≈ 85,71%)
- 90% → rémunération réelle à **32/35ème** (≈ 91,43%)

Pour vérifier : consultez votre bulletin de paie. Si vous travaillez à 80% et êtes payé plus que 80%, ce décret s'applique.

---

### Options de surcotisation (V06)

Si coché, vos trimestres liquidables comptent à **100%** pendant la période progressive (même à temps partiel), moyennant un surcoût de cotisation.

> ⚠️ **Limite réglementaire — Art. L11 bis CPCMR :** La surcotisation est limitée à **4 trimestres supplémentaires maximum sur l'ensemble de la carrière**. Si vous avez déjà surcotisé dans le passé, indiquez le nombre de trimestres déjà utilisés dans le champ prévu — le simulateur calculera les trimestres encore disponibles et bloquera automatiquement la surcotisation si le plafond est atteint.

> 💡 **Comment savoir combien de trimestres vous avez déjà utilisés ?** Renseignez-vous auprès de votre employeur ou consultez votre espace personnel sur [ensap.gouv.fr](https://ensap.gouv.fr).

Le taux de surcotisation est calculé automatiquement selon votre quotité (barème 2024) :

| Quotité | Taux de surcotisation | Durée max utile |
|---|---|---|
| 50% | 23,85% | ~2 ans |
| 60% | 21,30% | ~2,5 ans |
| 70% | 18,75% | ~3,3 ans |
| 80% | 16,20% | **~5 ans** |
| 90% | 13,65% | ~10 ans |

---

### Droits liés aux enfants

**Bonification (enfants nés/adoptés avant 2004)**
- Conditions : interruption ou réduction d'activité ≥ 2 mois + enfant élevé ≥ 9 ans avant ses 16 ans
- Gain : **4 trimestres liquidables + 4 trimestres d'assurance** par enfant

**Majoration (enfants nés/adoptés à partir de 2004)**
- Conditions : naissance/adoption après recrutement dans la fonction publique
- Gain : **2 trimestres d'assurance** par enfant (pas d'impact sur les liquidables)

**Majoration familiale (Article L18)**
Calculée automatiquement sur le total d'enfants élevés :
- 3 enfants → +10%
- 4 enfants → +15%
- 5 enfants → +20% (etc.)

---

## 2️⃣ Résultats de la simulation

Après calcul, le simulateur affiche :

- **Durées** : périodes calculées en méthode SRE (base 360 j/an)
- **Compteurs au départ progressif** : assurance et liquidables à la date de début de la RP
- **Revenus pendant la RP** : traitement à la quotité + pension provisoire + net après surcotisation si applicable
- **Analyse de rentabilité surcotisation** : tableau comparatif 3 placements (voir ci-dessous)
- **Tableau comparatif par quotité** : revenus totaux pour les 5 quotités possibles (50% à 90%)
- **Situation en fin de période** : compteurs finaux, taux de liquidation
- **Pension définitive estimée** : montant principal + majoration familiale si applicable
- **Décote ou surcote** : détail des trimestres manquants ou des majorations appliquées
- **Export PDF** : bouton en bas de page pour télécharger les résultats

### Fonctionnement de la pension provisoire

| Élément | Explication |
|---|---|
| Calculée au départ | Sur les droits acquis AVANT le départ progressif |
| Évolution | Si vous changez de quotité, la part versée s'ajuste automatiquement |
| Pendant la RP | Les nouveaux trimestres ne modifient PAS le montant provisoire |
| Retraite définitive | Tous les droits acquis pendant la RP sont pris en compte au recalcul final |

### Analyse de rentabilité de la surcotisation

Quand la surcotisation est cochée, le simulateur compare automatiquement le **supplément de pension** obtenu avec 3 scénarios de placement alternatif :

| Placement | Taux | Profil |
|---|---|---|
| Livret A | 1,7% | Garanti, disponible, variable |
| Assurance-vie fonds euros | 3,5% | Garanti, peu risqué |
| PEA ETF MSCI World | 5% | Non garanti, long terme |

> **À vous de décider :** la surcotisation génère un supplément de pension à vie mais le capital investi est définitivement perdu. Le placement génère un revenu mensuel sur intérêts avec le capital conservé et transmissible à vos héritiers. La décision dépend de votre situation patrimoniale et familiale.

---

## 3️⃣ Mode Expert — fonctionnalités avancées

Le **Mode Expert (V06)** donne accès à des onglets supplémentaires non disponibles dans l'Assistant Guidé :

### Onglet Retraite Définitive

Permet de simuler une retraite définitive sans période progressive, selon différents scénarios de quotité.

1. Cliquez sur **"↻ Récupérer les données"** pour importer vos paramètres
2. Saisissez votre date de départ et la quotité envisagée jusqu'à la retraite
3. Cochez éventuellement la surcotisation si applicable
4. Cliquez sur **"Calculer la simulation"**

### Onglet Graphique

Affiche la courbe des revenus totaux bruts selon la quotité de travail pendant la retraite progressive. Le point rouge indique votre quotité choisie.

### Onglet Analyse Rachat

Évalue si le rachat ou la surcotisation rétroactive est financièrement pertinent par rapport à un placement alternatif.

1. Cliquez sur **"↻ Récupérer les données"** pour pré-remplir depuis vos paramètres
2. Choisissez le **type** :

| Type | Description |
|---|---|
| Années d'études supérieures | Rachat classique Art. L9 bis CPCMR |
| Années civiles incomplètes | Rachat classique Art. L9 bis CPCMR |
| **Surcotisation rétroactive** | Récupérer des trimestres perdus pendant des périodes à temps partiel **depuis le 01/01/2004** (Art. L11 bis + Décret 2004-678) |

3. Pour le rachat classique, choisissez l'option :
   - **Option 1 (Taux seul)** : évite la décote, n'augmente pas le montant de la pension
   - **Option 2 (Taux + Durée)** : augmente aussi la durée d'assurance → gain de pension
4. Saisissez l'âge au moment du rachat et votre TMI
5. Cliquez sur **"Analyser la rentabilité"**

#### Surcotisation rétroactive (Art. L11 bis CPCMR)

Permet de récupérer des trimestres liquidables perdus pendant des périodes à temps partiel effectuées depuis le 01/01/2004, dans la limite de **4 trimestres sur toute la carrière**.

> **Exemple :** Vous avez travaillé 10 ans à 80% en début de carrière (sans surcotiser à l'époque). Vous pouvez demander rétroactivement à surcotiser pour récupérer jusqu'à 4 trimestres perdus. Le coût est calculé selon le Décret n°2004-678.

> ⚠️ Les coefficients utilisés sont **indicatifs** (base 2024, catégorie sédentaire). Demandez toujours un devis officiel au SRE via [ensap.gouv.fr](https://ensap.gouv.fr).

### Onglet Sources

Références réglementaires complètes utilisées dans le simulateur.

### Onglet Mentions Légales

Conditions d'utilisation, limites de responsabilité, politique de confidentialité (aucune donnée transmise).

---

## 💾 Export et sauvegarde (Mode Expert)

- **Exporter** : sauvegarde tous les paramètres en fichier JSON pour les recharger ultérieurement
- **Importer** : rechargement d'une session précédente
- **Export PDF** : disponible dans les onglets Résultats RP, Retraite Définitive et Analyse Rachat

---

## 🔒 Confidentialité

Toutes les données restent **exclusivement dans votre navigateur**. Aucune information n'est transmise à un serveur. Le simulateur fonctionne entièrement hors ligne une fois la page chargée.

---

## ❓ Que faire si les résultats diffèrent d'info-retraite.fr ?

Vérifiez :
1. Que les jours résiduels sont bien saisis séparément des trimestres complets
2. Que la date du relevé est exacte
3. Que les bonifications enfants correspondent à votre situation réelle
4. Que la quotité avant la RP est correctement renseignée

Si l'écart persiste, ouvrez une **Issue** sur le dépôt GitHub en indiquant vos valeurs et le résultat info-retraite.fr attendu.

---

*Développé bénévolement par J34NMY · Licence CC BY-NC-SA 4.0 · Juin 2026*
