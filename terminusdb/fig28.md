# Figure 28

Strictly embedded logical model. Diagrammed as a Mermaid flowchart using subgraphs.

```mermaid
%%{init: {"theme": "neutral"} }%%
flowchart LR
subgraph Order
order_id
date
subgraph Customer
customer_id
name
address
end
subgraph OrderLines
subgraph OrderLine
line_id
quantity
subgraph Product
product_id
SKU_number
description
unit_price
end
end
end
end
```