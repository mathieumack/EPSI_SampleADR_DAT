<!-- Title: API Manager -->
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
    
# API Manager

<!-- Include: ac:toc -->

## Statut
Statut: Proposée .

## Contexte
Le service d'API management doit permettre d'exposer des APIs en internes et aux externes (partenaires). Le service doit héberger les APIs, inclure des règles de traitement (policies), collecter et analyser les usages et fournir un portail développeur pour permettre aux consommateurs de s'enregistrer et de gérer leurs accès aux APIs.

## Décisions

### Arguments
- C'est une solution complètement managée.
- Support de HTTP et HTTPs

## Questions ouvertes:
- Quel niveau de service utiliser ? Standard ou Premium ?

## Conséquences
Si le service tiers Standard est retenu, il faudra prendre en compte les éléments suivants :
- Le service étant ouvert à l'extérieur il n'est plus protégé directement par le Front Door.
- Un filtrage IP devra être mis en place pour limiter les accès aux APIs par le Front Door uniquement.

## Notes
### Azure API Management
Azure API Management est un service entièrement managé qui permet aux développeurs de publier des APIs aux consommateurs internes et externes. Le service héberge les APIs, applique des règles de traitement, collecte et analyse les statistiques d'utilisation et fournit des portails développeurs pour que les consommateurs s'enregistrent, découvrent et consomment les APIs.