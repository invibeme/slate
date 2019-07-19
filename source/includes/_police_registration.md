# Police Registration Service


## Register a Guest


```shell
curl -X POST \
  https://api.chekin.io/api/v1.1/tools/police/register/ \
  -H 'Authorization: Token yourUserTokenHere' \
  -H 'Content-Type: application/json' \
  -d '{
        "police_type": "POL",
        "police_user": "H41811AAXQU",
        "police_password": "APARTAMENTOA2017",
        "test_mode": true,
        "check_in_date": "2019-02-22",
        "nights_of_stay": 2,
        "name": "Mariano",
        "first_surname": "Martinez",
        "second_surname": "Grasso",
        "doc_type": "D",
        "doc_number": "25698412S",
        "doc_issue_date": "2012-12-14",
        "sex": "M",
        "nationality": "ESP",
        "birth_date": "1987-07-20",
        "generate_receipt": true,
        "accommodation_nif": "77552368S",
        "accommodation_name": "Carlos Homes",
        "accommodation_province": "Sevilla",
        "accommodation_city": "Huelva",
        "receipt_signature": "data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAGQAAABkCAYAAABw4pVUAAAABHNCSVQICAgIfAhkiAAABERJREFUeAHtmk1S2zAYhj85XXVDMrAnPQHpCTDLhgXuCZqeAHoChhOQG+DewF1Al7g34Aake5jAqmyQ+kqJSWASkD35EeNXMxr/RD+fnlc/n+SIMJAACZAACZAACZAACZAACZAACZAACZAACZAACZAACZAACZAACZAACZAACZAACZAACZAACZAACZAACZAACZAACYRAQPkYkZzfZCJqVz5Gn7K91p1PHqapRiDyyqakKTY+SMcrPRNVJuAniKiBq8FoClIZtV9GP0GMjAXBKGFYKgE/QaIod1YoEy/VGhYufoJIMULUDpktl4CXl2VNSC5urXe1IQqe1pfWwL5bR0h+D9vKyPa8uo2R+2y/dTXv99Dff/A20JhclDoQ/RgjT+qdr2JCB17LjongSBhMlUZZTw/3WsxrZaKLofPYFAMkzCWKTtbZgV4zddZv/oIolaOAA4gS45oiLjRYAURrlO/gQwDdNHb8Ovq4mYzle7ycPwJGwtmptY08PZTTwz7qe7a/lS7U4CUVNmnmGxU4YEZfA9Bdtr/ZeiO518/J+bAjSn9D4gSx/SLTPUZGDiWuIBJi4w49Hc9+YVz2EVLb8qFh9Pk9TGXegtg2Jee3A/S6bbTua9bdyuy7siG5HDbVw+OB0eoIZXWm8qPnS+ZEiBr5oqYZTF99lHuIcn9hlCRT9QV5W06Qi9sjtOIUguQQZK9Mi8ZT0jHyJBCiOc5rRUjhKGRlen+petEB5J8eujxrdkh87C4nyKhxAxS8gfgj627a3vdqeBLCzudPwfzB1Jeual7HKElRtZ26vGx+MnMNN777EGfa6GDR9MZ2nmIKO5xnM4SIk4ubSyyq1xgRRZ6fzm3ubsWrEsPZ59Yi3FlvLfBQaoQUbYHX0oO3dTZ+tutKqgx280bgGekY13hqfSimpf6i1oXCDt/rMhwS37rLpqskiK0EvT/B3qAP8FjkZwQjf/E2xZF9P4Qj+1A2tjNIPXvlvw95lg3u0MjLypwwYvcmpuOSGOxXcPaVdf1d1BdFL+nR7l3wTUekjThADDJUFqRoTSFM8RzuFfsZkV1sPmNcc8QgQ6lFPcgW+BqFDa1v0nWmq48g7+QTQn0EWWe3L1E3BSkBaxVJayPI5GjGeVqrYFupjtoIUonOGjLVS5DRZhWn1jj2DzTUSxBV7D90Eqge3n9yCNX+cnapKHUZlBzjYPQsxJFS+SyrHIlwUr84GMWJDzaM9oukwZ8Bo6kjFY0jFmWaYhonq/zSWDtBbNcYn/4eQQz7sWz24eikD630G0otBZmwhjj2o5v9z7J+bOPwEbEIBiOmMZi4y8V7XkmABEiABEiABEiABEiABEiABEiABEiABEiABEiABEiABEiABEiABEiABEiABEiABEiABEiABEiABEiABEiABEiABEiABEiABEiABEiABEiABEiABEiABEiABEiABEiABN4Hgf9R1jRAiigWLAAAAABJRU5ErkJggg=="
    }
    '
```


