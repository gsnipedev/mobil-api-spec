# Mobil Mobilan API Documentation

## Base Url :
- http://localhost:8080/api/v1/


## Ambil Semua data Mobil

Request :
- Method : GET
- Endpoint : `/cars`
- Auth Required : NO
- Header :
    - Content Type : application/json
    - Accept : application/json

- Query :
    - Year (Nullable)
    - Keyless (Nullable)
    - Capacity (Nullable)
- Response :
```json
[
  {
    "ID": "Number",
    "Plate": "String",
    "Manufacture": "String",
    "Model": "String",
    "Keyless" : "Boolean",
    "Image": "String",
    "RentPerDay": "Number",
    "Capacity": "Number",
    "Description": "String",
    "Transmission": "String[automatic, manual]",
    "Type": "String",
    "Year": "String",
    "Options": [
      "Nitrous Oxide System",
      "Drift Tires"
    ],
    "Specs": [
      "Torsi 5000 RPM",
      "Pake turbo"
    ],
    "AvailableAt": "String"
  }
]
```

- Success Response Example:

```json
[
  {
    "ID": 0,
    "Plate": "AB 2022 CD",
    "Manufacture": "Toyota",
    "Model": "Supra",
    "Keyless" : false,
    "Image": "https://lorem.picsum",
    "RentPerDay": 2000000,
    "Capacity": 4,
    "Description": "Mobil keren, supra mk4 bisa dipake balapan",
    "Transmission": "Manual",
    "Type": "MK4",
    "Year": "2000",
    "Options": [
      "Nitrous Oxide System",
      "Drift Tires"
    ],
    "Specs": [
      "Torsi 5000 RPM",
      "Pake turbo"
    ],
    "AvailableAt": "20-05-2023"
  },
  {
    "ID": 1,
    "Plate": "AB 5555 CD",
    "Manufacture": "Hummer",
    "Model": "GMC",
    "Keyless" : true,
    "Image": "https://upload.wikimedia.org/wikipedia/commons/thumb/1/1d/GMC_Hummer_EV.jpg/450px-GMC_Hummer_EV.jpg",
    "RentPerDay": 5000000,
    "Capacity": 6,
    "Description": "Mobil keren, supra mk4 bisa dipake offroad",
    "Transmission": "Manual",
    "Type": "EV",
    "Year": "2001",
    "Options": [
      "Enforced Front and Rear Bumper",
      "Enforced Window"
    ],
    "Specs": [
      "7500 Tenaga Kuda",
      "Bisa bawa beban sampai dengan 500 Kilogram"
    ],
    "AvailableAt": "20-05-2023"
  }
]
```

## Ambil Data Mobil Berdasarkan ID

Request :
- Method : GET
- Endpoint : `/cars/{id}`
- Auth Required : NO
- Header :
    - Content Type : application/json
    - Accept : application/json
- Success Response Example :
```json
  {
    "ID": 1,
    "Plate": "AB 5555 CD",
    "Manufacture": "Hummer",
    "Model": "GMC",
    "Keyless" : true,
    "Image": "https://upload.wikimedia.org/wikipedia/commons/thumb/1/1d/GMC_Hummer_EV.jpg/450px-GMC_Hummer_EV.jpg",
    "RentPerDay": 5000000,
    "Capacity": 6,
    "Description": "Mobil keren, supra mk4 bisa dipake offroad",
    "Transmission": "Manual",
    "Type": "EV",
    "Year": "2001",
    "Options": [
      "Enforced Front and Rear Bumper",
      "Enforced Window"
    ],
    "Specs": [
      "7500 Tenaga Kuda",
      "Bisa bawa beban sampai dengan 500 Kilogram"
    ],
    "AvailableAt": "20-05-2023"
  }
```
