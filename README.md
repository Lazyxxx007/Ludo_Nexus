# LUDO NEXUS — Prototype v0.1

Prototype local du jeu de plateau cyberpunk LUDO NEXUS.

## Lancer le jeu

1. Télécharge ou décompresse le dossier.
2. Ouvre `index.html` dans Chrome, Edge ou Firefox.
3. Clique sur **Lancer le dé**.
4. Les pions lumineux sont sélectionnables lorsque leur déplacement est valide.
5. Clique sur **Nouvelle partie** pour recommencer.

Aucune installation, dépendance ou connexion Internet n'est nécessaire.

## Ce que contient cette version

- Interface cyberpunk responsive.
- Plateau circulaire avec quatre factions.
- Dé interactif.
- Déploiement sur un 6.
- Déplacements, captures simples et bonus de lancer sur un 6.
- Journal des événements.
- Nouvelle partie.

## Limites connues de la V0.1

C'est un prototype visuel et fonctionnel, pas encore un Ludo complet :
- Il n'y a pas encore de voie finale propre à chaque faction ; la progression et la victoire restent volontairement simplifiées.
- Le mode local est une simulation de tours entre quatre factions, pas un multijoueur réseau.
- Les règles sont simplifiées et le code JavaScript est encore directement intégré à la page.
- Les captures et les cases de sécurité devront être revérifiées lors de la création du moteur de règles officiel.
- Il n'y a pas encore de comptes, de base de données ou d'IA.

Ces limites sont intentionnelles : la prochaine version doit être construite avec tes retours.

## Prochaines étapes possibles

1. Séparer HTML, CSS et JavaScript dans des fichiers distincts.
2. Formaliser le parcours et les règles du Ludo.
3. Créer un moteur de règles indépendant et des tests automatisés.
4. Ajouter une vraie voie d'arrivée et une condition de victoire.
5. Ajouter une IA.
6. Ajouter le multijoueur en ligne.

## Git et GitHub

Voir `GIT_GUIDE.md` pour les commandes de base et la publication du dépôt.
