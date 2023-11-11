# Eventual consistency

La cohérence éventuelle est une approche de conception visant à améliorer l'évolutivité et les performances, et les événements de domaine (Domain Events) peuvent contribuer à atteindre cet objectif en agissant comme un déclencheur transportant des informations de domaine

## CAP

Le théorème CAP dit qu'il est impossible sur un système informatique de calcul distribué de garantir en même temps (c'est-à-dire de manière synchrone) les trois contraintes suivantes:

- Cohérence (Consistency en anglais) : tous les nœuds du système voient exactement les mêmes données au même moment ;
- Disponibilité (Availability en anglais) : garantie que toutes les requêtes reçoivent une réponse ;
- Tolérance au partitionnement (Partition Tolerance en anglais) : aucune panne moins importante qu'une coupure totale du réseau
ne doit empêcher le système de répondre correctement (ou encore : en cas de morcellement en sous-réseaux,
chacun doit pouvoir fonctionner de manière autonome).


__L'Eventual Consistency__ opte pour la disponibilité et la tolérance de partitionnement, avec l'idée que la cohérence sera éventuellement atteinte après un certain temps.

https://blogs.oracle.com/developers/post/simplify-microservice-transactions-with-oracle-database-sagas
