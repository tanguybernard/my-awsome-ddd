# Aggregate

## Definition

Un agrégat est une collection d'objets du domaine qui forment une frontière cohérente.

## Invriant

### True Invariants

Les vrais invariants sont les règles de gestion qui parlent de cohérence transactionnelle. En d'autres termes, une règle qui n'a pas de sens d'être "vérifiée" plus tard. Cette "vérification" ou validation doit avoir lieu au moment où une opération est tentée.

## Invariant (Business Rules/Invariant) vs Règle de gestion

La validation est le processus d'approbation d'un état donné de l'objet. 
Tandis que l'invariant se produit avant même que cet état ait été atteint.

Un corollaire est que l'application des invariants est mieux réalisée par l'objet qui est muté (ou créé) lui-même, comme un réflexe d'autoprotection, alors que la validation est généralement réalisée par une tierce partie.

L'école de pensée "Always valid" préconise l'utilisation d'invariants plutôt que la validation. Cela s'accorde parfaitement avec DDD et les agrégats.


## Invariants vs Corrective Policies

Invariants et politiques correctives

Une règle de gestion invariante est une règle qui s'appliquera toujours, quelle que soit la manière dont nous essayons d'agir dans notre système. Un exemple pourrait être un système de carte de crédit dans lequel nous nous assurons qu'un client ne peut pas dépasser la limite de sa carte de crédit. Dans la réalité, il n'est généralement pas possible d'appliquer cette règle dans 100 % des cas. Il est plausible de dire que certaines transactions seront traitées hors ligne (par exemple, dans l'avion ou dans des endroits où la connectivité est mauvaise).



Dans ce cas, une politique corrective permet de s'assurer que le système sait comment réagir en cas de violation de la règle de gestion. Un exemple pourrait être une politique de surutilisation, qui facturerait des intérêts supplémentaires en plus des intérêts normaux. Ce n'est qu'un exemple parmi d'autres où les concepteurs de logiciels ont besoin de l'avis d'experts du domaine pour décider de la manière de gérer la violation des règles de gestion.


## 4 règles de base (rules of thumb)

### Modéliser les vrais invariants comme des limites de cohérence.

True invariants are those business rules that are speaking of transactional consistency.

Example: Video Game, Two Fighters, Fighter life point 0 and later die. IT's NOT TRUE INVARIANT. If Fighter life point go to 0, he die immediatly. THAT's TRUE INVARIANT.

### Design small aggregate

https://www.informit.com/articles/article.aspx?p=2020371&seqNum=3

### Reference other aggregate by identity only

### Update other aggregate using eventual consitency

Nous traitons chaque agrégat séparément. La cohérence éventuelle signifie qu'à un moment donné, notre système sera dans un état incohérent, mais qu'après un certain temps, il sera cohérent.


## Aggregate Canvas (by Yoan Thirion)

![aggregate_canvas](https://github.com/tanguybernard/my-awsome-ddd/assets/14818169/089d1301-6561-4d8e-81a3-5329938a4d29)


source https://speakerdeck.com/thirion/ddd-re-distilled


## Credits

https://domaincentric.net/blog/modelling-business-rules-invariants-vs-corrective-policies

https://dev.to/jamesmh/what-are-aggregates-in-domain-driven-design-16nh

https://www.kamilgrzybek.com/blog/posts/processing-multiple-aggregates-transactional-vs-eventual-consistency



