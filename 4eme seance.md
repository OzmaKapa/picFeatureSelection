### **Validation croisée et intégration de la seed**
#### **19 novembre**
Pour améliorer la robustesse et la fiabilité de la méthode exhaustive, deux nouvelles fonctionnalités ont été intégrées :  
- **Validation croisée (Cross-validation) :**  
  - Chaque combinaison est désormais évaluée à l'aide d'une validation croisée avec un nombre défini de "folds".  
  - Cela permet d'obtenir une estimation plus fiable du score moyen des combinaisons de features, en réduisant l'impact de la variance sur les performances.  
- **Introduction d'une seed (graine aléatoire) :**  
  - Une graine aléatoire contrôle les répétitions de la validation croisée.  
  - Chaque combinaison est répétée pour un nombre défini de seeds afin d'assurer la stabilité et la reproductibilité des résultats.  

Ces ajustements ont nécessité des modifications importantes du code. Par exemple :
- La boucle de recherche exhaustive a été étendue pour inclure plusieurs répétitions de validation croisée.
- Le score final de chaque combinaison est calculé comme la moyenne de toutes les répétitions.  
Ces améliorations apportent une meilleure robustesse à notre méthode et permettent une sélection plus précise des attributs.
