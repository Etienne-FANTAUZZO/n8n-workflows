# Guide Export/Import des Workflows N8N

## Export depuis N8N

### Méthode UI

1. Ouvrir le workflow
2. Cliquer sur **Menu** (⋮)
3. Sélectionner **Download**
4. Le fichier JSON est téléchargé

### Structure du fichier export

Le fichier export contient :
- La configuration du workflow
- Les nodes et leurs paramètres
- Les connexions entre nodes
- Les triggers

## Import dans N8N

### Méthode UI

1. Cliquer sur **Workflows**
2. Cliquer sur **Import from File**
3. Sélectionner le fichier JSON
4. Configurer les credentials
5. Sauvegarder

### Vérification post-import

- Vérifier que tous les credentials sont configurés
- Tester le workflow avec un run manuel
- Vérifier les logs d'exécution

## Bonnes pratiques

- Nommer les workflows de manière explicite
- Ajouter une description dans le workflow
- Vérifier les versions de N8N compatibles
- Sauvegarder régulièrement sur GitHub
