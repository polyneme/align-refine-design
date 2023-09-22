# Figure 20

Relational BTM.
Mermaid entity-relationship diagrams, unlike flowchart diagrams, do not support subgraphs.
Here, we copy-paste a Mermaid class diagram with inheritance arrows to designate our Pet subtypes.

```mermaid
%%{init: {"theme": "neutral"} }%%
classDiagram
  direction TB
  Pet <|.. Dog
  Pet <|.. Cat
  Pet <|.. Bird
```

See Figure 16.