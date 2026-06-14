# Guide de contribution

Merci de l'intérêt porté à ce simulateur. Les contributions sont les bienvenues, dans le respect du cadre décrit ci-dessous.

---

## Signaler une erreur de calcul (Issue)

Si vous constatez un résultat qui vous semble erroné par rapport aux simulateurs officiels, ouvrez une **Issue** en précisant :

1. **Le fichier concerné** : V.04.2.8 (réforme 2023) ou V.05 (gel 2026)
2. **Les paramètres saisis** : date de naissance, date du relevé, trimestres d'assurance et liquidables, quotité, dates de RP
3. **Le résultat obtenu** par le simulateur
4. **Le résultat attendu** issu d'ensap.gouv.fr ou info-retraite.fr (avec capture d'écran si possible)
5. **La génération concernée** (année de naissance)

> ⚠️ Ne partagez jamais votre numéro de sécurité sociale, votre identifiant ENSAP ou toute donnée d'identification personnelle dans une Issue publique.

---

## Proposer une correction (Pull Request)

1. Forkez le dépôt
2. Créez une branche nommée explicitement : `fix/decote-generation-1965` ou `feature/export-csv`
3. Effectuez la modification dans le fichier HTML concerné
4. Documentez la modification dans votre PR :
   - Quelle règle réglementaire est corrigée ou appliquée ?
   - Quelle source (texte officiel, circulaire SRE, résultat ENSAP) justifie le changement ?
   - Quels cas de test permettent de valider ?
5. Soumettez la Pull Request

---

## Ce qui est hors périmètre

Ce simulateur est dédié à la **Fonction Publique d'État, catégorie sédentaire**. Les contributions concernant :
- Le régime général (CNAV)
- La CNRACL (fonctionnaires territoriaux et hospitaliers)
- Les catégories actives ou insalubres de la FPE

...ne sont pas dans le périmètre de ce projet, même si certaines règles sont proches.

---

## Code de conduite

Les échanges doivent rester courtois, factuels et centrés sur les aspects techniques et réglementaires. Ce projet traite de sujets qui peuvent avoir des implications financières importantes pour des personnes réelles — la rigueur et la prudence sont de mise.
