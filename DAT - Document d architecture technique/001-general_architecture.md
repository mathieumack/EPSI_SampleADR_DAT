<!-- Title: Architecture générale -->
<!-- Parent: DAT - Document d'architecture technique -->

<!-- Macro: \!\[.*\]\((.+)\)\<\!\-\- width=(.*) \-\-\>
     Template: ac:image
     Attachment: ${1}
     Width: ${2} -->

# Architecture générale

<!-- Include: ac:toc -->

## Architecture
La solution est une solution de type PaaS qui permet de connecter des applications et des données entre elles. Elle permet de créer des flux de données entre les applications et les bases de données. Elle permet également de créer des API pour les applications qui ne disposent pas de service API:

La solution est déployée dans Azure et est accessible depuis l'extérieur tout en étant intégrée dans le réseau privé de l'entreprise.

## Organisation des ressources

Les groupes de ressources sont répartis comme suit :

| Ressource group | Objectif |
| --------------- | -------- |
| infra | Services partagés à tous les environnements. Front Door (WAF, ...), Azure AD b2c |
| infra-network | Contient la partie network contenant le Hub réseau connecté avec le on-premise. Le peering entre réseau virtuel permet à chaque environnement d'accéder au réseau on-premise |
| core | Services partagés à un environnement. API Management, Azure SQL, et l'environnement Azure Container Apps). Il s'agit de services qui sont inclus et déployés dans la landing zone |
| core-network | Réseau virtuels et subnets sur lesquels les services seront intégrés. Intégration aussi des network security groups pour le filtrage des accès |
| core-monitoring | Contient les services de monitoring liés à l'environnement. |
| app-x | Ressource group dédié à l'hébergement d'une API ou d'une Web App. Contient l'instance Conteneur Apps et les services liés (keyvault pour les secrets, storage pour du fichier, une base de données SQL) |