> The above command returns JSON structured like this:

```json
  {
      "id": "64672caf4d2140e19d68b222fa0da318",
      "created": "2018-12-01T03:42:21.659258Z",
      "status": "NEW",
      "status_display": "Nuevo",
      "status_details": "",
      "police_type": "POL",
      "police_user": "H41811AAXQU",
      "guest_type": null,
      "name": "MARIANO",
      "first_surname": "MARTINEZ",
      "second_surname": "GRASSO",
      "sex": "M",
      "nationality": "ESP",
      "birth_date": "1987-07-20",
      "birth_place": null,
      "doc_type": "D",
      "doc_number": "25698412S",
      "doc_issue_date": "2012-12-14",
      "doc_isue_place": null,
      "check_in_date": "2019-02-22",
      "nights_of_stay": 2,
      "generate_receipt": true,
      "accommodation_nif": "77552368S",
      "accommodation_name": "Carlos Homes",
      "accommodation_province": "Sevilla",
      "accommodation_city": "Huelva",
      "receipt_url": ""
  }
```

This endpoint sends the guests data to the police.

If you want to register a group of persons (family or just a few people with single document) please check out the following section: **Register a group of people**.

We currently support Spain, Italy and Portugal polices. More countries coming soon!

Optionally, the registration receipt can be generated.
The police registration runs asynchronously, then on this first call the registration will be triggered and you will get a status "NEW".
You will need to do a second call later to check the status until it is "COM" (completion time can be 5-10 seconds).

The police don't allow modifying the guests data once they have been registered successfully.
It also has no problem with changes related to the stay, for example if the number of nights of stay is extended later.
It is not necessary to inform about that type of changes.

If istat credentials are specified the app will send aggregated statistics once a day.
Currently we support ISTAT for italian Radar, Campania, Emilia-Romagna, Abruzzo, Lombardia, Piemonte, Veneto, Toscana Turistat3 and Sardegna.

### HTTP Request

`POST https://api.chekin.io/api/v1.1/tools/police/register/`

### Query Parameters

Parameter | Required | Description
--------- | -------- | -----------
test_mode | false | `false` by default. If it's set to `true`, then the data isn't sent to the police, but you will get the same answer as in a successful registration.
police_type | false | Police type and police credentials are required to send the guests data to the police. Police type depends of the country. See police types by country below.
police_user | false | The username used to do login in the police website.
police_password | false | The password used to do login in the police website.
police_cert_password | false | Used for Italy Only. The password of the certificate which is usually the same as the user password.
establishment_num | false | Used for Portugal Only. It's an extra numer provided by the police to do login.
is_housing_group | false | Used only if police type is POL. Set it to true only if the accommodation is registered at the police as part of a Group.
police_hostelry_code | false | Used only if is_housing_group is true. Hostelry code given by the police to this accommodation.
check_in_date | true | The arrival date in format YYYY-MM-DD, i.e. 2018-12-30
nights_of_stay | true | The number of nights of the stay as an integer, i.e. 3
doc_type | true | Doc types depends on the country. See Doc Types Table below.  
doc_number | true | An alpha-numeric string shown in the identification document.
sex | true | "F" (Female) / "M" (Male)
name | true | The guest's name/s.
first_surname | true | The guest's first surname
second_surname | false | The guest's seconds surname. Only required for spanish people.
doc_issue_date | true | The issue date of the identification document in format YYYY-MM-DD, i.e. 2010-11-23
doc_issue_country | false | Country code in ISO 3-letters format, i.e. ESP (Spain) / DEU (Germany) / ITA (Italy). It is required for Emila-Romagna/Abruzzo/Lombardia/Piemonte/Toscana Turistat3/Sardegna ISTATs.
doc_isue_place | false | Used for Italians in Italy Only. Also it is required if doc_issue_country is Italy. It must be the CODE of one of the Italian cities (see below).
birth_date | true | The guest's birth date in format YYYY-MM-DD, i.e. 1982-10-15
birth_place | false | Used for Italians in Italy Only. It must be the CODE of one of the Italian cities (see below).
nationality | true | Country code in ISO 3-letters format, i.e. ESP (Spain) / DEU (Germany) / ITA (Italy)
residence_country | false | Country code in ISO 3-letters format, i.e. ESP (Spain) / DEU (Germany) / ITA (Italy). It is required for Emila-Romagna/Abruzzo/Lombardia/Piemonte/Toscana Turistat3/Sardegna ISTATs.
residence_city | false | Used if residence_country is Italy. It must be the CODE of one of the Italian cities (see below).
rooms_occupied | false | Number of rooms occupied. Used for Emila-Romagna/Abruzzo/Lombardia/Piemonte/Sardegna ISTATs only.
generate_receipt | false | true by default. If set to false, the registration receipt won't be generated.
accommodation_nif | false | NIF number of the legal holder of the accommodation, to be used in the receipt if generate_receipt is true.
accommodation_name | false | The property name, to be used in the receipt if generate_receipt is true.
accommodation_province | false | The name of teh province where the accommodation is placed, to be used in the receipt if generate_receipt is true.
accommodation_city | false | The name of the city where the accommodation is placed, to be used in the receipt if generate_receipt is true.
receipt_signature | false | The guest signature, base64 encoded, to be used in the receipt if generate_receipt is true.
guest_type | false | Type of guest, can be a `SINGLE` (default value) or a group of people. Check the section **Register a group of guests** for details.
istat_type | false | Istat account type, could be `ITRA` (Italy Radar), `ITCA` (Italy Campania), `ITER` (Emilia-Romagna), `ITAB` (Abruzzo), `ITLO` (Lombardia), `ITPI` (Piemonte), `ITVE` (Veneto), `ITT3` (Toscana Turistat3) and `ITSA` (Sardegna) for now
istat_username | false | Username for istat account
istat_password | false | Password for istat account
istat_structure_code | false | Code of structure (property) for istat account. It needed if you have more than one structure in your Emila-Romagna/Abruzzo/Lombardia/Piemonte/Veneto istat account.
istat_sardegna_city_code | false | Code of city for Sardegna istat account (see below). This field is reguired for `ITSA` (Sardegna) istat_type.

