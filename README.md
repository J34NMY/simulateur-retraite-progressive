# 🇫🇷 Simulateur de Retraite Progressive - Version V.04.2

## 🎯 Vue d'ensemble du Projet

Ce dépôt contient le code du **Simulateur de Retraite Progressive - Version V.04.2**, un outil d'aide à la décision open source conçu spécifiquement pour les **fonctionnaires d'État** (SRE).

Son objectif principal est de vous permettre de **planifier votre fin de carrière**, d'étudier des scénarios (temps partiel, surcotisation, retraite progressive) et de vérifier la cohérence des calculs officiels grâce à une grande transparence de ses formules.

---

## ⚖️ Non-Opposabilité et Fiabilité

Il est crucial de comprendre que cet outil n'est **PAS OFFICIEL** et n'a **AUCUNE VALEUR JURIDIQUE** face à l'administration.

| Aspect | Simulateur Non-Officiel (Ce fichier) | Simulateur Officiel (SRE/ENSAP) |
| :--- | :--- | :--- |
| **Valeur** | Aide à la décision, anticipation, pédagogie et vérification. | **Référence légale et administrative unique.** |
| **Opposabilité** | **Nulle.** Le résultat peut différer légèrement (écart d'arrondis ou subtilités administratives) et ne fait pas foi. | **Maximale.** Le résultat est celui appliqué par l'administration. |
| **Transparence** | **Très élevée.** Les formules et barèmes utilisés (surcote, décote) sont explicites dans le code. | Souvent opaque ("boîte noire"). |

**Recommandation :** Utilisez ce simulateur pour **construire votre stratégie** et **contrôler** le calcul final de votre droit.

---

## ✨ Forces et Fonctionnalités

Le simulateur se distingue par l'intégration de règles complexes et une approche pédagogique :

* **Calcul de la Retraite Progressive :** Détermine précisément la fraction de pension perçue en fonction de la quotité de travail à temps partiel.
* **Formule Explicite :** La base du calcul est clairement affichée :
    $$ \text{Pension} = \text{Traitement indiciaire} \times 75\% \times \frac{\text{Trimestres liquidables}}{\text{Trimestres requis}} $$
* **Mise à Jour Législative :** Il est basé sur la législation post-réforme, intégrant notamment :
    * Le **Décret n° 2023-799** (Réforme des retraites).
    * L'âge minimum de **60 ans** et la condition des **150 trimestres** pour l'ouverture du droit à la retraite progressive (selon le Décret de 2025).
* **Analyse de Surcotisation :** Il permet d'évaluer l'impact financier précis d'une surcotisation pour le temps partiel.

---

## 🛠️ Maintenance et Mise à Jour des Règles

La fiabilité de l'outil dépend d'une veille réglementaire :

1.  **Contrôle Annuel (Chaque Janvier) :**
    * Mettre à jour la **valeur du point d'indice** (traitement indiciaire) et le montant du **Minimum Garanti (MG)**, qui sont revalorisés annuellement.
2.  **Contrôle Événementiel :**
    * Vérifier immédiatement les règles et les barèmes après la publication de tout nouveau décret ou loi touchant la **retraite progressive**, les **trimestres requis**, ou les **bonifications/majorations**.
