<!-- Title: Network -->
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

# Network

<!-- Include: ac:toc -->

## Statut
Statut: Acceptée

## Contexte
Certaines données et services internes sont déployés sur un réseau on-premise. La solution doit donc être en mesure de communiquer avec ces services.
Un lien réseau sécurisé doit être créé entre le réseau on-premise et le réseau Azure.

## Décisions
Une connection VPN Gateway sera créée entre le réseau on-premise et le réseau Azure.

## Conséquences

## Notes
### VNet peering
Le peering de VNET est une connexion entre 2 VNETs dans la même région. Il est possible de faire du peering entre VNETs dans des régions différentes mais il faut passer par un service de transit (Azure backbone network).
Pour plus d'informations, voir [VNet peering](https://docs.microsoft.com/en-us/azure/virtual-network/virtual-network-peering-overview).