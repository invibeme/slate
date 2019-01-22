# Check-in Online

Check-in Online allows the guest to register himself in the police, by using a user-friendly WebApp. 

It's a simple solution to register guests in the police, when you don't want to develop your own UX or if you don't want to deal with Guests data.
 

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
    "id": 55,
    "guest_phone": "34685434324",
    "guest_email": "carlos33@gmail.com",
    "accommondation_name": "MY HOUSE",
    "check_in_date": "2019-02-22",
    "status": "BKD"
  }

```

This endpoint allows you to create a Check-in Online. Once you create a Check-in Online, a link is sent to the guest by SMS or email.

The guest will be able to open the link and complete his data through a Web App to be sent to the police.

Optionally you can add and/or combine extra features with the Check-in Online:
 - A Web OCR scanner, combined with a Biometric Match service, can be added to verify the identity of the guest. 
 - If you use electronic locks of one of our supported brands, you can use Chekin Key App to give the guest direct access to the room using Bluetooth, after verifying his identity. 
 

Support for RFID locks comming soon.


### HTTP Request

`POST https://api.chekin.io/api/v1/tools/chekin_online/`


### Query Parameters

Parameter | Required | Description
--------- | -------- | -----------
guest_phone | true | Number of the guest to send the SMS, includes the prefix but without the +.
guest_email | false | Email of the guest to send the email.
include_ocr | true | Indicates whether the OCR Service is included or not.
include_biometric_match | true | Indicates whether the Biometric Matching Service is included or not.
include_smart_locks | true | Indicates whether the opening of smart locks is included or not.
smart_lock_opening_method | false | Indicates the method of opening smart locks, You can see the methods below.
police_type | true | Police type and police credentials are required to send the guests data to the police. Police type depends of the country. See police types by country below. You can see the polices types below.
police_user | true | The username used to do login in the police website.
police_password | true | The password used to do login in the police website.
check_in_date | true | The arrival date in format YYYY-MM-DD, i.e. 2019-03-30.
nights_of_stay | true | The number of nights of the stay as an integer, i.e. 3.
generate_receipt | false | False by default. If set to true, the registration receipt will be generated for each guest.
accommodation_nif | false | NIF number of the legal holder of the accommodation, to be used in the receipt if generate_receipt is true.
accommondation_name | true | The property name, to be used in the receipt if generate_receipt is true.
accommodation_province | false | The name of the city where the accommodation is placed, to be used in the receipt if generate_receipt is true.
accommodation_city | false | The name of the city where the accommodation is placed, to be used in the receipt if generate_receipt is true.



### Smart Lock opening methods
Value | Description
----- | -----------
BLE   | The locks are opened via bluetooth.
RFID  | The locks are opened via RFID card.


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


## Set Lock BLE Key

If you want to use Chekin Key and Smart Locks to allow the guests to open the door you need to provide the Bluetooth binary key.

```shell
curl -X POST \
  https://api.chekin.io/api/v1/tools/chekin_online/ble/key/ \
  -H 'Authorization: Token yourUserTokenHere' \
  -H 'content-type: multipart/form-data;' \
  -F chekin_online=55 \
  -F 'key_file=@/your/local/path/key.bin'
```


> The above command returns JSON structured like this:


```json
  {
    "id": 1,
    "chekin_online": 55,
    "key_file": "some url",
  }

```

### HTTP Request

`POST https://api.chekin.io/api/v1/tools/chekin_online/ble/key/`


### Query Parameters

Parameter | Required | Description
--------- | -------- | -----------
chekin_online | true | ID of the Check-in Online to which this key is associated.
key_file | false | BLE Key to open the door, used by Chekin Key App to open the room's door.


