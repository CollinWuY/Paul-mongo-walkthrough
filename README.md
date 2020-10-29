
# Animal Shelter DB
1. View the details of all the animals in the Shelter
2. Add in a new animal
3. Update an existing animal
4. View the details of all the vets that are taking care of the animals
5. Keep Track of which vet is taking care of which animal

# Animal Document (represent one animal)
```
{
    "_id": ObjectId("1234567"),
    "name": "Fluffy",
    "species": "Dog",
    "breed": "Golden Retriever",
    "microchip": "X12345Z"
}
```

# Vet Document (represent one vet)
```
{
    "_id": ObjectId("55667788"),
    "first_name": "Mary",
    "last_name": "Sue",
    "address": Telok Blangah Lane 14 #01-01",
    "license": "NAR12355"
}
```
# Checkup (document references)
```
{
    "_id": ObjectId("7717771")
    "animal_id": ObjectId("1234567"),
    "vet_id": ObjectId("55667788"),
    "diagnosis": "Overweight",
    "treatment": "Go on a diet"}
```
# Checkup (using embedded document)
```
{
    "_id": ObjectId("1234567"),
    "name": "Fluffy",
    "species": "Dog",
    "breed": "Golden Retriever",
    "microchip": "X12345Z",
    "checkups":[
        {
            "_id": ObjectId("1123555"),
            "vet_id": ObjectId("55667788"),
            "vet": "Mary Sue",
            "license": "NAR12355"
            "diagnosis": "Overweight",
            "treatment": "Go on a diet",
            "date": "21-08-2019"
        },   
        
        {
            "_id": ObjectId("1234555"),
            "vet_id": ObjectId("55667788"),
            "vet": "Mary Sue",
            "license": "NAR12355"
            "diagnosis": "Cancer"
            "treatment": "Operation"
            "date": "20-05-2020"
        }

    ]


}
```