### Test Mode
There is a test mode that can be activated setting the attribute test_mode in true. In this mode you can send any police username and any police password, no real login will be attempted and data won't be sen't to the police. You can use it to test the api or to test your integrations.

To make a real registration you will need to get the property owner user and password that they use to login into the police website.  

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

### Accommodation Group Police Users
The parameter is housing group is optional and it's only used for the police type POL, "Policía Nacional".
In some cases, when the user has a lot of properties, this police gives to the property owners a user of type "Group User".
That means that the user has several accommodations inside the same police account. In that case, you will need to send this parameter "is housing group" in true and you will need to provide also an extra "property subcode" in the parameter police_hostelry_code. That subcode, that identifies the property inside the police account, should be asked to the property owner, and it's shown on the police website.

### Doc types in Spain
Value | Description
----- | -----------
"D" | Spanish ID card, called DNI.
"C" | Spanish Driving Licence.
"N" | Spanish residence permission.
"I" | European ID card.
"X" | Foreign residence permission.
"P" | Passport.


### Doc types in Portugal
Value | Description
--------- | -----------
"B" | Portugal ID, called "BILHETE DE IDENTIDADE".
"P" | Passport.
"O" | For any other documents, like Foreign IDs.


### Doc types in Italy
There are a lot of document types in Italy. The most common ones are "PASSAPORTO ORDINARIO" (Passports), "CARTA DI IDENTITA'" (ID cards without MRZ code), and "CARTA IDENTITA' ELETTRONICA" (ID cards with MRZ code).

