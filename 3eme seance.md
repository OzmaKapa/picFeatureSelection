### **Amélioration du format d'affichage des résultats**

#### **5 novembre**
Dans le cadre de la recherche exhaustive des meilleures combinaisons de features, nous avons modifié le format de sortie des résultats. Les ajustements réalisés sont les suivants :  
- **Passage de CSV à Excel :** Les résultats sont désormais enregistrés dans des fichiers Excel pour une meilleure compatibilité et lisibilité.  
- **Ajout d'indicateurs binaires pour les attributs :**
  Chaque attribut est désormais représenté par une colonne avec une valeur binaire :
  - **1 :** Attribut sélectionné dans la combinaison.
  - **0 :** Attribut non sélectionné.  
- **Ajout du calcul des écarts (gaps) :** Deux métriques ont été introduites pour comparer chaque combinaison avec la meilleure :
  - **Gap1 :** Différence entre le score de la combinaison et le meilleur score.  
  - **Gap2 :** Pourcentage de cet écart par rapport au meilleur score.

Ces modifications permettent une analyse plus structurée et facilitent l'interprétation des résultats obtenus.


