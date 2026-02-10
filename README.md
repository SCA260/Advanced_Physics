# Advanced_Physics
Three Games using Unreal Engine Chaos Physics

**Level 1: Projet Pachinko**
 
  <img width="409" height="480" alt="image" src="https://github.com/user-attachments/assets/dd1fd590-4c7d-410b-a81b-d78daa9849d4" />

contrôles: barre d'espace.

Ce projet est une simulation du jeu d'arcade, de type Pachinko, l'objectif était de maitriser les interactions physiques, la gestion des collisions et la boucle de jeu, par des BluePrints.
**Mécaniques physiques**
Le gameplay repose sur le moteur Chaos Physics d'unreal:
- Matériaux Physiques: pour la restitution et la frictions (Frictions et rebonds). La configuration utilisée permet de Maximiser les rebonds et minimiser les frottements, afin d'obtenir un comportements réalistes et dynamiques.
- Impulsions: Ajout d'une force artificielle lors des collisions avec les colonnes, calcul de la direction du rebond basé sur la Normale de l'impact.
![Extrait_pachinko](https://github.com/user-attachments/assets/7e00ce0c-32fc-4831-bdad-354630009ff0)
- Zone de Triggers: ils servent à faire disparaitre les balles et à gérer les conditions de victoire ou défaites:
	- Malus: la balle tombe et disparait
	- Bonus: ajoute 100 points de scores
	- Bonus+ ajoute une balle supplémentaire


