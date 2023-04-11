<!-- Title: Droits et accès aux ressources -->
<!-- Parent: DAT - Document d'architecture technique -->

<!-- Macro: \!\[.*\]\((.+)\)\<\!\-\- width=(.*) \-\-\>
     Template: ac:image
     Attachment: ${1}
     Width: ${2} -->

# Groupes de sécurités

<!-- Include: ac:toc -->

## Contexte
Voici la liste des groupes de sécurité qui sont utilisés et qui auront des accès à la plateforme Azure.

| AAD Group | Description |
| -------- | -------- |
| ipaas_infra_adm | Groupe d'administrateurs qui auront un accès global aux ressources d'infrastructure (ex : réseau, AD 2c) afin d'en créer depuis le portail azure, et qui pourront aussi affecter des droits Azure RBAC |
| ipaas_infra_mgt | Groupe d'utilisateurs qui pourront modifier les ressources et leur configuration mais sans possibilité de modifier les droits Azure accès RBAC |
| ipaas_apps_mgt | Groupe d'utilisateurs qui pourront accéder aux ressources dédiées aux apps. |

Ces groupes de sécurité sont configurés au niveau des souscriptions ou ressource groups et associé à des rôles Azure afin de protéger les accès aux ressources.