Value | Description
------| -----------
"ACMIL" |	"TESS. APP.TO AG.CUSTODIA"
"ACSOT" |	"TESS. SOTT.LI AG.CUSTODIA"
"ACUFF" |	"TESS. UFF.LI AG.CUSTODIA"
"AMMIL" |	"TESS. MILITARE TRUPPA A.M"
"AMSOT"	| "TESS. SOTTUFFICIALI A.M."
"AMUFF" |	"TESS. UFFICIALI A.M."
"CCMIL" |	"TESS. APP.TO CARABINIERI"
"CCSOT" |	"TESS. SOTTUFFICIALI CC"
"CCUFF" |	"TESS. UFFICIALE"
"CERID" |	"CERTIFICATO D'IDENTITA'"
"CFMIL" |	"TESS. AG. E AG.SC. C.F.S."
"CFSOT" |	"TESS. SOTTUFICIALI C.F.S."
"CFUFF" |	"TESS. UFFICIALI C.F.S."
"CIDIP" |	"CARTA ID. DIPLOMATICA"
"DESIS" |	"TESS. S.I.S.D.E."
"EIMIL" |	"TESS. MILITARE E.I."
"EISOT" |	"TESS. SOTTUFFICIALI E.I."
"EIUFF" |	"TESS. UFFICIALI E.I."
"GFMIL" |	"TESS. APP.TO FINANZIERE"
"GFSOT" |	"TESS. SOTT.LI G.D.F."
"GFTRI" |	"TESS. POL. TRIB. G.D.F."
"GFUFF" |	"TESS. UFFICIALI G.D.F."
"IDELE" |	"CARTA IDENTITA' ELETTRONICA"
"IDENT" |	"CARTA DI IDENTITA'"
"MAGIS" |	"TESS. PERS. MAGISTRATI"
"MMMIL" |	"TESS. MILIT. M.M."
"MMSOT" |	"TESS. SOTTUFICIALI M.M."
"MMUFF" |	"TESS. UFFICIALI M.M."
"PARLA" |	"TESS. PARLAMENTARI"
"PASDI" |	"PASSAPORTO DIPLOMATICO"
"PASOR" |	"PASSAPORTO ORDINARIO"
"PASSE" |	"PASSAPORTO DI SERVIZIO"
"PATEN" |	"PATENTE DI GUIDA"
"PATNA" |	"PATENTE NAUTICA"
"PORM1" |	"PORTO FUCILE USO CACCIA"
"PORM2" |	"PORTO FUCILE DIF. PERSON."
"PORM3" |	"PORTO D'ARMI USO SPORTIVO"
"PORM4" |	"PORTO PISTOLA DIF. PERSON"
"PORM5" |	"PORTO D'ARMI GUARDIE GIUR"
"PPAGE" |	"TESS. AGENTI/ASS.TI P.P."
"PPISP" |	"TESS. ISPETTORI P.P."
"PPSOV" |	"TESS. SOVRINTENDENTI P.P."
"PPUFF" |	"TESS. UFFICIALI P.P."
"PSAPP" |	"TESS. AGENTI/ASS.TI P.S."
"PSFEM" |	"TESS. POLIZIA FEMMINILE"
"PSFUN" |	"TESS. FUNZIONARI P.S."
"PSISP" |	"TESS. ISPETTORI P.S."
"PSSOT" |	"TESS. SOVRINTENDENTI P.S."
"PSUFF" |	"TESS. UFFICIALI P.S."
"RIFUG" |	"TITOLO VIAGGIO RIF.POLIT."
"SDMIL" |	"TESS. MILIT. TRUPPA SISMI"
"SDSOT" |	"TESS. SOTTUFFICIALI SISMI"
"SDUFF" |	"TESS. UFFICIALI SISMI"
"TEAMC" | "TESS. ISCR. ALBO MED/CHI."
"TEAOD" |	"TESS. ISCRIZ. ALBO ODONT."
"TECAM" | "TES. UNICO PER LA CAMERA"
"TECOC" |	"TESS. CORTE DEI CONTI"
"TEDOG" |	"TES.DOGANALE RIL.MIN.FIN."
"TEFSE" | "TESS. FERROV. SENATO"
"TEMPI" |	"TESS. MIN.PUBB.ISTRUZIONE"
"TENAT" |	"TESS. MILITARE NATO"
"TENAV" |	"TES. ENTE NAZ. ASSIS.VOLO"
"TEPOL" |	"TESS.MIN.POLIT.AGRIC.FOR."
"TESAE" |	"TESS. MIN. AFFARI ESTERI"
"TESAR" |	"TESS.ISCR.ALBO ARCHITETTI"
"TESAV" |	"TESSERA ISCR. ALBO AVVOC."
"TESCA" |	"TESS. CORTE D'APPELLO"
"TESCS" |	"TESS. CONSIGLIO DI STATO"
"TESDI" |	"TESSERA RICONOSC. D.I.A."
"TESEA" |	"TESS. MEMBRO EQUIP. AEREO"
"TESIN" | "TESS.ISCR. ALBO INGEGNERI"
"TESLP" |	"TESS. MINISTERO LAVORI PU"
"TESMB" |	"TESS. MIN.BEN.E ATT.CULT."
"TESMD" |	"TESS. MINISTERO DIFESA"
"TESMF" |	"TESS. MINISTERO FINANZE"
"TESMG" |	"TESS. MINISTERO GIUSTIZIA"
"TESMI" |	"TESS. MINISTERO INTERNO"
"TESMN" |	"TESS. MINIST. TRASP/NAVIG"
"TESMS" |	"TESS. MINISTERO SANITA'"
"TESMT" |	"TESS. MINISTERO TESORO"
"TESNO" |	"TESSERA DELL'ORDINE NOTAI"
"TESOG" |	"TESS. ORDINE GIORNALISTI"
"TESPC" |	"TESS. PRES.ZA CONS. MIN."
"TESPI" |	"TESS. PUBBLICA ISTRUZIONE"
"TESPT" |	"TES. POSTE E TELECOMUNIC."
"TESUN" |	"TESSERA U.N.U.C.I."
"TETEL" |	"TESS. IDENTIF.TELECOM IT."
"TFERD" | "TES. FERROVIARIA DEPUTATI"
"TFEXD" |	"TES. FERROV. EX DEPUTATI"
"VIMIL" |	"TESS. APP.TO/VIG. URBANO"
"VISOT" |	"TESS. SOTT.LI VIG. URBANI"
"VIUFF" |	"TESS. UFF.LI VIG.URBANI"
"VVMIL" |	"TESS. APP.TO/VIG. VV.FF."
"VVSOT" |	"TESS. SOTTUFF.LI VV.FF."
"VVUFF" |	"TESS. UFFICIALI VV.FF."

