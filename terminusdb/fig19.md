# Figure 19

Nested physical data models for our animal shelter.
This diagram uses Mermaid’s class-diagram mode.
“¶” indicates a reference rather than an embedding.
“{}” indicates a Set collection.
A filled-in diamond signifies composition, and an open diamond signifies aggregation.
“*” indicates the attribute is required.

```mermaid
%%{init: {"theme": "neutral"} }%%
classDiagram
  class Gender {
    gender_code ＊  ＜xsd∶string＞
    gender_name ＊  ＜xsd∶string＞
  }
  class VaccinationType {
    vaccination_code ＊  ＜xsd∶string＞
    vaccination_name ＊  ＜xsd∶string＞
  }
  Pet --* Gender
  Pet --o Vaccination
  class Pet {
    gender ＊  ¶＜Gender＞
    pet_number ＊  ＜xsd∶integer＞
    vaccinations｛｝ ¶＜Vaccination＞
  }
  Vaccination --* VaccinationType
  class Vaccination {
    vaccination_date ＊  ＜xsd∶date＞
    vaccination_type ＊  ¶＜VaccinationType＞
  }
```