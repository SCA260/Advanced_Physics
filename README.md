# Advanced_Physics
Three Games using Unreal Engine Chaos Physics

**Level 1: Projet Pachinko**
 
<img width="896" height="492" alt="Capture d’écran 2026-02-11 151654" src="https://github.com/user-attachments/assets/aa4f1007-571a-499e-b34d-e46bd616461a" />

  
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

**Choix Techniques**
- GameMode centralisé: 
	- Agit comme le cerveau de la partie
	- Stocke le score et les variables
- Systeme de spawner:
	- limites de balles
- UI
	- Affichage du score
	- DataBinding

**Problèmes rencontrés**
- Rebonds de la balle sur l'axe Z

Solution: décomposer le vecteur et ajouter l'impulsion uniquement sur X et Y, laisser Z à 0.
- Conflits Souris/Cameras
On ne pouvais pas cliquer sur le bouton "play again" et après on ne récupérait pas l'input du joueur

Solution: ajouter "Set Input Mode UI Only" et "Set Input Mode Game Only"

-
**Level 2: Projet Wrecking Ball**

<img width="716" height="400" alt="Capture d’écran 2026-02-11 151056" src="https://github.com/user-attachments/assets/80207352-0754-434c-88f2-24f0679ec6be" />

Le joueur controlle une Grue ( touches Q et D ) avec une Boule de démolition pour détruire des structures et marqués des points dans un temps imparti.

**Mécaniques physiques**
- Simulation physiques et gravités: configuration avec "Simulates Physics"
- Contraintes Physiques: relie la boule et la grue avec un cable et permet d'obtenir un balancement réaliste.
- Gestion de la masse: permet d'ajuster la masse pour qu'il y ait assez d'énergie cinétique.
- Collisions : Configuration des Collision Presets sur "PhysicsActor" pour que les cubes s'effondrent dynamiquement lors de l'impact.

**Choix Techniques**
- Scoring: une TriggerBox detecte les cubes qui tombent à l'aide d'un tag
- Timer/Gestion du temps
- Victoire/défaite

**Problèmes rencontrés**
- communication entre les blueprints: Target is self
Solution: Variable de référence.



