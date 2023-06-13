# Patterns Tactiques



##


## Event sourcing

### Definition

L’event sourcing est un design pattern qui a lui pour but de ne plus baser ça source donnée sur un état complet d’un objet, mais sur les événements arrivés sur cette objet. Cela veut dire que notre source de vérité n’est plus l’objet en lui même, mais chacun des événements de son cycle de vie, stocké dans un “Event Store”. 

En partant de ce principe, il y a deux règles d’or : l’event store est “append only” et il est interdit d’altérer un event. Concernant la seconde règle, cela implique que si il y a une erreur il faudra un event de correction pour rectifier l’erreur.


### Drawback (Inconvénient) et Solution

L'état de l'application étant désormais codé sous la forme d'une série d'événements, il n'existe pas de moyen simple d'y accéder. Rejouer les événements chaque fois que nous avons besoin de récupérer l'état de l'application n'est pas une solution évolutive, car le nombre d'événements peut augmenter considérablement au fil du temps.

Il va falloir alors créer un système de dénormalisation. Cette couche de dénormalisation va intercepter un event, appliquer cette event sur l’état de d’objet concerner et le stocker dans une base de donner de lecture.

C'est pourquoi le pattern CQRS embrasse si bien l'Event Sourcing.






## Credits

Event sourcing


https://medium.com/swlh/event-sourcing-as-a-ddd-pattern-fea6de35fcca

https://medium.com/codeshake/cqrs-events-sourcing-avec-gcp-1-3-introduction-e5a62bbdae28


Hexagonal

https://vaadin.com/blog/ddd-part-3-domain-driven-design-and-the-hexagonal-architecture
