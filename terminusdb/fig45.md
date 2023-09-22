# Figure 45

Nested arrays added for color and images.

```mermaid
%%{init: {"theme": "neutral"} }%%
flowchart TB

subgraph Pe["Pet Denormalized Full"]
pet_number["Pet Number"]
pet_name["Pet Name"]
pet_age_qty["Pet Age"]
gender_code["Gender Code"]
adoption_code["Adoption Code"]
subgraph Vaccinations
subgraph Vaccination
vcode["Vaccination Code"]
vname["Vaccination Name"]
end
end

subgraph Colors
subgraph Color
ccode["Color Code"]
cname["Color Name"]
ppco["Pet Primary Color Indicator"]
end
end

subgraph Images
subgraph Image
inum["Image Number"]
ipathname["Image Path Name"]
pfia["Pet Feature Image Indicator"]
end
end

end
```