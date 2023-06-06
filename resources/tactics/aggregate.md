# Aggregate


## Invariant (Business Rules/Invariant) vs Règle de gestion

La validation est le processus d'approbation d'un état donné de l'objet. 
Tandis que l'invariant se produit avant même que cet état ait été atteint.

Un corollaire est que l'application des invariants est mieux réalisée par l'objet qui est muté (ou créé) lui-même, comme un réflexe d'autoprotection, alors que la validation est généralement réalisée par une tierce partie.

L'école de pensée "Always valid" préconise l'utilisation d'invariants plutôt que la validation. Cela s'accorde parfaitement avec DDD et les agrégats.

## 4 règles de base

### 1st rule of thumb: Model true invariants as consistency boundaries.

True invariants are those business rules that are speaking of transactional consistency.

Example: Video Game, Two Fighters, Fighter life point 0 and later die. IT's NOT TRUE INVARIANT. If Fighter life point go to 0, he die immediatly. THAT's TRUE INVARIANT.

### 2nd Design small aggregate
https://www.informit.com/articles/article.aspx?p=2020371&seqNum=3

### 3rd : Reference other aggregate by identity only

### 4th: Update other aggregate using eventual consitency


## Aggregate Canvas (by Yoan Thirion)

![aggregate_canvas](https://github.com/tanguybernard/my-awsome-ddd/assets/14818169/089d1301-6561-4d8e-81a3-5329938a4d29)


source https://speakerdeck.com/thirion/ddd-re-distilled
