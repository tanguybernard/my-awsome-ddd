# Hexa (ports & adapters), Onion et Clean Architecture.

## Hexa (Alistair Cockburn)

https://alistair.cockburn.us/hexagonal-architecture/

- Ports & Adapters
- Application

*En comprenant l'architecture des ports et des adaptateurs, nous pouvons voir que les cas d'utilisation 
devraient généralement être écrits à la frontière de l'application (l'hexagone intérieur), pour spécifier les fonctions et les événements 
pris en charge par l'application, indépendamment de la technologie externe. - Alistair Cockburn*

## Onion (Jeffrey Palermo)

https://jeffreypalermo.com/2008/07/the-onion-architecture-part-1/


- User Interface et Infrastructure (cercle exterieur)
- Application Core
    - Application Services
    - Domain Services
    - Domain Model


## Clean (Robert C. Martin)

https://blog.cleancoder.com/uncle-bob/2012/08/13/the-clean-architecture.html

- Frameworks and Drivers (Database, the Web Framework)
- Interface Adapters (Presenters, Views, and Controllers)
- Use cases
- Entities
