# ML-Workflow-Orchestration-With-Prefect

Démarrer le serveur Prefect (dans un terminal séparé):
prefect server start

Dans un nouveau terminal PowerShell :
# Définir l'URL de l'API
$env:PREFECT_API_URL="http://127.0.0.1:4200/api"

# Vérifier que le serveur est accessible
curl http://127.0.0.1:4200/api/health

# Démarrer le worker
prefect worker start --pool DC-work-pool --type process

Votre déploiement Prefect a été créé avec succès
Démarrer le worker (dans un nouveau terminal) :
# 1. Définir l'URL de l'API
$env:PREFECT_API_URL="http://127.0.0.1:4200/api"

# 2. Démarrer le worker pour le pool
prefect worker start --pool "DC-work-pool" --type process

Lancer une exécution manuelle :
prefect deployment run 'ml-workflow/first-prefect-deployment'