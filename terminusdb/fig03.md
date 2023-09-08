# Figure 3: Map of an informational landscape

```mermaid
%%{init: {"theme": "neutral"} }%%
flowchart LR

Gender ---|Categorize| Pet
Size ---|Group| Pet
Color ---|Describe| Pet

Pet ---|Belong to| Breed
Pet ---|Be given| Vaccination
Pet ---|Take| Image

subgraph Pet
    direction LR
    Dog
    Cat
    Bird
end
```