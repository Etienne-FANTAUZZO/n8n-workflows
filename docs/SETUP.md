# Guide d'installation N8N

## Installation locale

### Docker (recommandé)

```bash
docker run -d -p 5678:5678 --name n8n n8nio/n8n
```

## Installation auto-hébergée sur Hostinger

### Prérequis
- VPS avec Node.js 18+
- PostgreSQL ou MySQL
- Accès SSH

### Étapes

1. Connectez-vous à votre VPS
2. Installez les dépendances
3. Clonez les workflows depuis ce repo
4. Configurez les credentials

## Accès à l'instance

- URL: http://localhost:5678 (local)
- URL: https://votre-domaine.com (production)

## Premiers pas

1. Créer un utilisateur admin
2. Importer les workflows
3. Configurer les credentials
4. Tester les workflows
