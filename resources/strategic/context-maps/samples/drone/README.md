# Context Map - Reflexion



## UserAccounts ->Shipping (Mutualy dependent) - Partnership - OHS - ACL

Si tu veux expedier un colis
Tu dois transmettre le lieu de depart et d'arriver, le poids..

## Shipping -> UserAccounts (Mutualy dependent) - PArtnership - OHS - ACL

Si tu veux connaitre l'ETA, etre prevenu de l'arrivé du drone
Je dois avoir ton mail, un sms

Si tu veux avoir une remise je dois savoir combien d'expedition tu as passé.

## Shipping -> Drone Management (U/D)

Le shipping a besoin de savoir si un drone est disponible
Le shipping a besoin de savoir si le drone est bien revenu...
Le shipping a besoin de planifier un vol, le drone choisi doit avoir la capacité de transport suffisant.

## Shipping -> Invoice ()

Le shipping va pousser les infos à l'invoice pour qu'il genere la facture pour le consumer

## Invoice -> User Account

L'invoice va envoyer la facture au user


## Done Management <-> Drone Sharing ?

Le drone management est le sharing, partage peut etre la meme base ?

Juste à savoir si il est loué ou expédié.

Les caractèreistiques du drone sont les memes: hélices, autonomie, charge utile... ?

Donc modèle partager ? donc shared-kernel


Solution : Ne partage pas forcément la meme base.

La location de drone va requisitionner le drone dans la base de Management et le rendre plus tard.

Drone Sharing  est Dowstream il consomme de Drone Management (Upstream)

Drone Sharing pourrait d'ailleurs etre conformiste car le modele du drone n'a pas besoin de changer dans le cas d'une location.
Si conformist alors pas d'acl.