### City codes for Sardegna ISTAT

Code | Description
------| -----------
"iw_ca" |	Cagliari
"iw_ci" |	Ministero degli Affari Esteri
"iw_vs" |	Regione Autonoma Della Sardegna
"iw_nu" |	Nuoro
"iw_og" |	Ogliastra
"iw_ot" |	Olbia Tempo
"iw_or" |	Oristano
"iw_ss" |	Sassari

### Italian cities
This field is only required for italians being registered in Italian State Police.

You can get the full list of cities and IDs doing the following request:

`GET https://api.chekin.io/api/v1.1/tools/police/italy/cities/`

The response will be a JSON list of cities with a name and a code. The code must be used in the api.

<aside class="success">
Remember — you need to send the authentication headers with User Token!
</aside>

```shell
curl -X GET \
  https://api.chekin.io/api/v1.1/tools/police/italy/cities/ \
  -H 'Authorization: Token yourUserTokenHere' \
  -H 'Content-Type: application/json'
```


> The above command returns JSON structured like this:

```json
    [
        {
            "text": "AGLIE'",
            "code": "401001001"
        },
        {
            "text": "AIRASCA",
            "code": "401001002"
        },
        {
            "text": "ALA DI STURA",
            "code": "401001003"
        },
        {
            "text": "ALBIANO D'IVREA",
            "code": "401001004"
        }
    ]
```

## Register a group of people

```shell
curl -X POST \
  https://api.chekin.io/api/v1.1/tools/police/register/ \
  -H 'Authorization: Token yourUserTokenHere' \
  -H 'Content-Type: application/json' \
  -d '{
    "test_mode": false,
    "police_type": "ISP",
    "police_user": "somePoliceUser",
    "police_cert_password": "someCertPassword",
    "police_password": "somePolicePassword",
    "check_in_date": "2019-03-04",
    "nights_of_stay": 1,
    "name": "CARLOS ALBERTO",
    "first_surname": "LAGARES GALLARDO",
    "doc_type": "IDELE",
    "doc_number": "75560632C",
    "doc_issue_date": "2014-02-14",
    "sex": "M",
    "nationality": "ESP",
    "birth_date": "1981-11-12",
    "generate_receipt": false,
    "guest_type": "GROUP",
    "group_members": [{
        "name": "MARIANO",
        "surname": "MARTINEZ",
        "nationality": "ESP",
        "sex": "M",
        "birth_date": "1987-07-20",
        "nights_of_stay": 1,
        "birth_place": "ESP"
    }]
}'
```


<aside class="warning">
Warning: Groups currently supported only for Italian State Police
</aside>

If you want to register a group of persons (family or just a few people with a single document)
you have to set the `guest_type` field in the request body and fill in the `group_memebers` field.

The rest of payload is equal to the registration of a single person, as described in previous section.
The person in the root of the request body will be used as a group leader and should contain information that is
necessary to verify that person, such as document type, number, etc. See the previous section for details.

For the `guest_type` you can use one of the following values:

Value | Description
--------- | --------
FAMILY | Family, group of relatives (matches to "17", "Capo Famiglia" in Italian State Police)
GROUP | Generic group, e.g. friends (matches to "18", "Capo Gruppo" in Italian State Police)

