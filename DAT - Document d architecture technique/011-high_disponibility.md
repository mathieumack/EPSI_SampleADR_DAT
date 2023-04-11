<!-- Title: Haute disponibilité des services -->
<!-- Parent: DAT - Document d'architecture technique -->

<!-- Macro: \!\[.*\]\((.+)\)\<\!\-\- width=(.*) \-\-\>
     Template: ac:image
     Attachment: ${1}
     Width: ${2} -->

# Haute disponibilité

<!-- Include: ac:toc -->

## Contexte
La solution est configurée pour être hautement disponible. Cela consiste à avoir une redondance des services dans plusieurs régions afin de palier à une panne majeure d'une région Azure.

En cas de panne d'une région, les services basculeront automatiquement sur une seconde région.

Tous les services sont configurés pour être disponibles sur plusieurs régions en environnement de production. Les autres environnements ne sont pas redondés.

## Régions
La région primaire est la région `North Europe (Ireland)`. La région secondaire est la région `West Europe (Netherlands)`. Cette paire de région est celle qui offre la meilleure latence entre les deux régions et permet de réduire les coûts (North Europe étant généralement moins cher que West Europe).
