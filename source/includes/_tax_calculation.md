# Tax calculator

To get taxes you have to specify a bunch of fields common for every location and some fields that are required for a 
specific region or province. Check the sections below to get details.
**Important: the calculator supports age exemptions only. So you don't need pass people with other exemptions kinds to the calculator.**

The common fields are:

- `country_id` - should contain a 2-char country code according to ISO 3166-2
- `date` - guest check in date, ISO 8601-formatted date, `YYYY-MM-DD`, like `2019-01-20`, if skipped will be set to today;
- `nights_number` - number of night the guest stay.

In response you'll get two additional fields: `tax` and `currency` which will contain amount of tax and currency code (like `EUR`)

## Get taxes for Austria

```shell
curl -X POST \
https://api.chekin.io/api/v1/tax/calculation/ \
-H 'Api-key: yourAPIKeyHere' \
-H 'Content-Type: application/json' \
-d '{
  "country_id": "AT",
  "property_type_id": "a4aafe73-2a51-44c9-ad64-a8ad78d9bbe5",  
  "date": "2019-01-01",
  "location_id": "fce69e07-1712-4346-a874-cd5ac4fe79f2",
  "birth_dates": ["1999-04-23", "2007-04-22"],
  "nights_number": 1
}
'
```

> The above command returns JSON structured like this:

```json
{
    "country_id": "AT",
    "property_type_id": "a4aafe73-2a51-44c9-ad64-a8ad78d9bbe5",
    "date": "2019-01-01",   
    "location_id": "fce69e07-1712-4346-a874-cd5ac4fe79f2",
    "nights_number": 1,
    "tax": 1.5,
    "currency": "EUR",
    "ages": [
        20,
        12
    ],
    "birth_dates": [
        "1999-04-23",
        "2007-04-22"
    ]
}
```

The fields you have to specify to get tax calculation for Austria are:

- `birth_dates` - list of date items that are dates of birth of guests. Depending on this there can be various tax discounts;
- `ages` - you can fill in this field with actual guest ages instead of `birth_dates` field;
- `property_type_id` - entity ID from `/api/v1/tax/property-types/`
- `nights_number` - number of nights
- `location_id` - entity ID from `/api/v1/geo/locations/`

Required only for Wien:

- `cost_per_night` - cost of your accomodation per night. Required only for Wien tax calculation.

Additional field `ages` will be added to response if `birth_dates` are specified.

## Get taxes for Italy

```shell
curl -X POST \
https://api.chekin.io/api/v1/tax/calculation/ \
-H 'Api-key: yourAPIKeyHere' \
-H 'Content-Type: application/json' \
-d '{
  "country_id": "IT",
  "property_type_id": "97c6973a-069b-49f0-ad68-5dbe3ff4189f",
  "property_subtype_id": "7095e023-98b4-435d-a52f-d9ebaab0fe58",
  "date": "2019-01-01",
  "location_id": "12c39879-bdb1-4f9a-8c92-cdfabb046596",
  "birth_dates": ["2007-04-23", "2007-04-22"],
  "nights_number": 1
}
'
```

> The above command returns JSON structured like this:

```json
{
    "country_id": "IT",
    "property_type_id": "97c6973a-069b-49f0-ad68-5dbe3ff4189f",
    "property_subtype_id": "7095e023-98b4-435d-a52f-d9ebaab0fe58",
    "date": "2019-01-01",
    "location_id": "12c39879-bdb1-4f9a-8c92-cdfabb046596",
    "nights_number": 1,
    "ages": [
        12,
        12
    ],
    "birth_dates": [
        "2007-04-23",
        "2007-04-22"
    ],
    "tax": 4,
    "currency": "EUR"
}
```

The fields you have to specify to get tax calculation for Italy are:

- `birth_dates` - list of date items that are dates of birth of guests. Depending on this there can be various tax discounts;
- `ages` - you can fill in this field with actual guest ages instead of `birth_dates` field;
- `property_type_id` - entity ID from `/api/v1/tax/property-types/`
- `property_subtype_id` - entity ID from `/api/v1/tax/property-subtypes/`
- `location_id` - entity ID from `/api/v1/geo/locations/`

Additional field `ages` will be added to response if `birth_dates` are specified.

## Get taxes for Portugal

```shell
curl -X POST \
https://api.chekin.io/api/v1/tax/calculation/ \
-H 'Api-key: yourAPIKeyHere' \
-H 'Content-Type: application/json' \
-d '{
  "country_id": "PT",
  "date": "2019-01-01",
  "location_id": "bea00375-a792-48f7-a937-2c73ebab201c",
  "ages": [10, 12, 20],
  "nights_number": 1
}
'
```

> The above command returns JSON structured like this:

```json
{
    "date": "2019-01-01",
    "country_id": "PT",
    "location_id": "bea00375-a792-48f7-a937-2c73ebab201c",
    "nights_number": 1,
    "tax": 1.5,
    "currency": "EUR",
    "ages": [
        10,
        20,
        12
    ]
}
```

The fields you have to specify to get tax calculation for Portugal are:

- `birth_dates` - list of date items that are dates of birth of guests. Depending on this there can be various tax discounts;
- `ages` - you can fill in this field with actual guest ages instead of `birth_dates` field;
- `location_id` - entity ID from `/api/v1/geo/locations/`
- `is_camping` - optional boolean field. You can add it to request with `true` value to get calculate tax for camping. It is `false` by default.

Additional field `ages` will be added to response if `birth_dates` are specified.

