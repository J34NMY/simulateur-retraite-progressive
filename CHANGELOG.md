# Historique des versions (CHANGELOG)

Toutes les modifications notables sont documentées dans ce fichier.  
Format : [Version] — Date — Description

---

## [V.06] — Octobre 2026 — Indice majore jusqu'a 1600 (usage magistrats)

### Fichiers : `simulateur_retraite_progressive_V06_expert.html`, `simulateur_retraite_progressive_V06_guide.html`

- Le plafond de controle de l'indice majore passe de **900 a 1600** (expert et guide ; le champ du guide passe de `max="1200"` a `max="1600"`). La grille des magistrats de l'ordre judiciaire en vigueur depuis le 01/12/2025 va jusqu'a l'IM 1596 (circulaire JUSB2533423C) : jusqu'ici tout indice superieur a 900 bloquait le calcul.
- Mode d'emploi : ajout d'une note sur l'usage indicatif par un magistrat (retraite progressive ouverte, limite d'age 67 ans, maintien en activite jusqu'a 70 ans, RAFP non incluse).
- Aucune modification de la formule de calcul.

---

## [V.06] — Octobre 2026 — Regime fige par phase (RP vs definitive)

### Fichiers : `simulateur_retraite_progressive_V06_expert.html`, `simulateur_retraite_progressive_V06_guide.html`

**Correction :** jusqu'ici, V06 appliquait systematiquement le bareme Gel 2026 (LFSS 2026, art. 105) a l'ensemble du calcul, y compris a la pension provisoire d'une retraite progressive demandee avant le 01/09/2026. Or le droit a pension se fige a la date a laquelle il est ouvert, pas a la date de liquidation finale.

#### Nouveau comportement
- La **pension provisoire** (pendant la RP) applique desormais le regime en vigueur a la **date de demande de la retraite progressive** (`dateDebut`) : Reforme 2023 si cette date est anterieure au 01/09/2026, Gel 2026 sinon.
- La **pension definitive** applique le regime en vigueur a la **date de demande de retraite definitive** (`dateFin`), independamment du regime applique a la phase provisoire.
- Chaque phase reste figee sur son propre regime : une RP demandee le 01/01/2026 et liquidee le 01/10/2027 combine desormais une pension provisoire sous Reforme 2023 et une pension definitive sous Gel 2026, dans le **meme fichier** V06 (expert et guide).
- Impact concret : barème des trimestres requis, age legal de surcote classique, eligibilite a la surcote parentale (generations 1964 / 1965 T1) et majoration excedentaire (suspendue sous Gel 2026, active sous Reforme 2023) sont desormais determines independamment pour chaque phase.
- Correctif applique a tous les points de calcul : formulaire principal, graphiques (RP et definitive), export PDF (RP, definitive, et tableau comparatif par quotite), et previsualisation du nombre de trimestres requis a la saisie de la date de naissance.

**Cadre reglementaire :** Decret n°2023-799 du 21 aout 2023 (Reforme 2023) et LFSS 2026, art. 105 (suspension / gel), coexistant desormais dans un seul fichier selon la date de chaque demande.

---

## [V.05] — Juin 2026 — Gel 2026 (LFSS 2026, art. 103)

### Nouveau fichier : `simulateur_gel_2026_V05.html`

**Cadre réglementaire :** Suspension de la réforme 2023, applicable au 1er septembre 2026

#### Modifications des paramètres de retraite
- Âge légal maintenu à **62 ans** pour toutes les générations (suspension de la progressivité 62→64 ans)
- Durée de cotisation selon le **barème pré-réforme** (génération 1964 : 171 trimestres requis au lieu de 172)
- Majoration excédentaire (trimestres au-delà du taux plein) **suspendue**

#### Corrections spécifiques au gel
- Surcote parentale **non applicable** aux générations 1964 et 1er trimestre 1965 (âge légal 62T3 < 63 ans requis — source CNRACL, 19/05/2026)
- Surcote classique : plafonnée à 70 ans (confirmation ENSAP)
- Avertissement automatique si départ définitif > 31/12/2027

#### Fonctionnalités restaurées (absentes dans la première version du gel)
- Onglet **Analyse Rachat** complet : coût détaillé, impact pension, comparaison placement, recommandation actuarielle colorée, export PDF
- **Analyse de rentabilité actuarielle de la surcotisation** dans les résultats RP (fonctions `calculerRentabiliteSurcotisation` et `afficherAnalyseRentabilite`)
- Bloc surcotisation dans les résultats RP : coût mensuel, revenu net après surcotisation
- Structure HTML de l'onglet rachat enrichie : bandeau avertissement, textes d'aide, bloc coefficients indicatifs

#### Correction logique
- Cohérence entre « Comparaison stratégique » et « Recommandation » dans l'analyse surcotisation : la recommandation est désormais unifiée autour de `strategieOptimale` (surcotisation vs placement) et non plus sur des seuils de `tauxRentabilite` incohérents

---

## [V.04.2.8] — Novembre 2025 — Réforme 2023

### Fichier : `simulateur_reforme_2023_V04.2.8.html`

**Cadre réglementaire :** Décret n°2023-799 du 21 août 2023

#### Fonctionnalités principales
- Calcul complet retraite progressive (RP) et retraite définitive selon la réforme 2023
- Analyse de rentabilité actuarielle de la surcotisation (données INSEE 2024)
- Onglet Analyse Rachat : 12 coefficients par âge (20 à 62 ans), 2 options, 2 types, export PDF
- Graphique interactif des revenus selon la quotité
- Export/Import JSON des paramètres
- 31 règles de validation des données saisies

#### Corrections apportées au cours du développement (V.04.2.5 → V.04.2.8)
- Trimestres requis génération 1964 : **171** (corrigé depuis une valeur erronée de 172 provisoire)
- Taux de décote : **1,25%/trimestre** (valeur correcte FPE sédentaire)
- Application de la décote : **multiplicative** (et non soustractive) — méthode SRE confirmée
- Décret n°82-624 : calcul 6/7ème (80%) et 32/35ème (90%) correctement appliqué
- Surcote parentale : règles SRE/CNRACL correctement implémentées
- Plafond L13 : pension plafonnée à 100% du traitement, avec la majoration familiale L18 s'appliquant au-delà

---

## Versions antérieures (V.04.2.5 à V.04.2.7)

Versions de développement intermédiaires — corrections progressives de la méthode de calcul SRE, non publiées.
