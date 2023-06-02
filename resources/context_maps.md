# Context Maps



## OHS (Open Host Service)

L'OHS est un protocole qui permet à un système en aval de s'intégrer avec nous - un système en amont. 
Il peut s'agir d'une API REST, d'une façade, d'un accès à un bus CQRS, de SOAP, etc.

Le mieux est de considérer ce type d'intégration comme un contrôleur Http ou une API REST. Il s'agit d'un point d'entrée dans notre système.

Imaginons qu'une partie de votre système soit une passerelle de paiement. Comment l'intégrer ? 
Peut-être en interrogeant la base de données ou en utilisant le code de l'application comme les services ou les entités ? 
Cela ressemble à un désastre... Bien sûr, nous devrions définir un protocole pour accéder à la passerelle. 

C'est comme si quelqu'un vous demandait quelque chose et que vous lui donniez la possibilité de le faire d'une certaine manière et selon vos règles.

Un  hote ouvert OH(S) ou context ouvert est un __contexte délimité__ qui fournit une API bien conçue, axée sur le domaine, destinée à être utilisée par de nombreux consommateurs et non adaptée à un consommateur spécifique.
