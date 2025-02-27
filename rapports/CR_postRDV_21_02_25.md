PLDAC RL Tabulaire \- Bilan post RDV 21-02-2025

Sujets abordés durant la réunion : 

**Discussions des hyperparamètres**

* **Alpha (α)** : Taux d'apprentissage, contrôle la rapidité d'adaptation du modèle.

énoncé du projet

* **Épsilon-greedy (ϵ)** : Stratégie d'exploration  
  Avec probabilité qui détermine si une action est choisie **au hasard** ou si on prend l'action optimale  
* **Softmax (β)** : Contrôle le degré d'aléatoire dans le choix des actions  
  Plus β est **grand**, plus la politique devient **déterministe** (les actions avec de meilleures valeurs sont favorisées).  
  Plus β est **petit**, plus les actions sont choisies de manière **aléatoire**.  
* **Gamma (γ)** : Facteur d'actualisation  
  Définit à quel point les récompenses futures influencent les décisions actuelles.  
  Un gamma élevé favorise une vision à long terme, tandis qu'un gamma faible privilégie des gains immédiats.


**Introduction à certains aspects du projet**  
Cadre **model-free**  
Le **Critic** utilise une fonction de valeur V(s) plutôt qu'une table de valeurs Q(s,a).

**A faire (pour le 17-03-2025)**

* Corriger TME1 si nécessaire, à remettre   
* TME2 \- implémenter SARSA et Q-learning (et TME3 selon l’avancée), à remettre  
* Se familiariser avec le SAC

