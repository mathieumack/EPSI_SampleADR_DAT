<!-- Title: Networking -->
<!-- Parent: DAT - Document d'architecture technique -->

<!-- Macro: \!\[.*\]\((.+)\)\<\!\-\- width=(.*) \-\-\>
     Template: ac:image
     Attachment: ${1}
     Width: ${2} -->

# Networking

<!-- Include: ac:toc -->

## Contexte
## VNET
Chaque environnement est associé à un VNET.

Du peering est mis en place entre les VNETs des différents environnements et le Hub VNET connecté au réseau on-premise.

Liste des vnets et leurs configurations :

| VNET | CIDR | Description |
|------|------|-------------|
| Hub |   | VNET connecté au réseau on-premise |
| Dev | ********** | VNet dédié au VNet de DEV |
| Recette | ********** | VNet dédié au VNet de Recette |
| PréProd | ********** | VNet dédié au VNet de PréProd |
| Prod - West Europe | ********** | VNet dédié au VNet de Prod dans la région primaire |
| Prod - North Europe | ********** | VNet dédié au VNet de Prod dans la région secondaire |

## Subnets
Chaque VNET est composé de plusieurs subnets.
