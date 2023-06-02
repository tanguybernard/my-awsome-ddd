# Event Storming

Repris de cette article: 

https://jordanchapuy.com/posts/2021/10/une-introduction-a-levent-storming/


## Introduction


L'objectif est de cartographier la connaissance.

Les signes pour déclencher un event storming: on a trop de bugs, on a des zones de floues, on veut s’aligner avec un existant, on veut cartographier de la connaissance.


## Les éléments


## Events

Les événements sont décrits par un verbe au participe passé. « Facture générée », « Commande livrée ». 
C’est quelque chose qui a eu lieu. C’est très important. On veut forcer les participants à penser avec des actions achevées, des changements d’état, des choses qui peuvent agir comme un déclencheur pour une autre action.

### Commands

C’est ce qui déclenche un événement, souvent une conséquence d’une action utilisateur, une prise de décision, ou d’un système externe.

On peut trouver que la commande et l’événement sont redondants. Avec la commande, on parle de l’action réalisée par un acteur, qui sera le déclencheur d’un ou plusieurs événements. Il n’y a pas forcément une commande sur chaque événement. 
Avec les commandes, on se projette également un peu dans le code (use case).

### Policy

Une Policy permet de rendre explicite une règle métier. C’est la glu qui lie un événement et une commande. Avec une Policy, on représente des commandes qui sont exécutées suite à un événement et selon une condition précise. En général, on décrit une Policy avec Lorsque ... alors ... : « Lorsque le paiement dépasse 500 €, alors il faut envoyer un SMS à l’utilisateur ».

### Read Model

On va parler des données que l’on affiche et/ou qui vont aider les acteurs à prendre des décisions. 


### Aggregate

Les agrégats vont apporter une vision bien plus micro et être très proche du code. Pour paraphraser Martin Fowler, un agrégat est un regroupement d’objets du domaine qui peuvent être manipulés comme un seul objet. 

Ce regroupement a du sens pour le métier. On préfèrera manipuler l’agrégat plutôt que chaque objets individuellement - ces objets sont cohérents s’ils sont manipulés ensemble. Dans l’exemple du e-commerce, on peut imaginer un agrégat « Panier » qui contiendrait plusieurs objets « Article » et un objet « Promotion ».

L’intérêt en faisant émerger les agrégats avant de se plonger dans le code va être de visualiser où ils se retrouvent, s’il n’y a pas trop d’événements ou commandes autour d’un même agrégat.

## Le rendu

On obtient de la visibilité. L’ensemble du processus, du système est rendu visible.

On obtient de la compréhension. On peut avoir des prises de conscience comme “je ne pensais pas que je te créais des problèmes là-bas en faisant ça” ou “je ne savais pas que tu faisais ceci”. Les participants comprennent ce qu’il se passe chez eux et chez les autres, on casse les silos. On espere améliorer la collaboration.

On obtient de l’alignement. On s’est mis d’accord tous ensemble sur le modèle, sur les problèmes. Continuons d’avancer ensemble.


## La suite

La suite est très modulable, tout comme l’est l’atelier. On peut imaginer un tas de choses pour travailler sur le processus :

- Voter pour le problème principal, qui pourrait devenir la priorité numéro une.
- Mettre en lumière les zones à améliorer, et travailler dessus avec le temps.
- Identifier où il peut manquer des compétences.
- Regarder le niveau de qualité dans les zones les plus importantes pour le métier.
- Travailler sur les dépendances et goulots d’étranglement.
- Simplifier le processus.


## Comparaison

### User story mapping

Le user story mapping est une méthode de visualisation des fonctionnalités, cartographiées selon les étapes clés du parcours utilisateur. En quelque sorte, c’est une autre manière de représenter son backlog et ses user stories. 

Très concrètement, il s’agit d’une grille de user stories, toutes disposées sous des étapes chronologiques dont l’enchaînement illustre l’expérience des utilisateurs avec votre produit.

Event Storming est plus haut niveau.

Ave le User Story Mapping, on se concentre sur l'affinement du backlog afin de fournir un produit fonctionnel à l'utilisateur.

https://www.followtribes.io/user-story-mapping/

https://www.easyagile.com/blog/the-ultimate-guide-to-user-story-maps/#:~:text=User%20story%20mapping%20vs%20event%20storming&text=Unlike%20user%20story%20mapping%2C%20which,in%20the%20product%20planning%20process.

Credits:

https://jordanchapuy.com/posts/2021/10/une-introduction-a-levent-storming/

https://blog.ippon.fr/2020/02/19/un-event-storming-avec-alberto-brandolini/
