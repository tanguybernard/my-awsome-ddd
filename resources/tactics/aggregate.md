# Aggregate


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
