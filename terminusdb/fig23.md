# Figure 23

Relational BTM.

```mermaid
%%{init: {"theme": "neutral"} }%%
erDiagram
Customer }|--o{ Account : Own
"Account Balance" }o--|| Account : Contain
```