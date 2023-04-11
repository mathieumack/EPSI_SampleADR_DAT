<!-- Title: API Hosting -->
<!-- Parent: Cadrage projet -->
<!-- Parent: New archi architecture decisions -->
<!-- Parent: Cloud solution -->

<!-- Macro: Statut: Proposée 
    Template: ac:status 
    Title: Proposée 
    Color: Blue -->

<!-- Macro: Statut: Acceptée 
    Template: ac:status 
    Title: Acceptée 
    Color: Green -->
    
# API Hosting

<!-- Include: ac:toc -->

## Statut

Statut: Acceptée .

## Contexte
Chaque backend doit être hébergé dans un service cloud. Le service doit être capable d'augmenter ou réduire ses resources en fonction de la charge. Le service doit être capable d'être déployé dans plusieurs environnements (dev, recette, pré-prod, prod).

## Décisions
Azure Container Apps est utilisé pour hébergés les backends (API).

### Arguments
- Azure Container Apps est un service managée
- Scale up & down automatiquement en fonction de règles

## Conséquences

## Notes
### Azure container Apps
Azure Container Apps permet de créer des microservices serverless basés sur des conteneurs.