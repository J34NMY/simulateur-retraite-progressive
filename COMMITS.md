# Historique des commits — simulateur-retraite-progressive

Ce fichier documente les évolutions majeures du simulateur, avec une convention de nommage pour faciliter la traçabilité et la compréhension.

## Convention utilisée

Format : `[type] [zone] : [action ou contenu]`

- `feat` → ajout de fonctionnalité
- `fix` → correction d’un bug ou d’un calcul
- `doc` → documentation ou amélioration du README
- `legal` → mentions légales, licence
- `meta` → métadonnées, version, mentions IA
- `style` → mise en forme, interface

---

## V.04.2.6 (Octobre 2025)

- `[feat] exportsPDF : support natif des accents (jsPDF 2.5.1)`
- `[legal] LICENSE.txt : ajout ligne introductive + texte officiel`
- `[doc] README : ajout résumé express de la licence`
- `[meta] simulateur.html : mise à jour mentions Claude (Anthropic)`
- `[doc] README : documentation phase de validation en cours`
- `[legal] mentions légales : avertissements renforcés (PDF, footer, bannière)`
- `[fix] simulateur.html : correction toutes les dates affichées`

## V.04.2.5 (Janvier 2025)

- `[fix] calculsSRE : remplacement barèmes secteur privé → FP`
- `[feat] analyseRachat : interpolation des coefficients selon âge`
- `[doc] README : tableau comparatif des coûts rachat`
- `[legal] mentions légales : avertissements sur caractère indicatif`

## V.04.2.4 (Janvier 2025)

- `[fix] pensionProvisoire : correction évolution quotité`
- `[doc] README : ajout encadré informatif dans Paramètres`
- `[doc] Sources : mise à jour références réglementaires`

## V.04.2.3 (Janvier 2025)

- `[feat] retraiteDefinitive : ajout nouvel onglet`
- `[feat] simulateur.html : intégration Décret 1982 (6/7ème et 32/35ème)`
- `[style] graphique : optimisation responsive (aspectRatio 3, max-width 800px)`

## V.04.2.x (2024)

- `[style] interface : amélioration ergonomie et lisibilité`
- `[meta] simulateur.html : mise à jour mentions IA et version`

## V.04.1.x (2024)

- `[feat] analyseRachat : création onglet dédié (barèmes erronés)`
- `[doc] README : documentation rachat de trimestres`

## V.04.0.x (2023)

- `[feat] surcoteParentale : intégration Décret 2023-799`
- `[doc] README : explication surcote parentale`
