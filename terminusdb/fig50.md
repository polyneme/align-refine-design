# Figure 50

Our TerminusDB PDM.

```json
[
{
"@type": "@context",
"@base": "https://petadopt.example.org/data/",
"@schema": "https://petadopt.example.org/schema#"
},
{
"@type": "Enum",
"@id": "PetSize",
"@value": ["small", "medium", "large"]
},
{
"@type": "Enum",
"@id": "PetGender",
"@value": ["male", "female", "unknown"]
},
{
"@type": "Class",
"@abstract": [],
"@id": "Pet",
"pet_name": "xsd:string",
"pet_size": "PetSize",
"pet_gender": "PetGender",
"adopted": {
    "@class": "xsd:boolean",
    "@type": "Optional"
},
"vaccinations": {
    "@class": "Vaccination",
    "@type": "Set"
},
"pet_breed": {
    "@class": "PetBreed",
    "@type": "Cardinality",
    "@min_cardinality" : 1
},
"pet_color": "PetColor",
"images": {
    "@class": "Image",
    "@type": "Cardinality",
    "@min_cardinality" : 1
}
},
{
"@type": "Class",
"@id": "Dog",
"@inherits": "Pet",
"good_with_children": "xsd:boolean"
},
{
"@type": "Class",
"@id": "Cat",
"@inherits": "Pet",
"declawed": "xsd:boolean"
},
{
"@type": "Class",
"@id": "Bird",
"@inherits": "Pet",
"exotic": "xsd:boolean"
},
{
"@type": "Class",
"@abstract": [],
"@id": "NamedAndCoded",
"code": "xsd:string",
"name": {"@type": "Optional", "@class": "xsd:string"},
"@unfoldable": []
},
{
"@type": "Class",
"@id": "Vaccination",
"@inherits": ["NamedAndCoded"],
"@key": {"@type": "Lexical", "@fields": ["code"]}
},
{
"@type": "Class",
"@id": "PetBreed",
"@inherits": ["NamedAndCoded"],
"@key": {"@type": "Lexical", "@fields": ["code"]}
},
{
"@type": "Class",
"@id": "PetColor",
"@inherits": ["NamedAndCoded"],
"@key": {"@type": "Lexical", "@fields": ["code"]}
},
{
"@type": "Class",
"@id": "Image",
"@key": {"@type": "Lexical", "@fields": ["image_path_name"]},
"image_path_name": "xsd:string",
"featured": {"@type": "Optional", "@class": "xsd:boolean"},
"@unfoldable": []
}
]
```