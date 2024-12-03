**                              

`                                   `**Compte rendu 1**

**Date :** 15 octobre
**Participants :** Hafsa Ed-Dahni,Safae errazki,Yasmine Skandrani

**Encadre par :** Arnaud Liefooghe


**Objectif de la réunion :** Planifier les premières étapes du projet et explorer les approches initiales pour la sélection d'attributs.

**1. Ordre du jour :**

- Comprendre les bases théoriques du projet.
- Déterminer les méthodes d'évaluation initiales pour la sélection d'attributs.
- Identifier les outils et techniques à utiliser.

**2. Points discutés :**

1. **Définition et enjeux de la sélection d'attributs :**
   1. Discussion sur l’importance de choisir un sous-ensemble optimal d’attributs pour améliorer la performance des modèles d’apprentissage automatique et faciliter leur interprétabilité.
   1. Analyse des défis associés, notamment la complexité combinatoire et les biais liés aux méthodes de recherche gloutonne.
1. **Techniques abordées :**
   1. **Recherche exhaustive :**
      Une approche systématique a été réalisée pour énumérer toutes les combinaisons possibles des attributs. Bien que coûteuse en termes de temps et de ressources, cette méthode garantit l’identification du sous-ensemble optimal pour un modèle donné.
   1. **Sélection séquentielle d'attributs en avant (Forward-SFS) :**
      Méthode consistant à construire progressivement un sous-ensemble d'attributs en ajoutant les plus pertinents à chaque itération.
   1. **Sélection séquentielle d'attributs en arrière (Backward-SFS) :**
      Technique inverse qui commence avec tous les attributs, puis retire les moins contributifs de manière itérative.



1. **Premières observations :**
   1. La recherche exhaustive a permis de valider l'efficacité théorique des méthodes locales comme FSFS et BSFS, mais sa faisabilité reste limitée pour de grands ensembles d’attributs.
   1. Les datasets ont été téléchargés depuis la plateforme **UCI Machine Learning Repository**, ce qui permettra de tester et comparer les méthodes abordées.
   1. Lors de cette réunion on a prévu de :
      1. Énumérer toutes les solutions (combinaisons possibles d'attributs).
      1. Calculer les scores associés pour chaque combinaison en utilisant les métriques **Balanced Accuracy**, **Précision Macro** et **F1-score**.
      1. Sauvegarder les résultats dans un fichier pour une analyse ultérieure.
      1. Mettre en œuvre ces étapes avec les trois méthodes : recherche exhaustive, Forward-SFS, et Backward-SFS.

**3. Décisions prises :**

- Effectuer une revue approfondie sur les approches existantes pour mieux comprendre les algorithmes avancés.
- Implémenter les trois méthodes sur des jeux de données téléchargés de la plateforme UCI.
- Comparer les résultats obtenus pour chaque méthode et chaque métrique

