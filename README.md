# n8n-workflows

Sauvegarde et documentation des workflows N8N - Automation, RPA et intégrations API

## 📋 Table des matières

- [À propos](#à-propos)
- [Structure du projet](#structure-du-projet)
- [Installation](#installation)
- [Guide d'utilisation](#guide-dutilisation)
- [Export et import de workflows](#export-et-import-de-workflows)
- [Dépannage](#dépannage)

## À propos

Ce dépôt centralise l'ensemble des workflows N8N créés pour :
- Automatisation des processus métier (RPA)
- Intégrations d'API B2B et B2C
- Webhooks et déclencheurs externes
- Workflows de données et ETL
- Intégrations AI (Gemini, Claude, LangChain)

## Structure du projet

```
n8n-workflows/
├── README.md                          # Ce fichier
├── .gitignore                         # Ignorer les fichiers sensibles
├── docs/                              # Documentation
│   ├── SETUP.md                      # Guide d'installation
│   ├── EXPORT_IMPORT.md              # Guide export/import
│   └── API_KEYS.md                   # Gestion des clés API
├── workflows/                         # Workflows principaux
│   ├── sales/                        # Workflows ventes
│   ├── automation/                   # RPA et automatisation
│   ├── integration/                  # Intégrations API
│   ├── data/                         # ETL et données
│   └── ai/                           # Workflows IA
└── configs/                           # Configurations N8N
    ├── credentials.example.json      # Modèle de credentials
    └── settings.json                 # Paramètres N8N
```

## Installation

### Prérequis
- N8N installé localement ou auto-hébergé
- Accès à votre instance N8N
- Les credentials pour les services externes

### Cloner le dépôt

```bash
git clone https://github.com/Etienne-FANTAUZZO/n8n-workflows.git
cd n8n-workflows
```

## Guide d'utilisation

### Accéder à N8N
```
http://localhost:5678  # Instance locale
OU
https://your-n8n-instance.com  # Instance auto-hébergée
```

### Importer un workflow

1. Ouvrir N8N
2. Cliquer sur **Workflows**
3. Cliquer sur **Import workflow**
4. Sélectionner le fichier JSON du workflow
5. Configurer les credentials manquants
6. Tester et activer le workflow

## Export et import de workflows

### Exporter depuis N8N

1. Ouvrir le workflow
2. Menu **⋮** → **Download**
3. Le fichier JSON est téléchargé
4. Placer le fichier dans le dossier approprié (`workflows/category/`)
5. Faire un commit : `git add` → `git commit` → `git push`

### Importer dans N8N

1. Dans N8N : **Import from File**
2. Sélectionner le fichier JSON du dépôt
3. Mettre à jour les **credentials** si nécessaire
4. Tester le workflow

### En ligne de commande (optionnel)

```bash
# Avec n8n-cli (si installé)
n8n import:workflow --input=workflows/category/workflow-name.json
```

## Configuration des credentials

⚠️ **Sécurité** : Les credentials ne doivent JAMAIS être commités sur GitHub

### Fichier .gitignore
Les fichiers suivants sont ignorés :
- `node_modules/`
- `.env`
- `*.credentials.json`
- `credentials/`

### Ajouter des credentials localement

1. Dans N8N : **Settings** → **Credentials**
2. Créer/mettre à jour les credentials
3. Les credentials sont stockés dans la base de données N8N locale

## Workflows disponibles

### Sales (Ventes)
- Lead automation
- B2B prospecting
- CRM integration

### Automation (RPA)
- Process automation
- Email workflows
- Data processing

### Integration (API)
- Webhook receivers
- Third-party syncs
- API aggregation

### Data (ETL)
- Data transformation
- Database operations
- Data validation

### AI (Intelligence artificielle)
- Gemini integration
- Claude integration
- LangChain chains

## Dépannage

### Workflow ne s'exécute pas
1. Vérifier les **credentials**
2. Consulter les **logs** d'exécution
3. Valider les **mappings** de données
4. Tester avec un trigger manuel

### Erreur de credentials
1. Vérifier la validité des clés API
2. Vérifier les permissions/scopes
3. Renouveler le token si expiré

### Problèmes de connexion
1. Vérifier la URL de l'instance N8N
2. Vérifier l'accès réseau
3. Consulter les logs du serveur N8N

## Contribution

Pour ajouter un nouveau workflow :
1. Créer une branche : `git checkout -b feature/workflow-name`
2. Ajouter le workflow JSON dans `workflows/category/`
3. Créer/mettre à jour la documentation
4. Faire un pull request

## License

Privé - Propriété personnelle

## Support

Pour toute question sur N8N :
- [Documentation N8N](https://docs.n8n.io)
- [Community N8N](https://community.n8n.io)

---

**Dernière mise à jour** : Janvier 2026
**Version N8N** : À vérifier dans votre instance
