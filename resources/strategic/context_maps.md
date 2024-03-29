# Context Maps


# WORK IN PROGRESS

## Team Relasionships

### Mutualy Dependent

Livre ensemble pour que cela fonctionne.

### Upstream /Downstream

Le contexte en amont influence un contexte en aval.

### Free

Le changement dans un bounded contexte n'a pas d'influence sur d'autres.


## Context Map Patterns

### Partnership

The teams have a mutual dependency on each other for delivery.

### Shared Kernel


### Conformist

Dans cette relation, l'équipe en aval adopte le modèle et le langage omniprésent (ubiquitous language) de l'équipe en amont. 
Lorsqu'une passerelle de paiement a trois étapes et une structure de données spécifique, vous la faites de manière similaire ou de la même manière dans votre système.

Comme pour le partage d'un noyau, l'avantage de la conformité est de faciliter l'intégration en éliminant la complexité de la traduction entre des contextes limités, mais l'inconvénient est une fois de plus un couplage accru, puisque la dépendance vis-à-vis de l'amont est renforcée et que le système en aval est limité aux capacités du modèle en amont.

### OHS (Open Host Service) - Service hôte (hébergement) ouvert

L'équipe qui fournit un service d'hébergement ouvert (OHS) se trouve généralement en amont, tandis que les clients qui l'utilisent sont des équipes en aval. Il peut s'agir d'une API REST, d'une façade, d'un accès à un bus CQRS, de SOAP, etc.
Les équipes en aval sont libres d'être conformistes ou de construire des couches anti-corruption.

Le mieux est de considérer ce type d'intégration comme un contrôleur Http ou une API REST. Il s'agit d'un point d'entrée dans notre système.

Imaginons qu'une partie de votre système soit une passerelle de paiement. Comment l'intégrer ? 
Peut-être en interrogeant la base de données ou en utilisant le code de l'application comme les services ou les entités ? 
Cela ressemble à un désastre... Bien sûr, nous devrions définir un protocole pour accéder à la passerelle. 

C'est comme si quelqu'un vous demandait quelque chose et que vous lui donniez la possibilité de le faire d'une certaine manière et selon vos règles.

Un  hote ouvert OH(S) ou context ouvert est un __contexte délimité__ qui fournit une API bien conçue, axée sur le domaine, destinée à être utilisée par de nombreux consommateurs et non adaptée à un consommateur spécifique.

Pour éviter que les équipes en aval ne développent chacun un ACL, on peut exposer une version simplifiée du BC en amont en utilisant un langage publié (Published Language) via un service hôte ouvert (OHS).



### Published Language

Exemple : MathML, iCalendar




## Credits

https://speakerdeck.com/mploed/systems-thinking-by-combining-team-topologies-with-context-maps

https://patryktrochowski.com/context-mapping/

https://ilegra.com/blog/ddd-model-integrity-patterns/
