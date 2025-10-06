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
2. **Surcote parentale** : 1,25% par trimestre l'année avant l'âge légal (max 5%)
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

**Simulation V.04.2.5 (NOUVEAU - CORRECT) :**
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

### Le graphique ne s'affiche pas
- Vérifiez que vous avez bien cliqué sur "Calculer la simulation"
- Actualisez la page (F5)
- Essayez un autre navigateur (Chrome, Firefox, Edge)

### Les résultats semblent bizarres
1. Cliquez sur "Valeurs par défaut"
2. Testez avec l'exemple fourni
3. Si l'exemple fonctionne, revérifiez vos données personnelles

### Les coûts de rachat me semblent trop élevés - NOUVEAU

**Si vous utilisez une version antérieure à V.04.2.5 :**
- Les barèmes étaient ceux du secteur privé (2-3× trop cher)
- Téléchargez la version V.04.2.5 avec les coefficients corrects

**Si vous utilisez V.04.2.5 :**
- Les coefficients sont indicatifs (base 2024, catégorie sédentaire)
- Pour un devis précis, contactez le SRE via [ensap.gouv.fr](https://ensap.gouv.fr)

### Le PDF ne se génère pas
- Vérifiez que vous avez calculé une simulation avant d'exporter
- Essayez un autre navigateur
- Vérifiez que les pop-ups ne sont pas bloquées
- Actualisez la page et recommencez

### Le PDF contient des caractères étranges
- Ce problème a été corrigé en V.04.2.5.1
- Téléchargez la dernière version
- La fonction `nettoyerPourPDF()` convertit automatiquement tous les accents

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
- **V.04.2.5.1** : Exports PDF + mentions légales complètes

---

## ✅ Checklist avant de partir en retraite

- Simulation sur ce simulateur
- Simulation sur [ensap.gouv.fr](https://ensap.gouv.fr) (obligatoire)
- Vérification du relevé de carrière SRE
- Validation des bonifications enfants (si applicable)
- Décision sur la surcotisation (si temps partiel)
- Analyse du rachat de trimestres (si pertinent) avec V.04.2.5
- Demande de devis officiel rachat au SRE (si intéressé)
- Constitution du dossier de demande (6 mois avant)
- Validation de l'indice majoré (règle des 6 mois)
- Anticipation des impacts fiscaux
- Préparation des justificatifs (enfants, études, etc.)
- Compréhension du mécanisme de la pension provisoire
- Anticipation d'éventuels changements de quotité pendant la progressive
- **Conservation des PDFs** de toutes vos simulations

---

## 📝 Historique des versions

### V.04.2.5.1 (Octobre 2025) - ACTUELLE

- Ajout exports PDF avec conversion automatique des accents
- 3 types d'exports : Résultats RP, Retraite Définitive, Analyse Rachat
- Fonction `nettoyerPourPDF()` pour compatibilité universelle
- Nouvel onglet "Mentions Légales" complet
- Bannière de consentement utilisateur
- Documentation développement avec Claude (Anthropic)
- Correction toutes les dates : Octobre 2025
- Modèle 100% gratuit confirmé

### V.04.2.5 (Janvier 2025)

- CORRECTION MAJEURE : Remplacement barèmes secteur privé → coefficients Fonction Publique d'État
- Calcul rachat : Traitement × Coefficient × Nb trimestres
- Interpolation linéaire des coefficients selon âge précis
- Division des coûts par ~2,5 (exemple : 15 200 € → 5 836 €)
- Tableau des coefficients dans onglet Sources
- Avertissements renforcés sur caractère indicatif

### V.04.2.4 (Janvier 2025)

- **CORRECTION MAJEURE** : Documentation pension provisoire (évolution quotité)
- Ajout encadré informatif dans Paramètres
- Mise à jour onglet Sources
- Correction MODE_EMPLOI.md et README.md
- Erreur corrigée en V.04.2.5 : Barèmes rachat secteur privé

### V.04.2.3 (Janvier 2025)

- Nouvel onglet "Retraite Définitive"
- Option Décret 1982 (6/7ème et 32/35ème)
- Graphiques optimisés (aspectRatio: 3, max-width: 800px)

### Versions antérieures

- V.04.2.x : Amélioration de l'interface utilisateur
- V.04.1.x : Ajout de l'analyse de rachat (avec barèmes erronés)
- V.04.0.x : Intégration de la surcote parentale (Décret 2023-799)

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
- **Format PDF** (bouton dans chaque onglet de résultats) : pour conserver, imprimer ou partager vos résultats

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
**R :** La V.04.2.5 corrige une **erreur majeure** : les versions précédentes utilisaient les barèmes du secteur privé, donnant des coûts 2 à 3 fois trop élevés. La V.04.2.5 utilise les coefficients corrects de la Fonction Publique d'État, basés sur votre traitement indiciaire.

**Exemple :**
- V.04.2.4 : 4 trim. à 40 ans = 15 200 € (FAUX)
- V.04.2.5 : 4 trim. à 40 ans = 5 836 € (CORRECT)

### Q14 : Comment obtenir un devis officiel pour le rachat ?
**R :** Connectez-vous sur [ensap.gouv.fr](https://ensap.gouv.fr) et suivez la procédure de demande de devis. Le SRE vous fournira un devis personnalisé et opposable, tenant compte de tous vos paramètres spécifiques.

### Q15 : Le rachat de trimestres est-il déductible des impôts ?
**R :** Oui ! Les sommes versées pour le rachat de trimestres sont déductibles de votre revenu imposable, selon votre tranche marginale d'imposition (TMI). Cela réduit significativement le coût réel du rachat.

**Exemple :**
- Coût brut : 6 000 €
- TMI 30% : économie de 1 800 €
- **Coût réel : 4 200 €**

### Q16 : Comment utiliser les exports PDF ? - NOUVEAU
**R :** Les exports PDF sont parfaits pour :
- Conserver vos simulations dans le temps
- Comparer plusieurs scénarios côte à côte
- Partager avec un conseiller retraite ou votre service RH
- Imprimer pour consultation papier
- Documenter votre réflexion et vos choix

Les PDFs sont générés avec conversion automatique des accents pour être lisibles partout.

---

## 🎯 Conseils d'utilisation avancés

### Optimiser votre stratégie de retraite progressive

1. **Testez plusieurs quotités** : utilisez le graphique pour visualiser l'impact
2. **Évaluez la surcotisation** : selon votre situation fiscale et patrimoniale
3. **Anticipez les changements** : vous pouvez modifier votre quotité en cours de route
4. **Planifiez avec la majoration familiale** : 3 enfants = +10% de pension
5. **Considérez la surcote parentale** : travaillez l'année avant votre âge légal
6. **Analysez le rachat** : avec V.04.2.5, les coûts corrects le rendent plus attractif
7. **Exportez régulièrement** : conservez vos simulations en PDF pour comparaison

### Stratégies selon votre profil

**Si vous avez une longue carrière :**
- Privilégiez un départ plus tôt avec quotité basse
- La surcotisation est moins intéressante (taux plein déjà atteint)
- Le rachat est probablement inutile
- Exportez plusieurs scénarios de quotité en PDF

**Si vous avez une carrière incomplète :**
- Envisagez le rachat de trimestres pour éviter la décote
- La surcotisation peut être très rentable
- Utilisez V.04.2.5 pour calculer le vrai coût du rachat
- Exportez l'analyse rachat en PDF avant de décider

**Si vous avez des enfants :**
- Vérifiez vos droits aux bonifications
- Optimisez la surcote parentale en travaillant l'année avant l'âge légal
- Simulez avec et sans bonifications pour voir l'impact

**Si vous approchez de l'âge légal :**
- Calculez l'intérêt de poursuivre pour bénéficier de la surcote classique
- Comparez avec un départ immédiat
- Exportez les deux scénarios en PDF

**Si vous envisagez le rachat :** - NOUVEAU
- Utilisez **impérativement V.04.2.5** (barèmes corrects)
- Simulez différentes options (taux seul vs taux+durée)
- Comparez avec l'épargne selon votre TMI
- Exportez l'analyse en PDF
- Demandez un devis officiel au SRE
- Considérez l'avantage fiscal (déductibilité)

---

## 🔗 Liens utiles

### Sites officiels
- [ensap.gouv.fr](https://ensap.gouv.fr) - Espace numérique sécurisé de l'agent public
- [retraitesdeletat.gouv.fr](https://retraitesdeletat.gouv.fr) - Service des Retraites de l'État
- [service-public.fr](https://www.service-public.fr/particuliers/vosdroits/F37400) - Retraite progressive
- [service-public.fr](https://www.service-public.fr/particuliers/vosdroits/F13243) - Rachat de trimestres
- [legifrance.gouv.fr](https://www.legifrance.gouv.fr/codes/id/LEGITEXT000006070302/) - Code des pensions

### Documentation technique
- [Décret n° 2023-799](https://www.legifrance.gouv.fr/jorf/id/JORFTEXT000047970226) - Surcote parentale
- [Décret n° 82-624](https://www.legifrance.gouv.fr/loda/id/LEGITEXT000006065164/) - Temps partiel
- [Décret n° 2007-262](https://www.legifrance.gouv.fr/loda/id/JORFTEXT000000465931/) - Rachat trimestres FP
- [Loi n° 2023-270](https://www.legifrance.gouv.fr/jorf/id/JORFTEXT000047392200) - Réforme des retraites

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
- La collaboration technique avec Claude (Anthropic)

**Un merci particulier** :
- Aux utilisateurs qui ont signalé les inexactitudes concernant l'évolution de la pension provisoire (V.04.2.4)
- À l'utilisateur qui a remarqué que les coûts de rachat étaient "très chers", permettant la découverte et la correction de l'erreur majeure sur les barèmes (V.04.2.5)
- À Claude (Anthropic) pour l'assistance technique, algorithmique et réglementaire

**Ces retours ont permis des améliorations majeures qui changent significativement les résultats et les décisions !**

---

## 📄 Licence et utilisation

Ce simulateur gratuit est fourni à titre **informatif et pédagogique**. Il ne remplace pas une consultation officielle auprès du SRE ou d'ENSAP.

**Utilisation libre** pour un usage personnel. La redistribution ou l'utilisation commerciale nécessite une autorisation.

**Clause de non-responsabilité** : Les résultats fournis sont des estimations. Seuls les calculs officiels du SRE font foi.

---

**Version du mode d'emploi :** V.04.2.5.1 - Octobre 2025

**Dernière mise à jour :** Ajout exports PDF + développement avec Claude (Anthropic)

**Prochaine mise à jour prévue :** Mise à jour de la valeur du point d'indice (juillet 2026)

**Version du mode d'emploi :** V.04.2.5 - Janvier 2025

**Dernière mise à jour :** Correction barèmes rachat Fonction Publique d'État (division coûts par ~2,5)

**Prochaine mise à jour prévue :** Mise à jour de la valeur du point d'indice (juillet 2025)