## Get taxes for Spain


```shell
curl -X POST \
https://api.chekin.io/api/v1/tax/calculation/ \
-H 'Content-Type: application/json' \
-d '{
     "property_type_id": "675c0357-2226-47c5-8e5c-0f0ba0d30523",
     "region_id": "f787d9cc-e474-4c38-9388-cb04f08b67f9",
     "date": "2019-06-01",
     "country_id": "ES",
     "nights_number": 12,
     "total_people_number": 10,
     "young_people_number": 0
}'
```

> The above command returns JSON structured like this:

```json
{
    "country_id": "ES",
    "property_type_id": "675c0357-2226-47c5-8e5c-0f0ba0d30523",
    "date": "2019-06-01",
    "region_id": "f787d9cc-e474-4c38-9388-cb04f08b67f9",
    "total_people_number": 10,
    "young_people_number": 0,
    "nights_number": 12,
    "tax": 157.5,
    "currency": "EUR"
}
```

- `total_people_number`
- `young_people_number`
- `property_type_id` - entity ID from `/api/v1/tax/property-types/`
- `region_id` - entity ID from `/api/v1/tax/regions/`;
- `province_id` - entity ID from `/api/v1/tax/provinces/`;
- `postal_code` - is required if province is not specified.

## Necessary data

### Property Types

Types are available at `/api/v1/tax/property-types/`
You can filter property types by country, you just need to add `country` param with ISO 2-alpha country code to your request. For example `/api/v1/tax/property-types/?country=IT`

```shell
curl -X GET \
https://api.chekin.io/api/v1/tax/property-types/ \
-H 'Api-key: yourAPIKeyHere' \
-H 'Content-Type: application/json'
```

> The above command returns JSON structured like this:

```json
[
    {
        "id": "460dae62-f8a6-4486-90d3-a0906c3ec186",
        "label": "Touristic accomodation",
        "region_id": "f787d9cc-e474-4c38-9388-cb04f08b67f9",
        "country_id": "ES"
    },
    {
        "id": "ba047676-779d-4b72-81ba-eab28efb2e4e",
        "label": "Other properties",
        "region_id": "f787d9cc-e474-4c38-9388-cb04f08b67f9",
        "country_id": "ES"
    }
]
```

### Property Subtypes

Subtypes are available at `/api/v1/tax/property-subtypes/`
You can filter property subtypes by country, you just need to add `country` param with ISO 2-alpha country code to your request. For example `/api/v1/tax/property-types/?country=IT`

```shell
curl -X GET \
https://api.chekin.io/api/v1/tax/property-subtypes/ \
-H 'Api-key: yourAPIKeyHere' \
-H 'Content-Type: application/json'
```

> The above command returns JSON structured like this:

```json
[
    {
        "id": "0e93e515-7dd8-4d85-8d5b-e77d7ad25a9d",
        "label": "1 star",
        "country_id": "IT"
    },
    {
        "id": "a8492f91-5dfd-416c-888d-57f529fac57a",
        "label": "2 star",
        "country_id": "IT"
    }
]
```

### Geo Locations

Locations are available at `/api/v1/geo/locations/`
You can filter locations by country, you just need to add `country` param with ISO 2-alpha country code to your request. For example `/api/v1/tax/property-types/?country=IT`

```shell
curl -X GET \
https://api.chekin.io/api/v1/geo/locations/ \
-H 'Api-key: yourAPIKeyHere' \
-H 'Content-Type: application/json'
```

> The above command returns JSON structured like this:

```json
[
    {
        "id": "8b644b29-ec8a-4f9e-9fa8-e4d004cb8584",
        "country": "IT",
        "region": "Basilicata",
        "province": null,
        "province_id": null,
        "city": "Matera"
    },
    {
        "id": "cefa3dcd-104c-4bf2-ac6d-9e118a9ff09e",
        "country": "IT",
        "region": "Basilicata",
        "province": null,
        "province_id": null,
        "city": "Policoro"
    }
]
```

### Regions and Provinces

You may need these entities to make a tax calculation for some location in Spain.

Regions are available at `/api/v1/tax/regions/`

```shell
curl -X GET \
https://api.chekin.io/api/v1/tax/regions/ \
-H 'Api-key: yourAPIKeyHere' \
-H 'Content-Type: application/json'
```

> The above command returns JSON structured like this:

```json
[
    {
        "id": "9cd434b9-833c-4978-933d-430a3e279376",
        "name": "Balearic Islands",
        "country_id": "ES"
    },
    {
        "id": "f787d9cc-e474-4c38-9388-cb04f08b67f9",
        "name": "Catalonia",
        "country_id": "ES"
    }
]
```

And the provinces are available at `/api/v1/tax/provinces/`

```shell
curl -X GET \
https://api.chekin.io/api/v1/tax/provinces/ \
-H 'Api-key: yourAPIKeyHere' \
-H 'Content-Type: application/json'
```

> The above command returns JSON structured like this:

```json
[
    {
        "id": "c10a258c-029f-40d4-b3df-cdb7d3334ab0",
        "region_id": "f787d9cc-e474-4c38-9388-cb04f08b67f9",
        "name": "Girona",
        "country_id": "ES"
    },
    {
        "id": "add4f783-821f-423c-8fba-5067270e5991",
        "region_id": "f787d9cc-e474-4c38-9388-cb04f08b67f9",
        "name": "Lleida",
        "country_id": "ES"
    }
]
```
