<!-- Title: FQDN -->
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
    
# FQDN

<!-- Include: ac:toc -->

## Statut
Statut: Acceptée . 

## Contexte
Chaque service dans l'architecture a son propre nom de domaine et tous les flux réseaux doivent être sécurisés en passant par des appels HTTPS.

## Décisions
Seuls les services exposés publiquement (internet) doivent avoir un nom de domaine customisé. Les services internes ne doivent pas avoir de nom de domaine customisés et doivent être accessibles uniquement par leur noms de domaines internes Azure.

## Arguments
- La gestion du noms de domaine et du certificat SSL est complexe et coûteuse. Il est donc préférable d'avoir à gérer cela à un seul endroit (Front Door).

## Conséquences

## Notes
### Azure KeyVault
Le certificat SSL doit être stocké dans Azure KeyVault. Il faut donc créer un KeyVault par environnement. Le certificat doit être stocké dans le KeyVault en mode "Certificat". Seul le service Azure Front Door via son identité managée doit avoir les droits de lecture sur le certificat.