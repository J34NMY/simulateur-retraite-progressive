# Historique des versions (CHANGELOG)

Toutes les modifications notables sont documentées dans ce fichier.  
Format : [Version] — Date — Description

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
