# Figure 16

A business terms model for our animal shelter.
Mermaid entity-relationship (ER) diagrams, unlike flowchart diagrams, do not support subgraphs.
Here, we use ER diagram attributes to designate our Pet subtypes.


```mermaid
%%{init: {"theme": "neutral"} }%%
erDiagram
    Gender ||--o{ Pet : Categorize
    Size ||--o{ Pet : Group
    Color ||--o{ Pet : Describe

    Pet }o--|{ Breed : "Belong to"
    Pet }o--o{ Vaccination : "Be given"
    Pet }|--|{ Image : Take

    Pet {
        subtype Dog
        subtype Cat 
        subtype Bird
    }
```