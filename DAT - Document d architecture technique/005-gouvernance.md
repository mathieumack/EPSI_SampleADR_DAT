<!-- Title: Gouvernance des ressources -->
<!-- Parent: DAT - Document d'architecture technique -->

<!-- Macro: \!\[.*\]\((.+)\)\<\!\-\- width=(.*) \-\-\>
     Template: ac:image
     Attachment: ${1}
     Width: ${2} -->

# Gouvernance

<!-- Include: ac:toc -->

## Contexte
Chaque ressource dans le CDH doit respecter des règles de nommage ainsi qu'un ensemble de tags qui permettront de filtrer et d'organiser les ressources.

## Règles de nommage
### Règles de nommage pour les ressources Azure
Ces règles complètent la documentation générale disponible [ici](lien vers la doc interne).

Les ressources Azure doivent respecter les règles suivantes:

| Type de ressource | Code |
|-------------------|------------------|
| Resource Group | rg |
| Virtual Network | vnet |
| Subnet | subnet |
| Network Security Group | nsg |
| Api management | apim |
| Azure Container Apps | acs |
| Azure Container Registry | acr |
| Azure Front Door | fd |
| Azure SQL Database | sql |
| Azure storage account | stg |
| Azure Key Vault | kv |

## Tags
Les tags sont des paires clé/valeur qui permettent d'organiser les ressources Azure. Ils sont utilisés pour filtrer les ressources dans le portail Azure, mais aussi dans les scripts PowerShell.

### Tags pour les ressources Azure
Les tags pour les ressources Azure sont les suivants:

| Nom du tag | Valeur |
|------------|--------|
| Project | nom du projet |
| AppName | nom de l'application |
| Environnement | nom de l'environnement |
| Owner | nom du propriétaire |
