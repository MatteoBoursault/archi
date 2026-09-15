# archi

Ce depot contient l'ensemble de mes idees et developpement concernant l'architecture logiciel.

## definition des principes d'architecture

### solid

#### Responsabilité unique (Single responsibility principle)

une classe, une fonction ou une méthode doit avoir une et une seule unique raison d'être (d'evoluer). Cela favorise la modularité et facilite la maintenance en évitant les classes surchargées de responsabilités.

=> definir explicitement la raison d'etre de chaque classe et de chaque methode dans un equivalent a doxygen (ADU formalisme)
=> verifier l'atomicite de ces definitions via llm (et/ou analyse syntaxique/logique)
=> generer les TU a partir de ces definitions

#### Ouvert/fermé (Open/closed principle)

une entité applicative (classe, fonction, module ...) doit être fermée à la modification directe mais ouverte à l'extension. L'objectif est de permettre l'ajout de nouvelles fonctionnalités sans altérer le code existant.

=> githook pour verification du respect de cette regle

#### Substitution de Liskov (Liskov substitution principle)

une instance de type T doit pouvoir être remplacée par une instance de type G, tel que G sous-type de T, sans que cela ne modifie la cohérence du programme. Cela garantit que les sous-classes peuvent être utilisées de manière interchangeable avec leurs classes de base.

#### Ségrégation des interfaces (Interface segregation principle)

préférer plusieurs interfaces spécifiques pour chaque client plutôt qu'une seule interface générale. Cela évite aux classes de dépendre de méthodes dont elles n'ont pas besoin, réduisant ainsi les couplages inutiles.

#### Inversion des dépendances (Dependency inversion principle)

il faut dépendre des abstractions, pas des implémentations. Cela favorise la modularité, la flexibilité et la réutilisabilité en réduisant les dépendances directes entre les modules.