The `group_members` has the following structure:


Parameter | Required | Description
--------- | -------- | -----------
name | true | The guest's name/s.
surname | true | The guest's surname
nationality | true | Country code in ISO 3-letters format, i.e. ESP (Spain) / DEU (Germany) / ITA (Italy)
sex | true | "F" (Female) / "M" (Male)
birth_date | true | The guest's birth date in format `YYYY-MM-DD`, i.e. 1982-10-15
birth_place | false | Used for Italians in Italy Only. It must be the CODE of one of the Italian cities (see previous section).
nights_of_stay | true | The number of nights of the stay as an integer, i.e. 3
residence_country | false | Country code in ISO 3-letters format, i.e. ESP (Spain) / DEU (Germany) / ITA (Italy). It is required for Emila-Romagna/Abruzzo/Lombardia/Piemonte/Toscana Turistat3/Sardegna ISTATs.  
residence_city | false | Used if residence_country is Italy. It must be the CODE of one of the Italian cities (see previous section).



## Retrigger Register Person

```shell
curl -X POST \
  https://api.chekin.io/api/v1/checkins/persons/retrigger \
  -H 'Authorization: Token yourUserTokenHere' \
  -H 'Content-Type: application/json' \
  -d '{
        "ids": [
          1189
        ]
      }'
```


> The above command returns JSON structured like this:

```json
    {
      "ids": [
        1189
      ]
    }
```

This endpoint allows retrigger the failed records to the police.

Parameter | Required | Description
--------- | -------- | -----------
ids | true | List of id (must be interger type) of the person checkin.


## Get Registration status & Receipt

```shell
curl -X GET \
  https://api.chekin.io/api/v1.1/tools/police/register/798ee3d0235a4ac7bb0bf5867f1bbb78/ \
  -H 'Authorization: Token yourUserTokenHere' \
  -H 'Content-Type: application/json'
```


> The above command returns JSON structured like this:

```json
    {
        "id": "798ee3d0235a4ac7bb0bf5867f1bbb78",
        "created": "2019-07-04T19:21:25.606112Z",
        "status": "COM",
        "status_display": "Police verification successfully completed",
        "status_details": "",
        "status_istat": "COM",
        "status_istat_display": "ISTAT verification successfully completed",
        "status_istat_details": "",
        "police_type": "ISP",
        "police_user": "test",
        "police_password": "test",
        "police_cert_password": "test",
        "establishment_num": "",
        "guest_type": "SINGLE",
        "name": "ERIC FERNANDO",
        "first_surname": "SANCHEZ",
        "second_surname": "GALVEZ",
        "sex": "M",
        "nationality": "ESP",
        "residence_country": null,
        "residence_city": null,
        "birth_date": "1982-11-21",
        "birth_place": null,
        "doc_issue_country": null,
        "doc_isue_place": null,
        "doc_type": "D",
        "doc_number": "48912467T",
        "doc_issue_date": "2016-02-03",
        "is_housing_group": false,
        "police_hostelry_code": "",
        "check_in_date": "2019-07-03",
        "nights_of_stay": 1,
        "rooms_occupied": null,
        "generate_receipt": true,
        "accommodation_nif": "77552368S",
        "accommodation_name": "Carlos Homes",
        "accommodation_province": "Rome",
        "accommodation_city": "Rome",
        "receipt_url": "https://test3.chekin.io/lnk/g5mse",
        "test_mode": true,
        "is_delayed_execution": false,
        "execution_datetime": null,
        "group_members": [],
        "is_identity_verified": false,
        "istat_type": "ITRA",
        "istat_username": "test",
        "istat_password": "test",
        "istat_structure_code": null,
        "police_country": "ITA"
    }
```

This endpoint returns the registration details, including the police registration status and ISTAT registration status. Also, if parameter generate_receipt = true, then a link to download the receipt will be included.


### HTTP Request

`GET https://api.chekin.io/api/v1.1/tools/police/register/<ID>/`

### URL Parameters

Parameter | Required | Description
--------- | -------- | -----------
ID | true | The ID of the registration, obtained previously when registration was triggered.


### Web Dashboard
You can also manage registers from the dashboard.
You will be able to see a full list of registers, check their status, download receipts, and re-trigger any registration if necessary.

You can access with the user and password used in Sign Up.

[https://tools.chekin.io/login](https://tools.chekin.io/login)
