# Guide Git et GitHub — LUDO NEXUS

## 1. Installer et configurer Git

Installe Git pour Windows depuis https://git-scm.com/download/win, puis ouvre PowerShell dans le dossier `ludo-nexus-v1`.

Vérifie l'installation :

```powershell
git --version
```

Configure ton identité une seule fois sur ton ordinateur :

```powershell
git config --global user.name "Ton nom GitHub"
git config --global user.email "Ton adresse e-mail GitHub"
```

Utilise l'adresse associée à ton compte GitHub, ou l'adresse `noreply` proposée par GitHub si tu préfères ne pas afficher ton adresse personnelle dans les commits publics.

## 2. Initialiser le dépôt local

Depuis le dossier du projet :

```powershell
git init
git add .
git commit -m "feat: create Ludo Nexus v0.1 prototype"
git branch -M main
```

- `git init` crée le dépôt local.
- `git add .` prépare les fichiers.
- `git commit` enregistre un instantané.
- `git branch -M main` nomme la branche principale `main`.

## 3. Créer le dépôt GitHub

1. Connecte-toi sur https://github.com.
2. Clique sur **New repository**.
3. Nom : `ludo-nexus`.
4. Ajoute une description, par exemple : `Cyberpunk-inspired Ludo game prototype built with HTML, CSS and JavaScript`.
5. Choisis Public si tu veux l'afficher dans ton portfolio.
6. Pour éviter les conflits au premier push, ne demande pas à GitHub de créer un README ou un `.gitignore` : ils sont déjà présents localement.
7. Crée le dépôt.

GitHub affichera l'URL du dépôt. Copie-la et exécute, en remplaçant l'exemple par ton URL :

```powershell
git remote add origin https://github.com/TON-PSEUDO/ludo-nexus.git
git push -u origin main
```

Si GitHub demande une authentification, suis le flux proposé dans le navigateur ou utilise GitHub CLI. N'inscris jamais un mot de passe ou un jeton directement dans un fichier du projet.

## 4. Ton cycle de travail pour chaque modification

Après avoir modifié et testé le jeu :

```powershell
git status
git diff
git add .
git commit -m "feat: improve board interactions"
git push
```

Choisis des messages précis. Exemples :

```text
feat: add faction selection
fix: correct pawn movement validation
style: improve mobile board layout
test: add movement rule tests
docs: update setup instructions
refactor: extract game engine
```

Un commit doit idéalement correspondre à une modification cohérente. N'attends pas la fin de tout le projet pour faire ton premier commit.

## 5. Travailler sur une nouvelle fonctionnalité

Pour développer une fonctionnalité sans risquer de casser `main` :

```powershell
git switch -c feat/game-rules-engine
```

Quand elle est testée :

```powershell
git add .
git commit -m "feat: implement game rules engine"
git push -u origin feat/game-rules-engine
```

Tu pourras ensuite ouvrir une Pull Request sur GitHub, examiner les changements, puis fusionner la branche dans `main`.

## 6. Héberger la version web avec GitHub Pages

Pour ce prototype statique :
1. Ouvre le dépôt GitHub.
2. Va dans **Settings → Pages**.
3. Sélectionne le déploiement depuis une branche.
4. Choisis `main` et le dossier `/ (root)`.
5. Enregistre et attends la publication.

Le fichier `index.html` doit être à la racine publiée. GitHub Pages peut héberger le frontend statique, mais pas un backend Python/FastAPI persistant ou une base PostgreSQL.

## 7. Bonnes pratiques pour le portfolio

- Ajoute une description claire et des captures d'écran au README.
- Documente les règles et les limites connues.
- Publie des commits réguliers et compréhensibles.
- Ajoute les étapes de lancement et les tests.
- Ne pousse jamais des mots de passe, clés API, fichiers `.env` ou données personnelles.
- Ne prétends pas qu'une fonctionnalité est terminée si elle ne l'est pas.
- Présente le projet comme un prototype évolutif et décris honnêtement les versions.

## 8. Commandes utiles

```powershell
git status
git log --oneline
git diff
git diff --staged
git branch
git switch main
git pull
```

Avant de commencer une session, vérifie `git status`. Avant de pousser, vérifie ce que tu as modifié et teste le jeu.
