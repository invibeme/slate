# Chekin Online


## Create Checkin Online


```shell
curl -X POST \
  https://api.chekin.io/api/v1/tools/chekin_online/ \
  -H 'Authorization: Token yourUserTokenHere' \
  -H 'Content-Type: application/json' \
  -d '{
        "guest_phone": "34685434324",
        "guest_email": "carlos33@gmail.com",
        "police_type": "POL",
        "police_user": "H41811AAXQU",
        "police_password": "APARTAMENTOA2017",
        "check_in_date": "2019-02-22",
        "nights_of_stay": "4",
        "generate_receipt": false,
        "accommondation_name": "MY HOUSE",
        "accommodation_nif": "77552368S",
        "accommodation_province": "Andalucia",
        "accommodation_city": "Huelva",
        "include_ocr": "false",
        "include_biometric_match": "false",
        "include_smart_locks": "true",
        "smart_lock_opening_method": "BLE"
      }
      '
```


> The above command returns JSON structured like this:


```json
  {
    "id": 1,
    "guest_phone": "34685434324",
    "guest_email": "carlos33@gmail.com",
    "accommondation_name": "MY HOUSE",
    "check_in_date": "2019-02-22",
    "status": "BKD"
  }

```

This endpoint allows you to send an online check in to the guest by SMS or email.

Optionally includes the opening of locks by Bluetooth or RFID, OCR Web services, and Biometric Matching services.


### HTTP Request

`POST https://api.chekin.io/api/v1/tools/chekin_online/`


### Query Parameters

Parameter | Required | Description
--------- | -------- | -----------
guest_phone | true | Number of the guest to register, includes the prefix but without the +.
guest_email | false | Email of the guest to register.
police_type | true | Police type and police credentials are required to send the guests data to the police. Police type depends of the country. See police types by country below. You can see the polices types below.
police_user | true | The username used to do login in the police website.
police_password | true | The password used to do login in the police website.
check_in_date | true | The arrival date in format YYYY-MM-DD, i.e. 2018-12-30.
nights_of_stay | true | The number of nights of the stay as an integer, i.e. 3.
generate_receipt | false | False by default. If set to false, the registration receipt won't be generated.
accommodation_nif | false | NIF number of the legal holder of the accommodation, to be used in the receipt if generate_receipt is true.
accommondation_name | true | The property name, to be used in the receipt if generate_receipt is true.
accommodation_province | false | The name of the city where the accommodation is placed, to be used in the receipt if generate_receipt is true.
accommodation_city | false | The name of the city where the accommodation is placed, to be used in the receipt if generate_receipt is true.
include_ocr | true | Indicates whether the OCR Service is included or not.
include_biometric_match | true | Indicates whether the Biometric Matching Service is included or not.
include_smart_locks | true | Indicates whether the opening of smart locks is included or not.
smart_lock_opening_method | false | Indicates the method of opening smart locks, You can see the methods below.

The fields shown below are stored encrypted:

`guest_phone, guest_email, accommondation_name, accommodation_nif, accommodation_name, accommodation_province, accommodation_city, police_type, police_user, police_password`


### Smart Lock openenig methods
Value | Description
----- | -----------
BLE   | Method for opening locks via bluetooth.
RFID  | Method for opening locks via RFID card.

### Police types in Spain
Police type will set which is the final police organization to which you want to send the data. Remember that there are 4 police forces in Spain:

Value | Description
----- | -----------
"POL" | Data is sent to "Policía Nacional".
"NAT" | Data is sent to "Guardia Civil".
"ERT" | Data is sent to "Ertzaintza".
"MOS" | Data is sent to "Mossos d'Esquadra".


### Police types in Portugal
Police type will set which is the final police organization to which you want to send the data. There is a single police organization in Portugal for this matters:

Value | Description
----- | -----------
"SEF" | Data is sent to "Serviço de Estrangeiros e Fronteiras".


### Police types in Italy
Police type will set which is the final police organization to which you want to send the data. There is a single police organization in Italy:

Value | Description
----- | -----------
"ISP" | Data is sent to "Polizia di Stato".
