# Ordre du Jour - 11/04/2025

## 1. Amélioration des Critic Update Rules
- Ajustement des paramètres de stagnation :
  - Passage de `max_no_improve` de 5 à 10 pour permettre une détection plus souple de la stagnation.
- Amélioration de la stabilité de `make_mdp` via l’utilisation de `mdp.unwrapped`.

## 2. Ajout de tests statistiques et de comparaisons numériques
- `run_static_tests` : exécute plusieurs runs indépendants pour chaque règle de mise à jour du Critic.
- `compare_rewards_statistically` :
  - Application d’un t-test pour comparer les performances entre chaque paire de règles.
  - Affichage de la significativité statistique (p-value).
- `summarize_mean_rewards` :
  - Création d’un tableau récapitulatif avec moyenne et écart-type des récompenses pour chaque formule.

## 3. Ajout de visualisations spécifiques pour chaque formule
- `plot_reward_curves` :
  - Comparaison des courbes de récompenses moyennes sur les 4 règles.
- `plot_reward_curve_per_rule` :
  - Courbes individuelles des récompenses, règle par règle.
- `plot_step_curve_per_rule` :
  - Évolution du nombre moyen d’étapes par épisode.
- `plot_q_table_heatmaps` :
  - Affiche des heatmaps des Q-tables pour visualiser les apprentissages par règle.

## 4. Nouvelle métrique : Accord entre Actor et Critic
- `compare_actor_critic_agreement` :
  - Mesure le taux d’accord entre l’action préférée de l’Actor (politique) et celle du Critic (Q-table).
  - Utilise `np.where` pour gérer les égalités de score entre actions.
  - Résultats :
    - Affichage d’un tableau de correspondance.
    - Heatmap des accords par état.
    - Pourcentage global d’accord affiché dans le titre.

## 5. Meilleure organisation du code
- Utilisation cohérente de `OmegaConf` pour gérer tous les hyperparamètres.
- Séparation claire des fonctions de test :
  - `run_experiment` : pour les tests comparatifs globaux.
  - `run_static_tests` : pour les tests plus fins avec visualisation par règle.
