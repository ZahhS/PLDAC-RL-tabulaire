PLDAC RL Tabulaire \- Bilan post RDV 21-03-2025



**Sujets abordés durant la réunion**

* Correction du passage des paramètres à la fonction de plot pour Actor-critic (TME3)
* Justification du terme (1-terminated) dans le calcul de delta (TME3)
* Discussion des hyperparamètres et tests statistiques (TME3)
* Introduction de Q-tables pour, aussi bien le critic que l'actor (cf. à faire)
* Plus tard : Quand est-ce que l'actor et le critic sont d'accord ? i.e. étude de quand l'action à la plus grande probabilité correspond à celle donnant la plus grande value (maximum de la q-value)


**A faire (pour le 28-03-2025)**

* Revoir TME3 - Actor-critic corrigé
* Implémenter les 4 fonctions suivantes pour l'algorithme Actor-critic :

1°: $Q(s_t, a_t) ← Q(s_t, a_t) + alpha-critic [r_{t+1} + \gamma Q(s_{t+1}, a_{t+1}) - Q(s_t, a_t)]$

2°: $Q(s_t, a_t) ← Q(s_t, a_t) + alpha-critic [r_{t+1} + \gamma max_a Q(s_{t+1}, a) - max_a Q(s_t, a)]$

3°: $Q(s_t, a_t) ← Q(s_t, a_t) + alpha-critic [r_{t+1} + \gamma max_a Q(s_{t+1}, a) - \Sigma_a \pi(a|s_t)  Q(s_t, a)]$

4°: $Q(s_t, a_t) ← Q(s_t, a_t) + alpha-critic [r_{t+1} + \gamma max_a Q(s_{t+1}, a) - Q(s_t, a_t)]$
