# Simulateur de Retraite Progressive V.04.2.1

## Notes personnelles de développement

### Historique des versions
- **V.04.2.1** (Janvier 2025) : Ajout onglet "Analyse Rachat de trimestres"
- **V.04.2** (Janvier 2025) : Module rachat intégré
- **V.04.1.9** : Disclaimer écart SRE ajouté
- Versions antérieures : développement initial

### État actuel
- Fichier unique : `simulateur_retraite_Version_V.04.2.1.html`
- Écart connu avec SRE : 1-2 trimestres liquidables (~1-2% pension)
- Méthode de calcul : base 360 jours/an (conforme documentation SRE)

### Fonctionnalités implémentées

#### Calcul principal
- Retraite progressive (quotités 50-90%)
- Décote automatique si < trimestres requis
- Trois surcotes cumulables (classique, parentale, excédentaire)
- Bonifications enfants avant/après 2004
- Majoration familiale (10% + 5% par enfant)

#### Analyses décisionnelles
1. **Surcotisation**
   - Coût mensuel et total
   - Comparaison avec placements (2-5%)
   - Durée rentabilisation (données INSEE 2024)
   
2. **Rachat de trimestres** (V.04.2+)
   - Barèmes 2024 intégrés (taux seul / taux+durée)
   - Déduction fiscale (TMI 0-45%)
   - Comparaison rachat vs placement
   - Récupération auto données simulateur

#### Interface
- 5 onglets : Paramètres, Résultats, Graphique, Analyse Rachat, Sources
- Import/Export JSON
- Chart.js pour graphiques
- Design responsive

### Maintenance à prévoir

#### Annuelle (janvier)
- [ ] Valeur point d'indice (actuellement 4,92278 €)
- [ ] Barèmes surcotisation
- [ ] Tables mortalité INSEE
- [ ] Barèmes rachat trimestres

#### Événementielle
- [ ] Nouveaux décrets retraite progressive
- [ ] Modifications durées cotisation
- [ ] Changements bonifications

### Ressources techniques

#### Structure code
HTML (structure) : ~600 lignes
CSS (style) : ~200 lignes
JavaScript (logique) : ~1700 lignes
Total : ~2500 lignes

#### Dépendances externes
- Chart.js 4.4.1 (CDN)
- Aucune autre dépendance

#### Navigateurs testés
- Chrome 120+ ✓
- Firefox 121+ ✓
- Safari 17+ ✓
- Edge 120+ ✓

### Points d'attention

**Écart avec SRE officiel**
- Cause probable : règles d'arrondi internes non documentées
- Trimestres liquidables : différence de 1-2 trimestres
- Impact pension : ~1-2%
- Solution : disclaimer visible dans résultats

**Formules critiques**
```javascript
// Arrondi trimestres liquidables
const trimestresComplets = Math.floor(totalJours / 90);
const joursRestants = totalJours % 90;
return trimestresComplets + (joursRestants >= 45 ? 1 : 0);
Calcul surcotes cumulables

Parentale en premier (max 4 trimestres)
Classique ensuite (âge légal → 67 ans)
Excédentaire sur le reste

TODO / Améliorations futures
Court terme

 Valider barèmes rachat 2025
 Tester cas limites (âges extrêmes)
 Optimiser performance graphique

Moyen terme

 Ajouter RAFP (Retraite Additionnelle)
 Export PDF résultats
 Historique simulations (localStorage possible ?)
 Mode sombre

Long terme (si publication)

 Nettoyage code
 Documentation technique complète
 Tests unitaires
 API REST ?

Notes de calcul
Base SRE : 360 jours/an
1 an = 360 jours
1 mois = 30 jours
1 trimestre = 90 jours
Temps partiel

Assurance : toujours 100%
Liquidables : quotité × durée (sauf surcotisation)

Décote (si < trimestres requis)

Nés avant 1964 : 1,25% par trimestre
Nés 1964+ : 1,09% par trimestre
Maximum : 25%
Annulation automatique à 67 ans

Surcote parentale (2023)

Conditions : né 1964+, enfants, taux plein atteint
Calcul : quotité × 4 trimestres (max)
Taux : 1,25% par trimestre
Maximum : 5%

Sauvegarde et versioning
Format export JSON
json{
  "version": "V.04.2.1",
  "decret": "Décret n° 2023-799 du 21 août 2023",
  "dateExport": "2025-01-XX",
  "indice": 478,
  "valeurPoint": 4.92278,
  ...
}
Nommage fichiers

Format : simulateur_retraite_Version_V.XX.X.X.html
Garder historique des versions majeures

Contacts utiles (si questions)

SRE : https://retraitesdeletat.gouv.fr
ENSAP : https://ensap.gouv.fr
Légifrance : https://www.legifrance.gouv.fr


Mémo personnel : Ne pas oublier que cet outil est une aide à la décision, pas un document officiel. Toujours recommander ENSAP pour estimation définitive.

**Instructions** :
1. Créez un fichier nommé `README.md` dans votre dépôt GitHub
2. Copiez tout le contenu ci-dessus
3. Collez-le dans le fichier README.md
4. Sauvegardez

C'est adapté à un usage privé : notes techniques, TODO personnelles, points d'attention code. Si plus tard vous rendez le dépôt public, vous remplacerez par le README PUBLIC que je vous ai fourni.
