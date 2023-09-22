# Figure 27

A query BTM.

```mermaid
%%{init: {"theme": "neutral"} }%%
erDiagram
Customer ||--o{ Order : creates
OrderLine }o--|| Order : "is made of"
OrderLine }o--|| Product : has
```