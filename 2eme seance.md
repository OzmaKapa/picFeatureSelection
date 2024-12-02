# **Rapport du 22 octobre - Optimisation de la Sélection des Features**

## **1. Introduction**
Dans le cadre de notre projet visant à optimiser la sélection des features, nous poursuivons nos travaux sur l’évaluation et la comparaison des méthodes de sélection. Après avoir étudié la recherche exhaustive, Forward SFS, et Backward SFS lors de la première phase, nous avons récemment intégré une nouvelle méthode, appelée `evaluate_feature_combinations`, et mis en place un calcul pour quantifier les écarts (gap) entre les scores obtenus par les approches séquentielles (SFS) et l’optimum atteint par la recherche exhaustive.

---

## **2. Méthodes Ajoutées**

### **2.1 Méthode `evaluate_feature_combinations`**
Nous avons implémenté une fonction modulaire permettant d’évaluer les performances des différentes approches de sélection de features. Cette méthode se distingue par sa flexibilité et sa capacité à automatiser la comparaison des résultats.

#### **Paramètres :**
- **Dataset** : Les données d’entrée utilisées pour les tests (peuvent inclure des variables explicatives et une cible).
- **Modèle** : L’algorithme de machine learning appliqué (exemple : régression logistique, Random Forest).
- **Score** : La métrique choisie pour évaluer la performance (par exemple, précision, F1-score, ou RMSE).

#### **Fonctionnalités :**
- **Recherche exhaustive** :
  - Analyse toutes les combinaisons possibles des features pour trouver l’ensemble optimal.
  - Fournit une référence idéale pour évaluer les autres méthodes.
- **Forward SFS** :
  - Ajoute itérativement les features les plus pertinentes selon le modèle et la métrique choisie.
- **Backward SFS** :
  - Retire itérativement les features les moins pertinentes jusqu’à trouver le sous-ensemble optimal.

#### **Retour :**
La méthode retourne les scores pour les trois approches, permettant une comparaison directe.

---

### **2.2 Calcul du Gap**
Un calcul du gap a été intégré pour quantifier l’écart entre les résultats des méthodes séquentielles (Forward et Backward SFS) et ceux de la recherche exhaustive.

#### **Objectif :**
- Identifier dans quelle mesure les méthodes approximatives (Forward et Backward SFS) s’écartent de l’optimum théorique.

#### **Formule utilisée :**
\[
\text{Gap} = | \text{Score}_{\text{exhaustive}} - \text{Score}_{\text{SFS}} |
\]

#### **Particularités :**
- Le gap est calculé pour chaque méthode (Forward SFS et Backward SFS).
- Permet une évaluation quantitative des différences.
