---
description: >-
  This API provides comprehensive data about Filecoin Storage Providers
  renewable energy purchases and consumption.
---

# 📈 Renewable Energy Certificates API

{% hint style="info" %}
**Good to know:** Comprehensive Open API documentation for all API methods is available [here](https://proofs-api.zerolabs.green/swagger/). Please note that you will need and API key for all endpoints that are covered in swagger but not listed here below.
{% endhint %}

## Filecoin Storage Providers

Listing all Filecoin Storage Providers who has purchased and consumed RECs.

{% swagger method="get" path="" baseUrl="https://proofs-api.zerolabs.green/api/partners/filecoin/nodes" summary="List Filecoin Storage Providers with purchased and consumed RECs" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-response status="200: OK" description="JSON response" %}
```javascript
[
  {
    "id": "f01051178",
    "buyerId": "6f48fb1a-5c54-4067-9ad3-430e24c506ec",
    "blockchainAddress": null,
    "createdAt": "2022-02-07T15:52:00.419Z",
    "updatedAt": "2022-02-07T15:52:00.419Z"
  },
  {
    "id": "f066596",
    "buyerId": "53fb6148-eb21-42de-91d6-f6195d028520",
    "blockchainAddress": null,
    "createdAt": "2022-02-07T15:52:00.419Z",
    "updatedAt": "2022-02-07T15:52:00.419Z"
  },
  {
    "id": "f0763337",
    "buyerId": "53fb6148-eb21-42de-91d6-f6195d028520",
    "blockchainAddress": null,
    "createdAt": "2022-02-07T15:52:00.419Z",
    "updatedAt": "2022-02-07T15:52:00.419Z"
  }
]
```
{% endswagger-response %}
{% endswagger %}

## Transactions

Listing all transactions for specified Filecoin Storage Provider.

{% swagger method="get" path="" baseUrl="https://proofs-api.zerolabs.green/api/partners/filecoin/nodes/{minerID}/transactions" summary="Listing all transactions for specified Filecoin Storage Provider." %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-parameter in="path" name="minerID*" type=" " %}
Miner Id (e.g. f01234)
{% endswagger-parameter %}

{% swagger-response status="200: OK" description="JSON response" %}
```javascript
{
	"minerId": "f01234",
	"buyerId": "93e399fb-991d-4f86-a315-4a1df8d18aee",
	"pageUrl": "https://proofs.zerolabs.green/partners/filecoin/nodes/f01234/beneficiary",
	"dataUrl": "https://proofs-api.zerolabs.green/api/partners/filecoin/nodes/f01234/transactions",
	"recsTotal": "260000000",
	"transactions": [{
		"id": "01ea3ef4-6163-4d46-8684-d523d9fa1f21",
		"pageUrl": "https://proofs.zerolabs.green/partners/filecoin/purchases/01ea3ef4-6163-4d46-8684-d523d9fa1f21",
		"dataUrl": "https://proofs-api.zerolabs.green/api/partners/filecoin/purchases/01ea3ef4-6163-4d46-8684-d523d9fa1f21",
		"downloadUrl": "https://proofs-api.zerolabs.green/api/files/0c160c7c-56b8-4721-be79-9217175ddc87",
		"sellerId": "8c0a45ce-1594-4107-baf0-ce8846b34afd",
		"reportingStart": "2020-01-01T00:00:00.000Z",
		"reportingStartTimezoneOffset": 60,
		"reportingEnd": "2020-12-31T23:59:59.999Z",
		"reportingEndTimezoneOffset": 60,
		"txHash": "0xea498b580c96b2758875c3fe333b489304a825fce548b65ba11d6112bad01679",
		"buyerId": "93e399fb-991d-4f86-a315-4a1df8d18aee",
		"contractId": "67f6aa92-aab3-4e3a-975d-e056ca8325be",
		"createdAt": "2022-05-26T13:52:49.567Z",
		"updatedAt": "2022-05-31T09:15:23.733Z",
		"recsSoldWh": "96000000",
		"reportingStartLocal": "2020-01-01T01:00:00.000+01:00",
		"reportingEndLocal": "2021-01-01T00:59:59.999+01:00",
		"generation": {
			"id": "f65360f5-8c1c-41c2-b662-176819eeea08",
			"energyWh": 96000000,
			"generatorName": "Amela",
			"generatorId": "did:zl:DG000000000001",
			"region": "",
			"country": "NO",
			"productType": "GO",
			"energySource": "HYDRO",
			"generationStart": "2021-03-04T00:00:00.000Z",
			"generationStartTimezoneOffset": 120,
			"generationEnd": "2021-03-04T23:59:59.999Z",
			"generationEndTimezoneOffset": 120,
			"txHash": "0xceaa23af72f40ea82ab360970507321b8df7aaf95a513d22b622086909fa9ad6",
			"initialSellerId": "8c0a45ce-1594-4107-baf0-ce8846b34afd",
			"redemptionDate": "2021-08-31T00:00:00.000Z",
			"nameplateCapacityW": 32000000,
			"commissioningDate": "1977-01-01T00:00:00.000Z",
			"commissioningDateTimezoneOffset": null,
			"label": null,
			"certificateCid": "bafyreigpm5ox3q7poet33kajd3wt4tkntrcjdaaqw7izbcztc5dtxwqsyu",
			"batchId": "2",
			"onchainId": "25",
			"createdAt": "2022-05-24T14:31:54.923Z",
			"updatedAt": "2022-05-26T09:16:16.983Z",
			"generationStartLocal": "2021-03-04T02:00:00.000+02:00",
			"generationEndLocal": "2021-03-05T01:59:59.999+02:00"
		}
	}, {
		"id": "bd9d1f9d-63b6-456b-a514-725d3dd5f6d4",
		"pageUrl": "https://proofs.zerolabs.green/partners/filecoin/purchases/bd9d1f9d-63b6-456b-a514-725d3dd5f6d4",
		"dataUrl": "https://proofs-api.zerolabs.green/api/partners/filecoin/purchases/bd9d1f9d-63b6-456b-a514-725d3dd5f6d4",
		"downloadUrl": "https://proofs-api.zerolabs.green/api/files/0c160c7c-56b8-4721-be79-9217175ddc87",
		"sellerId": "8c0a45ce-1594-4107-baf0-ce8846b34afd",
		"reportingStart": "2020-01-01T00:00:00.000Z",
		"reportingStartTimezoneOffset": 60,
		"reportingEnd": "2020-12-31T23:59:59.999Z",
		"reportingEndTimezoneOffset": 60,
		"txHash": "0x44fd62956c3b35f6bfa222458125e6e45880608364a9a88023313dca4188e580",
		"buyerId": "93e399fb-991d-4f86-a315-4a1df8d18aee",
		"contractId": "dbb6cec0-32b3-4e0b-b725-41143035fbfc",
		"createdAt": "2022-05-26T13:58:00.234Z",
		"updatedAt": "2022-05-31T09:15:26.186Z",
		"recsSoldWh": "2000000",
		"reportingStartLocal": "2020-01-01T01:00:00.000+01:00",
		"reportingEndLocal": "2021-01-01T00:59:59.999+01:00",
		"generation": {
			"id": "4b57da72-eef2-414f-8902-c4867b5a76a2",
			"energyWh": 2000000,
			"generatorName": "Solhom kraftverk",
			"generatorId": "did:zl:DG000000000002",
			"region": "",
			"country": "NO",
			"productType": "GO",
			"energySource": "HYDRO",
			"generationStart": "2020-10-01T00:00:00.000Z",
			"generationStartTimezoneOffset": 120,
			"generationEnd": "2020-10-01T23:59:59.999Z",
			"generationEndTimezoneOffset": 120,
			"txHash": "0xceaa23af72f40ea82ab360970507321b8df7aaf95a513d22b622086909fa9ad6",
			"initialSellerId": "8c0a45ce-1594-4107-baf0-ce8846b34afd",
			"redemptionDate": "2021-08-31T00:00:00.000Z",
			"nameplateCapacityW": 200000000,
			"commissioningDate": "1974-07-10T00:00:00.000Z",
			"commissioningDateTimezoneOffset": null,
			"label": null,
			"certificateCid": "bafyreiekntvja5jy52zarj34xqtncnpaj5xohecnk3lck6ikimrr2seppa",
			"batchId": "2",
			"onchainId": "24",
			"createdAt": "2022-05-24T14:31:54.915Z",
			"updatedAt": "2022-05-26T09:16:16.978Z",
			"generationStartLocal": "2020-10-01T02:00:00.000+02:00",
			"generationEndLocal": "2020-10-02T01:59:59.999+02:00"
		}
	}, {
		"id": "8e19e574-ee98-45f8-8388-7591b45395c7",
		"pageUrl": "https://proofs.zerolabs.green/partners/filecoin/purchases/8e19e574-ee98-45f8-8388-7591b45395c7",
		"dataUrl": "https://proofs-api.zerolabs.green/api/partners/filecoin/purchases/8e19e574-ee98-45f8-8388-7591b45395c7",
		"downloadUrl": "https://proofs-api.zerolabs.green/api/files/bd3720bc-3b74-4cf2-8080-1d42a8223c76",
		"sellerId": "8c0a45ce-1594-4107-baf0-ce8846b34afd",
		"reportingStart": "2021-07-01T00:00:00.000Z",
		"reportingStartTimezoneOffset": 120,
		"reportingEnd": "2021-07-31T23:59:59.999Z",
		"reportingEndTimezoneOffset": 120,
		"txHash": "0x3f3301c5a0f616a7899a3ddb57c0a99468e06ec68063ef129a01f5128803ebaf",
		"buyerId": "93e399fb-991d-4f86-a315-4a1df8d18aee",
		"contractId": "57ddb1b2-51e9-4f49-b8dd-b722c9a028dd",
		"createdAt": "2022-06-10T08:43:07.310Z",
		"updatedAt": "2022-06-10T08:43:10.921Z",
		"recsSoldWh": "32000000",
		"reportingStartLocal": "2021-07-01T02:00:00.000+02:00",
		"reportingEndLocal": "2021-08-01T01:59:59.999+02:00",
		"generation": {
			"id": "50efda2a-cdf1-41bc-99b1-fbaddfda48de",
			"energyWh": 32000000,
			"generatorName": "Unknown",
			"generatorId": "Unknown",
			"region": "",
			"country": "BE",
			"productType": "GO",
			"energySource": "WIND",
			"generationStart": "2021-07-31T00:00:00.000Z",
			"generationStartTimezoneOffset": 120,
			"generationEnd": "2021-07-31T23:59:59.999Z",
			"generationEndTimezoneOffset": 120,
			"txHash": "0x521cc95a6b8b465b606895501672ce86a80561d9911215f2ce25b233fd71d200",
			"initialSellerId": "8c0a45ce-1594-4107-baf0-ce8846b34afd",
			"redemptionDate": null,
			"nameplateCapacityW": null,
			"commissioningDate": null,
			"commissioningDateTimezoneOffset": null,
			"label": null,
			"certificateCid": "bafyreiag3iixpg7embrfrcm3gwuhqa6iipntlozohjvzmpo3peihg6eqg4",
			"batchId": "829",
			"onchainId": "852",
			"createdAt": "2022-06-08T21:02:33.380Z",
			"updatedAt": "2022-06-10T05:31:36.733Z",
			"generationStartLocal": "2021-07-31T02:00:00.000+02:00",
			"generationEndLocal": "2021-08-01T01:59:59.999+02:00"
		}
	}, {
		"id": "8612ce5a-6c37-4d7a-a8ea-bbdcb3456fcf",
		"pageUrl": "https://proofs.zerolabs.green/partners/filecoin/purchases/8612ce5a-6c37-4d7a-a8ea-bbdcb3456fcf",
		"dataUrl": "https://proofs-api.zerolabs.green/api/partners/filecoin/purchases/8612ce5a-6c37-4d7a-a8ea-bbdcb3456fcf",
		"downloadUrl": "https://proofs-api.zerolabs.green/api/files/bd3720bc-3b74-4cf2-8080-1d42a8223c76",
		"sellerId": "8c0a45ce-1594-4107-baf0-ce8846b34afd",
		"reportingStart": "2021-08-01T00:00:00.000Z",
		"reportingStartTimezoneOffset": 120,
		"reportingEnd": "2021-08-31T23:59:59.999Z",
		"reportingEndTimezoneOffset": 120,
		"txHash": "0xc61d738ba67531d764d9419b95efacd2c0a05a85c1e9cee28b2df7a3082cccc1",
		"buyerId": "93e399fb-991d-4f86-a315-4a1df8d18aee",
		"contractId": "e51bd084-cdcd-4a2a-b095-b1787de6e12e",
		"createdAt": "2022-06-10T08:43:25.019Z",
		"updatedAt": "2022-06-10T08:43:28.566Z",
		"recsSoldWh": "31000000",
		"reportingStartLocal": "2021-08-01T02:00:00.000+02:00",
		"reportingEndLocal": "2021-09-01T01:59:59.999+02:00",
		"generation": {
			"id": "00030616-52ef-4aab-a539-dfeb9980a25b",
			"energyWh": 31000000,
			"generatorName": "Unknown",
			"generatorId": "Unknown",
			"region": "",
			"country": "BE",
			"productType": "GO",
			"energySource": "WIND",
			"generationStart": "2021-08-31T00:00:00.000Z",
			"generationStartTimezoneOffset": 120,
			"generationEnd": "2021-08-31T23:59:59.999Z",
			"generationEndTimezoneOffset": 120,
			"txHash": "0x9d27b4be06692b517ad5d4d256ce3d854d1e1068118e87d0cae6a0b9bbdd48f9",
			"initialSellerId": "8c0a45ce-1594-4107-baf0-ce8846b34afd",
			"redemptionDate": null,
			"nameplateCapacityW": null,
			"commissioningDate": null,
			"commissioningDateTimezoneOffset": null,
			"label": null,
			"certificateCid": "bafyreigby5wy47t67nicwbco6oxoskboqllkun7lvxysbh6hpvrkydhohq",
			"batchId": "829",
			"onchainId": "856",
			"createdAt": "2022-06-08T21:02:33.475Z",
			"updatedAt": "2022-06-10T05:33:05.855Z",
			"generationStartLocal": "2021-08-31T02:00:00.000+02:00",
			"generationEndLocal": "2021-09-01T01:59:59.999+02:00"
		}
	}, {
		"id": "adcae032-0a58-42c7-b885-ac43db1e3cfc",
		"pageUrl": "https://proofs.zerolabs.green/partners/filecoin/purchases/adcae032-0a58-42c7-b885-ac43db1e3cfc",
		"dataUrl": "https://proofs-api.zerolabs.green/api/partners/filecoin/purchases/adcae032-0a58-42c7-b885-ac43db1e3cfc",
		"downloadUrl": "https://proofs-api.zerolabs.green/api/files/bd3720bc-3b74-4cf2-8080-1d42a8223c76",
		"sellerId": "8c0a45ce-1594-4107-baf0-ce8846b34afd",
		"reportingStart": "2020-07-01T00:00:00.000Z",
		"reportingStartTimezoneOffset": 120,
		"reportingEnd": "2021-03-31T23:59:59.999Z",
		"reportingEndTimezoneOffset": 120,
		"txHash": "0x1141041e3f2ee3d24d7d3517c0fabdcb52b5fe4b3dc6631c5c3b7be3971d32f5",
		"buyerId": "93e399fb-991d-4f86-a315-4a1df8d18aee",
		"contractId": "c6a7c25c-9a1f-48a3-9cb7-5b607ab157f0",
		"createdAt": "2022-06-10T08:46:28.746Z",
		"updatedAt": "2022-06-10T08:46:32.276Z",
		"recsSoldWh": "2000000",
		"reportingStartLocal": "2020-07-01T02:00:00.000+02:00",
		"reportingEndLocal": "2021-04-01T01:59:59.999+02:00",
		"generation": {
			"id": "8bb185c8-4e8b-4216-97b8-6ca9a3659f77",
			"energyWh": 8000000,
			"generatorName": "Unknown",
			"generatorId": "Unknown",
			"region": "",
			"country": "BE",
			"productType": "GO",
			"energySource": "WIND",
			"generationStart": "2021-01-31T00:00:00.000Z",
			"generationStartTimezoneOffset": 60,
			"generationEnd": "2021-01-31T23:59:59.999Z",
			"generationEndTimezoneOffset": 60,
			"txHash": "0xec9eb272a15b09d430024ec57317a6dc4830e51a5b93467066f23f96c66dff18",
			"initialSellerId": "8c0a45ce-1594-4107-baf0-ce8846b34afd",
			"redemptionDate": null,
			"nameplateCapacityW": null,
			"commissioningDate": null,
			"commissioningDateTimezoneOffset": null,
			"label": null,
			"certificateCid": "bafyreigvwzcyknenclgli7h53rokkdahkzow5rapicha4cbkotqcrucgve",
			"batchId": "829",
			"onchainId": "849",
			"createdAt": "2022-06-08T21:02:33.347Z",
			"updatedAt": "2022-06-10T05:30:31.653Z",
			"generationStartLocal": "2021-01-31T01:00:00.000+01:00",
			"generationEndLocal": "2021-02-01T00:59:59.999+01:00"
		}
	}, {
		"id": "44821e40-431e-4081-9661-5dc3c1d5a9fe",
		"pageUrl": "https://proofs.zerolabs.green/partners/filecoin/purchases/44821e40-431e-4081-9661-5dc3c1d5a9fe",
		"dataUrl": "https://proofs-api.zerolabs.green/api/partners/filecoin/purchases/44821e40-431e-4081-9661-5dc3c1d5a9fe",
		"downloadUrl": "https://proofs-api.zerolabs.green/api/files/bd3720bc-3b74-4cf2-8080-1d42a8223c76",
		"sellerId": "8c0a45ce-1594-4107-baf0-ce8846b34afd",
		"reportingStart": "2021-05-01T00:00:00.000Z",
		"reportingStartTimezoneOffset": 120,
		"reportingEnd": "2021-05-31T23:59:59.999Z",
		"reportingEndTimezoneOffset": 120,
		"txHash": "0x880d9f5c7e6e5e3bdfb9e811834cf45004424484c1ccc91f50eb032226b1cf8a",
		"buyerId": "93e399fb-991d-4f86-a315-4a1df8d18aee",
		"contractId": "b0da09da-50af-4ab8-ba23-a809d3165ff8",
		"createdAt": "2022-06-10T08:45:57.784Z",
		"updatedAt": "2022-06-10T08:46:01.359Z",
		"recsSoldWh": "26000000",
		"reportingStartLocal": "2021-05-01T02:00:00.000+02:00",
		"reportingEndLocal": "2021-06-01T01:59:59.999+02:00",
		"generation": {
			"id": "6aa16c57-c122-4a33-a5a4-0d6c4dc45387",
			"energyWh": 26000000,
			"generatorName": "Unknown",
			"generatorId": "Unknown",
			"region": "",
			"country": "BE",
			"productType": "GO",
			"energySource": "WIND",
			"generationStart": "2021-05-31T00:00:00.000Z",
			"generationStartTimezoneOffset": 120,
			"generationEnd": "2021-05-31T23:59:59.999Z",
			"generationEndTimezoneOffset": 120,
			"txHash": "0x8fb504a7cb1f8486be0a2b65d9a49a847794fdc9ca0a874dced6a5fe9d4009c1",
			"initialSellerId": "8c0a45ce-1594-4107-baf0-ce8846b34afd",
			"redemptionDate": null,
			"nameplateCapacityW": null,
			"commissioningDate": null,
			"commissioningDateTimezoneOffset": null,
			"label": null,
			"certificateCid": "bafyreigsinfzhypyxsfc72y5ixujbpkv4kwqqb5duj6etrkappugdvnece",
			"batchId": "829",
			"onchainId": "854",
			"createdAt": "2022-06-08T21:02:33.435Z",
			"updatedAt": "2022-06-10T05:32:15.657Z",
			"generationStartLocal": "2021-05-31T02:00:00.000+02:00",
			"generationEndLocal": "2021-06-01T01:59:59.999+02:00"
		}
	}, {
		"id": "69e492f5-743e-446e-9f08-b1065ffa1bcf",
		"pageUrl": "https://proofs.zerolabs.green/partners/filecoin/purchases/69e492f5-743e-446e-9f08-b1065ffa1bcf",
		"dataUrl": "https://proofs-api.zerolabs.green/api/partners/filecoin/purchases/69e492f5-743e-446e-9f08-b1065ffa1bcf",
		"downloadUrl": "https://proofs-api.zerolabs.green/api/files/bd3720bc-3b74-4cf2-8080-1d42a8223c76",
		"sellerId": "8c0a45ce-1594-4107-baf0-ce8846b34afd",
		"reportingStart": "2021-03-01T00:00:00.000Z",
		"reportingStartTimezoneOffset": 120,
		"reportingEnd": "2021-03-31T23:59:59.999Z",
		"reportingEndTimezoneOffset": 120,
		"txHash": "0xda822301f61b47b5113a4b65553753619b8bd61454f4dbc69c0fd8d214fef1b9",
		"buyerId": "93e399fb-991d-4f86-a315-4a1df8d18aee",
		"contractId": "bfcd046f-2f78-4652-b8fd-b1df27c64fd2",
		"createdAt": "2022-06-10T08:49:02.428Z",
		"updatedAt": "2022-06-10T08:49:05.885Z",
		"recsSoldWh": "20000000",
		"reportingStartLocal": "2021-03-01T02:00:00.000+02:00",
		"reportingEndLocal": "2021-04-01T01:59:59.999+02:00",
		"generation": {
			"id": "7e02a47a-d7c7-4dca-be2a-80a998bcd1cc",
			"energyWh": 20000000,
			"generatorName": "Unknown",
			"generatorId": "Unknown",
			"region": "",
			"country": "BE",
			"productType": "GO",
			"energySource": "WIND",
			"generationStart": "2021-03-31T00:00:00.000Z",
			"generationStartTimezoneOffset": 120,
			"generationEnd": "2021-03-31T23:59:59.999Z",
			"generationEndTimezoneOffset": 120,
			"txHash": "0x79314802ba7aed0c7845cddf9b7c8f8f19719e66fa091b03426dcd571839e39a",
			"initialSellerId": "8c0a45ce-1594-4107-baf0-ce8846b34afd",
			"redemptionDate": null,
			"nameplateCapacityW": null,
			"commissioningDate": null,
			"commissioningDateTimezoneOffset": null,
			"label": null,
			"certificateCid": "bafyreieatianuteeij6oky7xnxjvaghrh7kt4roydyihlxpj4logo2ulme",
			"batchId": "829",
			"onchainId": "851",
			"createdAt": "2022-06-08T21:02:33.371Z",
			"updatedAt": "2022-06-10T05:31:16.815Z",
			"generationStartLocal": "2021-03-31T02:00:00.000+02:00",
			"generationEndLocal": "2021-04-01T01:59:59.999+02:00"
		}
	}, {
		"id": "c6924a11-0cc8-43f7-8fbf-00cd6fb0032a",
		"pageUrl": "https://proofs.zerolabs.green/partners/filecoin/purchases/c6924a11-0cc8-43f7-8fbf-00cd6fb0032a",
		"dataUrl": "https://proofs-api.zerolabs.green/api/partners/filecoin/purchases/c6924a11-0cc8-43f7-8fbf-00cd6fb0032a",
		"downloadUrl": "https://proofs-api.zerolabs.green/api/files/bd3720bc-3b74-4cf2-8080-1d42a8223c76",
		"sellerId": "8c0a45ce-1594-4107-baf0-ce8846b34afd",
		"reportingStart": "2021-04-01T00:00:00.000Z",
		"reportingStartTimezoneOffset": 120,
		"reportingEnd": "2021-04-30T23:59:59.999Z",
		"reportingEndTimezoneOffset": 120,
		"txHash": "0x800afa3255591b695d205e45a71289e701366c8517eb071dd6b4621a5c403ebd",
		"buyerId": "93e399fb-991d-4f86-a315-4a1df8d18aee",
		"contractId": "b23d20c8-f8d9-42ea-bcc6-935f1e00ad85",
		"createdAt": "2022-06-10T08:45:40.741Z",
		"updatedAt": "2022-06-10T08:45:44.389Z",
		"recsSoldWh": "15000000",
		"reportingStartLocal": "2021-04-01T02:00:00.000+02:00",
		"reportingEndLocal": "2021-05-01T01:59:59.999+02:00",
		"generation": {
			"id": "1021bf0c-2c00-494d-b7b1-cf4068c8c112",
			"energyWh": 15000000,
			"generatorName": "Unknown",
			"generatorId": "Unknown",
			"region": "",
			"country": "BE",
			"productType": "GO",
			"energySource": "WIND",
			"generationStart": "2021-04-30T00:00:00.000Z",
			"generationStartTimezoneOffset": 120,
			"generationEnd": "2021-04-30T23:59:59.999Z",
			"generationEndTimezoneOffset": 120,
			"txHash": "0x7502a53627a24d0cb7b327ec43d9a5606219c6c3443ecec81046ea4f03638553",
			"initialSellerId": "8c0a45ce-1594-4107-baf0-ce8846b34afd",
			"redemptionDate": null,
			"nameplateCapacityW": null,
			"commissioningDate": null,
			"commissioningDateTimezoneOffset": null,
			"label": null,
			"certificateCid": "bafyreidv424wroqs3ixks55amz2zbmczcaaim6jyly34y3an7skmr2vmfa",
			"batchId": "829",
			"onchainId": "853",
			"createdAt": "2022-06-08T21:02:33.411Z",
			"updatedAt": "2022-06-10T05:32:00.329Z",
			"generationStartLocal": "2021-04-30T02:00:00.000+02:00",
			"generationEndLocal": "2021-05-01T01:59:59.999+02:00"
		}
	}, {
		"id": "4c1ba652-2da6-4a6f-a347-b6ac1b54cc54",
		"pageUrl": "https://proofs.zerolabs.green/partners/filecoin/purchases/4c1ba652-2da6-4a6f-a347-b6ac1b54cc54",
		"dataUrl": "https://proofs-api.zerolabs.green/api/partners/filecoin/purchases/4c1ba652-2da6-4a6f-a347-b6ac1b54cc54",
		"downloadUrl": "https://proofs-api.zerolabs.green/api/files/bd3720bc-3b74-4cf2-8080-1d42a8223c76",
		"sellerId": "8c0a45ce-1594-4107-baf0-ce8846b34afd",
		"reportingStart": "2021-02-01T00:00:00.000Z",
		"reportingStartTimezoneOffset": 120,
		"reportingEnd": "2021-02-28T23:59:59.999Z",
		"reportingEndTimezoneOffset": 120,
		"txHash": "0x4264c093df9a47b98f8997fe703257dfa38d8dcb8d884b4fdd6c021af0870abb",
		"buyerId": "93e399fb-991d-4f86-a315-4a1df8d18aee",
		"contractId": "1c40d9d7-5be9-49c5-afac-027f41b97b63",
		"createdAt": "2022-06-10T08:48:49.097Z",
		"updatedAt": "2022-06-10T08:48:52.529Z",
		"recsSoldWh": "12000000",
		"reportingStartLocal": "2021-02-01T02:00:00.000+02:00",
		"reportingEndLocal": "2021-03-01T01:59:59.999+02:00",
		"generation": {
			"id": "a724feb5-e5ed-4d0c-a662-ca125e28cbf3",
			"energyWh": 12000000,
			"generatorName": "Unknown",
			"generatorId": "Unknown",
			"region": "",
			"country": "BE",
			"productType": "GO",
			"energySource": "WIND",
			"generationStart": "2021-02-28T00:00:00.000Z",
			"generationStartTimezoneOffset": 60,
			"generationEnd": "2021-02-28T23:59:59.999Z",
			"generationEndTimezoneOffset": 60,
			"txHash": "0x75d70a4e03667f797ac71180b0f06fb0e5dae84f2734b19b4f31eff8157961f5",
			"initialSellerId": "8c0a45ce-1594-4107-baf0-ce8846b34afd",
			"redemptionDate": null,
			"nameplateCapacityW": null,
			"commissioningDate": null,
			"commissioningDateTimezoneOffset": null,
			"label": null,
			"certificateCid": "bafyreignnexcvvvbkahfey4cui7mvgjaua36f35pushgi3qfqe2bltjgv4",
			"batchId": "829",
			"onchainId": "850",
			"createdAt": "2022-06-08T21:02:33.361Z",
			"updatedAt": "2022-06-10T05:30:55.150Z",
			"generationStartLocal": "2021-02-28T01:00:00.000+01:00",
			"generationEndLocal": "2021-03-01T00:59:59.999+01:00"
		}
	}, {
		"id": "55bde415-0341-4dd0-af78-9b79dbb052f3",
		"pageUrl": "https://proofs.zerolabs.green/partners/filecoin/purchases/55bde415-0341-4dd0-af78-9b79dbb052f3",
		"dataUrl": "https://proofs-api.zerolabs.green/api/partners/filecoin/purchases/55bde415-0341-4dd0-af78-9b79dbb052f3",
		"downloadUrl": "https://proofs-api.zerolabs.green/api/files/bd3720bc-3b74-4cf2-8080-1d42a8223c76",
		"sellerId": "8c0a45ce-1594-4107-baf0-ce8846b34afd",
		"reportingStart": "2021-06-01T00:00:00.000Z",
		"reportingStartTimezoneOffset": 120,
		"reportingEnd": "2021-06-30T23:59:59.999Z",
		"reportingEndTimezoneOffset": 120,
		"txHash": "0xbacfc708994d103a3e311aa248aa3a9ef8a5e056bd91ae4aa2b0a479ec52dde5",
		"buyerId": "93e399fb-991d-4f86-a315-4a1df8d18aee",
		"contractId": "6d3362b0-2c13-4232-a6e0-d6ad2bfe97e9",
		"createdAt": "2022-06-10T08:46:14.798Z",
		"updatedAt": "2022-06-10T08:46:18.305Z",
		"recsSoldWh": "18000000",
		"reportingStartLocal": "2021-06-01T02:00:00.000+02:00",
		"reportingEndLocal": "2021-07-01T01:59:59.999+02:00",
		"generation": {
			"id": "ae702dd3-7fd1-4cc1-aa98-0192c97b1388",
			"energyWh": 18000000,
			"generatorName": "Unknown",
			"generatorId": "Unknown",
			"region": "",
			"country": "BE",
			"productType": "GO",
			"energySource": "WIND",
			"generationStart": "2021-06-30T00:00:00.000Z",
			"generationStartTimezoneOffset": 120,
			"generationEnd": "2021-06-30T23:59:59.999Z",
			"generationEndTimezoneOffset": 120,
			"txHash": "0x9f04ecc98180e532edf3736f2e1bf4a61153a9e8221016a49850f33247e017b4",
			"initialSellerId": "8c0a45ce-1594-4107-baf0-ce8846b34afd",
			"redemptionDate": null,
			"nameplateCapacityW": null,
			"commissioningDate": null,
			"commissioningDateTimezoneOffset": null,
			"label": null,
			"certificateCid": "bafyreiggdddr2n3muizercqbysxvg7czowwapry6fsunqtcpgvww56gpvm",
			"batchId": "829",
			"onchainId": "855",
			"createdAt": "2022-06-08T21:02:33.461Z",
			"updatedAt": "2022-06-10T05:32:42.011Z",
			"generationStartLocal": "2021-06-30T02:00:00.000+02:00",
			"generationEndLocal": "2021-07-01T01:59:59.999+02:00"
		}
	}, {
		"id": "9ca13ef5-c56d-429d-a949-14c62b43b698",
		"pageUrl": "https://proofs.zerolabs.green/partners/filecoin/purchases/9ca13ef5-c56d-429d-a949-14c62b43b698",
		"dataUrl": "https://proofs-api.zerolabs.green/api/partners/filecoin/purchases/9ca13ef5-c56d-429d-a949-14c62b43b698",
		"downloadUrl": "https://proofs-api.zerolabs.green/api/files/bd3720bc-3b74-4cf2-8080-1d42a8223c76",
		"sellerId": "8c0a45ce-1594-4107-baf0-ce8846b34afd",
		"reportingStart": "2020-07-01T00:00:00.000Z",
		"reportingStartTimezoneOffset": 120,
		"reportingEnd": "2021-03-31T23:59:59.999Z",
		"reportingEndTimezoneOffset": 120,
		"txHash": "0x14e6b3369372e686d5a24a861ce0db856bdff0bec4a18aee002fda93c95e2e66",
		"buyerId": "93e399fb-991d-4f86-a315-4a1df8d18aee",
		"contractId": "36e490c4-ab97-406f-8542-8f844abbffab",
		"createdAt": "2022-06-10T09:29:46.672Z",
		"updatedAt": "2022-06-10T09:29:50.370Z",
		"recsSoldWh": "1000000",
		"reportingStartLocal": "2020-07-01T02:00:00.000+02:00",
		"reportingEndLocal": "2021-04-01T01:59:59.999+02:00",
		"generation": {
			"id": "8bb185c8-4e8b-4216-97b8-6ca9a3659f77",
			"energyWh": 8000000,
			"generatorName": "Unknown",
			"generatorId": "Unknown",
			"region": "",
			"country": "BE",
			"productType": "GO",
			"energySource": "WIND",
			"generationStart": "2021-01-31T00:00:00.000Z",
			"generationStartTimezoneOffset": 60,
			"generationEnd": "2021-01-31T23:59:59.999Z",
			"generationEndTimezoneOffset": 60,
			"txHash": "0xec9eb272a15b09d430024ec57317a6dc4830e51a5b93467066f23f96c66dff18",
			"initialSellerId": "8c0a45ce-1594-4107-baf0-ce8846b34afd",
			"redemptionDate": null,
			"nameplateCapacityW": null,
			"commissioningDate": null,
			"commissioningDateTimezoneOffset": null,
			"label": null,
			"certificateCid": "bafyreigvwzcyknenclgli7h53rokkdahkzow5rapicha4cbkotqcrucgve",
			"batchId": "829",
			"onchainId": "849",
			"createdAt": "2022-06-08T21:02:33.347Z",
			"updatedAt": "2022-06-10T05:30:31.653Z",
			"generationStartLocal": "2021-01-31T01:00:00.000+01:00",
			"generationEndLocal": "2021-02-01T00:59:59.999+01:00"
		}
	}, {
		"id": "c741a752-bb73-454f-8283-dc736054bda3",
		"pageUrl": "https://proofs.zerolabs.green/partners/filecoin/purchases/c741a752-bb73-454f-8283-dc736054bda3",
		"dataUrl": "https://proofs-api.zerolabs.green/api/partners/filecoin/purchases/c741a752-bb73-454f-8283-dc736054bda3",
		"downloadUrl": "https://proofs-api.zerolabs.green/api/files/bd3720bc-3b74-4cf2-8080-1d42a8223c76",
		"sellerId": "8c0a45ce-1594-4107-baf0-ce8846b34afd",
		"reportingStart": "2021-01-01T00:00:00.000Z",
		"reportingStartTimezoneOffset": 120,
		"reportingEnd": "2021-01-31T23:59:59.999Z",
		"reportingEndTimezoneOffset": 120,
		"txHash": "0x6b64231889c54edbf05e3424dea9e05c30f0a8a0a2cd7c857148e66d1ed5c203",
		"buyerId": "93e399fb-991d-4f86-a315-4a1df8d18aee",
		"contractId": "87b80f60-e8f5-4280-8da9-778570bcb0aa",
		"createdAt": "2022-06-10T09:33:33.190Z",
		"updatedAt": "2022-06-10T09:33:36.706Z",
		"recsSoldWh": "3000000",
		"reportingStartLocal": "2021-01-01T02:00:00.000+02:00",
		"reportingEndLocal": "2021-02-01T01:59:59.999+02:00",
		"generation": {
			"id": "8bb185c8-4e8b-4216-97b8-6ca9a3659f77",
			"energyWh": 8000000,
			"generatorName": "Unknown",
			"generatorId": "Unknown",
			"region": "",
			"country": "BE",
			"productType": "GO",
			"energySource": "WIND",
			"generationStart": "2021-01-31T00:00:00.000Z",
			"generationStartTimezoneOffset": 60,
			"generationEnd": "2021-01-31T23:59:59.999Z",
			"generationEndTimezoneOffset": 60,
			"txHash": "0xec9eb272a15b09d430024ec57317a6dc4830e51a5b93467066f23f96c66dff18",
			"initialSellerId": "8c0a45ce-1594-4107-baf0-ce8846b34afd",
			"redemptionDate": null,
			"nameplateCapacityW": null,
			"commissioningDate": null,
			"commissioningDateTimezoneOffset": null,
			"label": null,
			"certificateCid": "bafyreigvwzcyknenclgli7h53rokkdahkzow5rapicha4cbkotqcrucgve",
			"batchId": "829",
			"onchainId": "849",
			"createdAt": "2022-06-08T21:02:33.347Z",
			"updatedAt": "2022-06-10T05:30:31.653Z",
			"generationStartLocal": "2021-01-31T01:00:00.000+01:00",
			"generationEndLocal": "2021-02-01T00:59:59.999+01:00"
		}
	}, {
		"id": "6986b620-2764-48ce-b8c2-00d8d09a96e8",
		"pageUrl": "https://proofs.zerolabs.green/partners/filecoin/purchases/6986b620-2764-48ce-b8c2-00d8d09a96e8",
		"dataUrl": "https://proofs-api.zerolabs.green/api/partners/filecoin/purchases/6986b620-2764-48ce-b8c2-00d8d09a96e8",
		"downloadUrl": "https://proofs-api.zerolabs.green/api/files/bd3720bc-3b74-4cf2-8080-1d42a8223c76",
		"sellerId": "8c0a45ce-1594-4107-baf0-ce8846b34afd",
		"reportingStart": "2020-07-01T00:00:00.000Z",
		"reportingStartTimezoneOffset": 120,
		"reportingEnd": "2021-03-31T23:59:59.999Z",
		"reportingEndTimezoneOffset": 120,
		"txHash": "0x7658c40dc965493af4a8e5a434c65957b89d5516f6cfc1a60bc3035a9721ec73",
		"buyerId": "93e399fb-991d-4f86-a315-4a1df8d18aee",
		"contractId": "2400edf3-8f69-4fe9-8f7f-072af5f1981e",
		"createdAt": "2022-06-10T09:30:03.304Z",
		"updatedAt": "2022-06-10T09:30:07.031Z",
		"recsSoldWh": "1000000",
		"reportingStartLocal": "2020-07-01T02:00:00.000+02:00",
		"reportingEndLocal": "2021-04-01T01:59:59.999+02:00",
		"generation": {
			"id": "8bb185c8-4e8b-4216-97b8-6ca9a3659f77",
			"energyWh": 8000000,
			"generatorName": "Unknown",
			"generatorId": "Unknown",
			"region": "",
			"country": "BE",
			"productType": "GO",
			"energySource": "WIND",
			"generationStart": "2021-01-31T00:00:00.000Z",
			"generationStartTimezoneOffset": 60,
			"generationEnd": "2021-01-31T23:59:59.999Z",
			"generationEndTimezoneOffset": 60,
			"txHash": "0xec9eb272a15b09d430024ec57317a6dc4830e51a5b93467066f23f96c66dff18",
			"initialSellerId": "8c0a45ce-1594-4107-baf0-ce8846b34afd",
			"redemptionDate": null,
			"nameplateCapacityW": null,
			"commissioningDate": null,
			"commissioningDateTimezoneOffset": null,
			"label": null,
			"certificateCid": "bafyreigvwzcyknenclgli7h53rokkdahkzow5rapicha4cbkotqcrucgve",
			"batchId": "829",
			"onchainId": "849",
			"createdAt": "2022-06-08T21:02:33.347Z",
			"updatedAt": "2022-06-10T05:30:31.653Z",
			"generationStartLocal": "2021-01-31T01:00:00.000+01:00",
			"generationEndLocal": "2021-02-01T00:59:59.999+01:00"
		}
	}, {
		"id": "79d8dfed-35ca-48f8-b588-d1368eceddac",
		"pageUrl": "https://proofs.zerolabs.green/partners/filecoin/purchases/79d8dfed-35ca-48f8-b588-d1368eceddac",
		"dataUrl": "https://proofs-api.zerolabs.green/api/partners/filecoin/purchases/79d8dfed-35ca-48f8-b588-d1368eceddac",
		"downloadUrl": "https://proofs-api.zerolabs.green/api/files/bd3720bc-3b74-4cf2-8080-1d42a8223c76",
		"sellerId": "8c0a45ce-1594-4107-baf0-ce8846b34afd",
		"reportingStart": "2020-07-01T00:00:00.000Z",
		"reportingStartTimezoneOffset": 120,
		"reportingEnd": "2021-03-31T23:59:59.999Z",
		"reportingEndTimezoneOffset": 120,
		"txHash": "0xabb1ce125d0b2334edb84f02844b072c2a9126fdcfeaffb785d054cc6e31215d",
		"buyerId": "93e399fb-991d-4f86-a315-4a1df8d18aee",
		"contractId": "e2e8558c-2316-4631-91f1-10c659a191a2",
		"createdAt": "2022-06-10T09:30:25.554Z",
		"updatedAt": "2022-06-10T09:30:29.175Z",
		"recsSoldWh": "1000000",
		"reportingStartLocal": "2020-07-01T02:00:00.000+02:00",
		"reportingEndLocal": "2021-04-01T01:59:59.999+02:00",
		"generation": {
			"id": "8bb185c8-4e8b-4216-97b8-6ca9a3659f77",
			"energyWh": 8000000,
			"generatorName": "Unknown",
			"generatorId": "Unknown",
			"region": "",
			"country": "BE",
			"productType": "GO",
			"energySource": "WIND",
			"generationStart": "2021-01-31T00:00:00.000Z",
			"generationStartTimezoneOffset": 60,
			"generationEnd": "2021-01-31T23:59:59.999Z",
			"generationEndTimezoneOffset": 60,
			"txHash": "0xec9eb272a15b09d430024ec57317a6dc4830e51a5b93467066f23f96c66dff18",
			"initialSellerId": "8c0a45ce-1594-4107-baf0-ce8846b34afd",
			"redemptionDate": null,
			"nameplateCapacityW": null,
			"commissioningDate": null,
			"commissioningDateTimezoneOffset": null,
			"label": null,
			"certificateCid": "bafyreigvwzcyknenclgli7h53rokkdahkzow5rapicha4cbkotqcrucgve",
			"batchId": "829",
			"onchainId": "849",
			"createdAt": "2022-06-08T21:02:33.347Z",
			"updatedAt": "2022-06-10T05:30:31.653Z",
			"generationStartLocal": "2021-01-31T01:00:00.000+01:00",
			"generationEndLocal": "2021-02-01T00:59:59.999+01:00"
		}
	}]
}
```
{% endswagger-response %}
{% endswagger %}

## Contracts

Listing all contracts for specified Filecoin Storage Provider.

{% swagger method="get" path="" baseUrl="https://proofs-api.zerolabs.green/api/partners/filecoin/nodes/{minerID}/contracts" summary="" %}
{% swagger-description %}
Listing all contracts for specified Filecoin Storage Provider.
{% endswagger-description %}

{% swagger-parameter in="path" name="minerID*" type=" " %}
Miner Id (e.g. f01234)
{% endswagger-parameter %}

{% swagger-response status="200: OK" description="JSON response" %}
```javascript
{
  "id": "f01234",
  "buyerId": "93e399fb-991d-4f86-a315-4a1df8d18aee",
  "blockchainAddress": null,
  "createdAt": "2022-02-07T15:52:00.419Z",
  "updatedAt": "2022-02-07T15:52:00.419Z",
  "contracts": [
    {
      "id": "57ddb1b2-51e9-4f49-b8dd-b722c9a028dd",
      "productType": "GO",
      "energySources": [
        "WIND",
        "SOLAR"
      ],
      "contractDate": "2021-11-15T00:00:00.000Z",
      "deliveryDate": "2022-04-15T00:00:00.000Z",
      "reportingStart": "2021-07-01T00:00:00.000Z",
      "reportingEnd": "2021-07-31T23:59:59.999Z",
      "buyer": {
        "id": "93e399fb-991d-4f86-a315-4a1df8d18aee",
        "name": "Buyer 3",
        "blockchainAddress": null,
        "createdAt": "2022-02-07T15:52:00.419Z",
        "updatedAt": "2022-02-07T15:52:00.419Z"
      },
      "seller": {
        "id": "8c0a45ce-1594-4107-baf0-ce8846b34afd",
        "name": "3Degrees Group, Inc",
        "addressLine1": "235 Montgomery St Suite 320 CA94104 San Francisco US",
        "addressLine2": "",
        "contactPerson": "-",
        "blockchainAddress": null,
        "createdAt": "2022-02-07T15:52:00.419Z",
        "updatedAt": "2022-02-07T15:52:00.419Z"
      },
      "openVolume": "32000000",
      "deliveredVolume": "0",
      "purchases": [],
      "timezoneOffset": 120,
      "filecoinNode": {
        "id": "f01234",
        "buyerId": "93e399fb-991d-4f86-a315-4a1df8d18aee",
        "blockchainAddress": null,
        "createdAt": "2022-02-07T15:52:00.419Z",
        "updatedAt": "2022-02-07T15:52:00.419Z"
      },
      "externalId": null,
      "label": null,
      "createdAt": "2022-05-10T10:09:55.929Z",
      "updatedAt": "2022-05-10T10:09:55.929Z",
      "countryRegionMap": [
        {
          "country": "BE",
          "region": ""
        }
      ],
      "pageUrl": "https://proofs.zerolabs.green/partners/filecoin/contracts/57ddb1b2-51e9-4f49-b8dd-b722c9a028dd",
      "dataUrl": "https://proofs-api.zerolabs.green/api/partners/filecoin/contracts/57ddb1b2-51e9-4f49-b8dd-b722c9a028dd"
    },
    {
      "id": "e51bd084-cdcd-4a2a-b095-b1787de6e12e",
      "productType": "GO",
      "energySources": [
        "WIND",
        "SOLAR"
      ],
      "contractDate": "2021-11-15T00:00:00.000Z",
      "deliveryDate": "2022-04-15T00:00:00.000Z",
      "reportingStart": "2021-08-01T00:00:00.000Z",
      "reportingEnd": "2021-08-31T23:59:59.999Z",
      "buyer": {
        "id": "93e399fb-991d-4f86-a315-4a1df8d18aee",
        "name": "Buyer 3",
        "blockchainAddress": null,
        "createdAt": "2022-02-07T15:52:00.419Z",
        "updatedAt": "2022-02-07T15:52:00.419Z"
      },
      "seller": {
        "id": "8c0a45ce-1594-4107-baf0-ce8846b34afd",
        "name": "3Degrees Group, Inc",
        "addressLine1": "235 Montgomery St Suite 320 CA94104 San Francisco US",
        "addressLine2": "",
        "contactPerson": "-",
        "blockchainAddress": null,
        "createdAt": "2022-02-07T15:52:00.419Z",
        "updatedAt": "2022-02-07T15:52:00.419Z"
      },
      "openVolume": "31000000",
      "deliveredVolume": "0",
      "purchases": [],
      "timezoneOffset": 120,
      "filecoinNode": {
        "id": "f01234",
        "buyerId": "93e399fb-991d-4f86-a315-4a1df8d18aee",
        "blockchainAddress": null,
        "createdAt": "2022-02-07T15:52:00.419Z",
        "updatedAt": "2022-02-07T15:52:00.419Z"
      },
      "externalId": null,
      "label": null,
      "createdAt": "2022-05-10T10:09:55.944Z",
      "updatedAt": "2022-05-10T10:09:55.944Z",
      "countryRegionMap": [
        {
          "country": "BE",
          "region": ""
        }
      ],
      "pageUrl": "https://proofs.zerolabs.green/partners/filecoin/contracts/e51bd084-cdcd-4a2a-b095-b1787de6e12e",
      "dataUrl": "https://proofs-api.zerolabs.green/api/partners/filecoin/contracts/e51bd084-cdcd-4a2a-b095-b1787de6e12e"
    },
    {
      "id": "b23d20c8-f8d9-42ea-bcc6-935f1e00ad85",
      "productType": "GO",
      "energySources": [
        "WIND",
        "SOLAR"
      ],
      "contractDate": "2021-11-15T00:00:00.000Z",
      "deliveryDate": "2022-04-15T00:00:00.000Z",
      "reportingStart": "2021-04-01T00:00:00.000Z",
      "reportingEnd": "2021-04-30T23:59:59.999Z",
      "buyer": {
        "id": "93e399fb-991d-4f86-a315-4a1df8d18aee",
        "name": "Buyer 3",
        "blockchainAddress": null,
        "createdAt": "2022-02-07T15:52:00.419Z",
        "updatedAt": "2022-02-07T15:52:00.419Z"
      },
      "seller": {
        "id": "8c0a45ce-1594-4107-baf0-ce8846b34afd",
        "name": "3Degrees Group, Inc",
        "addressLine1": "235 Montgomery St Suite 320 CA94104 San Francisco US",
        "addressLine2": "",
        "contactPerson": "-",
        "blockchainAddress": null,
        "createdAt": "2022-02-07T15:52:00.419Z",
        "updatedAt": "2022-02-07T15:52:00.419Z"
      },
      "openVolume": "15000000",
      "deliveredVolume": "0",
      "purchases": [],
      "timezoneOffset": 120,
      "filecoinNode": {
        "id": "f01234",
        "buyerId": "93e399fb-991d-4f86-a315-4a1df8d18aee",
        "blockchainAddress": null,
        "createdAt": "2022-02-07T15:52:00.419Z",
        "updatedAt": "2022-02-07T15:52:00.419Z"
      },
      "externalId": null,
      "label": null,
      "createdAt": "2022-05-10T10:09:56.152Z",
      "updatedAt": "2022-05-10T10:09:56.152Z",
      "countryRegionMap": [
        {
          "country": "BE",
          "region": ""
        }
      ],
      "pageUrl": "https://proofs.zerolabs.green/partners/filecoin/contracts/b23d20c8-f8d9-42ea-bcc6-935f1e00ad85",
      "dataUrl": "https://proofs-api.zerolabs.green/api/partners/filecoin/contracts/b23d20c8-f8d9-42ea-bcc6-935f1e00ad85"
    },
    {
      "id": "b0da09da-50af-4ab8-ba23-a809d3165ff8",
      "productType": "GO",
      "energySources": [
        "WIND",
        "SOLAR"
      ],
      "contractDate": "2021-11-15T00:00:00.000Z",
      "deliveryDate": "2022-04-15T00:00:00.000Z",
      "reportingStart": "2021-05-01T00:00:00.000Z",
      "reportingEnd": "2021-05-31T23:59:59.999Z",
      "buyer": {
        "id": "93e399fb-991d-4f86-a315-4a1df8d18aee",
        "name": "Buyer 3",
        "blockchainAddress": null,
        "createdAt": "2022-02-07T15:52:00.419Z",
        "updatedAt": "2022-02-07T15:52:00.419Z"
      },
      "seller": {
        "id": "8c0a45ce-1594-4107-baf0-ce8846b34afd",
        "name": "3Degrees Group, Inc",
        "addressLine1": "235 Montgomery St Suite 320 CA94104 San Francisco US",
        "addressLine2": "",
        "contactPerson": "-",
        "blockchainAddress": null,
        "createdAt": "2022-02-07T15:52:00.419Z",
        "updatedAt": "2022-02-07T15:52:00.419Z"
      },
      "openVolume": "26000000",
      "deliveredVolume": "0",
      "purchases": [],
      "timezoneOffset": 120,
      "filecoinNode": {
        "id": "f01234",
        "buyerId": "93e399fb-991d-4f86-a315-4a1df8d18aee",
        "blockchainAddress": null,
        "createdAt": "2022-02-07T15:52:00.419Z",
        "updatedAt": "2022-02-07T15:52:00.419Z"
      },
      "externalId": null,
      "label": null,
      "createdAt": "2022-05-10T10:09:56.170Z",
      "updatedAt": "2022-05-10T10:09:56.170Z",
      "countryRegionMap": [
        {
          "country": "BE",
          "region": ""
        }
      ],
      "pageUrl": "https://proofs.zerolabs.green/partners/filecoin/contracts/b0da09da-50af-4ab8-ba23-a809d3165ff8",
      "dataUrl": "https://proofs-api.zerolabs.green/api/partners/filecoin/contracts/b0da09da-50af-4ab8-ba23-a809d3165ff8"
    },
    {
      "id": "6d3362b0-2c13-4232-a6e0-d6ad2bfe97e9",
      "productType": "GO",
      "energySources": [
        "WIND",
        "SOLAR"
      ],
      "contractDate": "2021-11-15T00:00:00.000Z",
      "deliveryDate": "2022-04-15T00:00:00.000Z",
      "reportingStart": "2021-06-01T00:00:00.000Z",
      "reportingEnd": "2021-06-30T23:59:59.999Z",
      "buyer": {
        "id": "93e399fb-991d-4f86-a315-4a1df8d18aee",
        "name": "Buyer 3",
        "blockchainAddress": null,
        "createdAt": "2022-02-07T15:52:00.419Z",
        "updatedAt": "2022-02-07T15:52:00.419Z"
      },
      "seller": {
        "id": "8c0a45ce-1594-4107-baf0-ce8846b34afd",
        "name": "3Degrees Group, Inc",
        "addressLine1": "235 Montgomery St Suite 320 CA94104 San Francisco US",
        "addressLine2": "",
        "contactPerson": "-",
        "blockchainAddress": null,
        "createdAt": "2022-02-07T15:52:00.419Z",
        "updatedAt": "2022-02-07T15:52:00.419Z"
      },
      "openVolume": "18000000",
      "deliveredVolume": "0",
      "purchases": [],
      "timezoneOffset": 120,
      "filecoinNode": {
        "id": "f01234",
        "buyerId": "93e399fb-991d-4f86-a315-4a1df8d18aee",
        "blockchainAddress": null,
        "createdAt": "2022-02-07T15:52:00.419Z",
        "updatedAt": "2022-02-07T15:52:00.419Z"
      },
      "externalId": null,
      "label": null,
      "createdAt": "2022-05-10T10:09:56.185Z",
      "updatedAt": "2022-05-10T10:09:56.185Z",
      "countryRegionMap": [
        {
          "country": "BE",
          "region": ""
        }
      ],
      "pageUrl": "https://proofs.zerolabs.green/partners/filecoin/contracts/6d3362b0-2c13-4232-a6e0-d6ad2bfe97e9",
      "dataUrl": "https://proofs-api.zerolabs.green/api/partners/filecoin/contracts/6d3362b0-2c13-4232-a6e0-d6ad2bfe97e9"
    },
    {
      "id": "c6a7c25c-9a1f-48a3-9cb7-5b607ab157f0",
      "productType": "GO",
      "energySources": [
        "WIND",
        "SOLAR"
      ],
      "contractDate": "2021-11-15T00:00:00.000Z",
      "deliveryDate": "2022-04-15T00:00:00.000Z",
      "reportingStart": "2020-07-01T00:00:00.000Z",
      "reportingEnd": "2021-03-31T23:59:59.999Z",
      "buyer": {
        "id": "93e399fb-991d-4f86-a315-4a1df8d18aee",
        "name": "Buyer 3",
        "blockchainAddress": null,
        "createdAt": "2022-02-07T15:52:00.419Z",
        "updatedAt": "2022-02-07T15:52:00.419Z"
      },
      "seller": {
        "id": "8c0a45ce-1594-4107-baf0-ce8846b34afd",
        "name": "3Degrees Group, Inc",
        "addressLine1": "235 Montgomery St Suite 320 CA94104 San Francisco US",
        "addressLine2": "",
        "contactPerson": "-",
        "blockchainAddress": null,
        "createdAt": "2022-02-07T15:52:00.419Z",
        "updatedAt": "2022-02-07T15:52:00.419Z"
      },
      "openVolume": "2000000",
      "deliveredVolume": "0",
      "purchases": [],
      "timezoneOffset": 120,
      "filecoinNode": {
        "id": "f01234",
        "buyerId": "93e399fb-991d-4f86-a315-4a1df8d18aee",
        "blockchainAddress": null,
        "createdAt": "2022-02-07T15:52:00.419Z",
        "updatedAt": "2022-02-07T15:52:00.419Z"
      },
      "externalId": null,
      "label": null,
      "createdAt": "2022-05-10T10:09:56.214Z",
      "updatedAt": "2022-05-10T10:09:56.214Z",
      "countryRegionMap": [
        {
          "country": "BE",
          "region": ""
        }
      ],
      "pageUrl": "https://proofs.zerolabs.green/partners/filecoin/contracts/c6a7c25c-9a1f-48a3-9cb7-5b607ab157f0",
      "dataUrl": "https://proofs-api.zerolabs.green/api/partners/filecoin/contracts/c6a7c25c-9a1f-48a3-9cb7-5b607ab157f0"
    },
    {
      "id": "36e490c4-ab97-406f-8542-8f844abbffab",
      "productType": "GO",
      "energySources": [
        "WIND",
        "SOLAR"
      ],
      "contractDate": "2021-11-15T00:00:00.000Z",
      "deliveryDate": "2022-04-15T00:00:00.000Z",
      "reportingStart": "2020-07-01T00:00:00.000Z",
      "reportingEnd": "2021-03-31T23:59:59.999Z",
      "buyer": {
        "id": "93e399fb-991d-4f86-a315-4a1df8d18aee",
        "name": "Buyer 3",
        "blockchainAddress": null,
        "createdAt": "2022-02-07T15:52:00.419Z",
        "updatedAt": "2022-02-07T15:52:00.419Z"
      },
      "seller": {
        "id": "8c0a45ce-1594-4107-baf0-ce8846b34afd",
        "name": "3Degrees Group, Inc",
        "addressLine1": "235 Montgomery St Suite 320 CA94104 San Francisco US",
        "addressLine2": "",
        "contactPerson": "-",
        "blockchainAddress": null,
        "createdAt": "2022-02-07T15:52:00.419Z",
        "updatedAt": "2022-02-07T15:52:00.419Z"
      },
      "openVolume": "1000000",
      "deliveredVolume": "0",
      "purchases": [],
      "timezoneOffset": 120,
      "filecoinNode": {
        "id": "f01234",
        "buyerId": "93e399fb-991d-4f86-a315-4a1df8d18aee",
        "blockchainAddress": null,
        "createdAt": "2022-02-07T15:52:00.419Z",
        "updatedAt": "2022-02-07T15:52:00.419Z"
      },
      "externalId": null,
      "label": null,
      "createdAt": "2022-05-10T10:09:56.231Z",
      "updatedAt": "2022-05-10T10:09:56.231Z",
      "countryRegionMap": [
        {
          "country": "BE",
          "region": ""
        }
      ],
      "pageUrl": "https://proofs.zerolabs.green/partners/filecoin/contracts/36e490c4-ab97-406f-8542-8f844abbffab",
      "dataUrl": "https://proofs-api.zerolabs.green/api/partners/filecoin/contracts/36e490c4-ab97-406f-8542-8f844abbffab"
    },
    {
      "id": "2400edf3-8f69-4fe9-8f7f-072af5f1981e",
      "productType": "GO",
      "energySources": [
        "WIND",
        "SOLAR"
      ],
      "contractDate": "2021-11-15T00:00:00.000Z",
      "deliveryDate": "2022-04-15T00:00:00.000Z",
      "reportingStart": "2020-07-01T00:00:00.000Z",
      "reportingEnd": "2021-03-31T23:59:59.999Z",
      "buyer": {
        "id": "93e399fb-991d-4f86-a315-4a1df8d18aee",
        "name": "Buyer 3",
        "blockchainAddress": null,
        "createdAt": "2022-02-07T15:52:00.419Z",
        "updatedAt": "2022-02-07T15:52:00.419Z"
      },
      "seller": {
        "id": "8c0a45ce-1594-4107-baf0-ce8846b34afd",
        "name": "3Degrees Group, Inc",
        "addressLine1": "235 Montgomery St Suite 320 CA94104 San Francisco US",
        "addressLine2": "",
        "contactPerson": "-",
        "blockchainAddress": null,
        "createdAt": "2022-02-07T15:52:00.419Z",
        "updatedAt": "2022-02-07T15:52:00.419Z"
      },
      "openVolume": "1000000",
      "deliveredVolume": "0",
      "purchases": [],
      "timezoneOffset": 120,
      "filecoinNode": {
        "id": "f01234",
        "buyerId": "93e399fb-991d-4f86-a315-4a1df8d18aee",
        "blockchainAddress": null,
        "createdAt": "2022-02-07T15:52:00.419Z",
        "updatedAt": "2022-02-07T15:52:00.419Z"
      },
      "externalId": null,
      "label": null,
      "createdAt": "2022-05-10T10:09:56.247Z",
      "updatedAt": "2022-05-10T10:09:56.247Z",
      "countryRegionMap": [
        {
          "country": "BE",
          "region": ""
        }
      ],
      "pageUrl": "https://proofs.zerolabs.green/partners/filecoin/contracts/2400edf3-8f69-4fe9-8f7f-072af5f1981e",
      "dataUrl": "https://proofs-api.zerolabs.green/api/partners/filecoin/contracts/2400edf3-8f69-4fe9-8f7f-072af5f1981e"
    },
    {
      "id": "e2e8558c-2316-4631-91f1-10c659a191a2",
      "productType": "GO",
      "energySources": [
        "WIND",
        "SOLAR"
      ],
      "contractDate": "2021-11-15T00:00:00.000Z",
      "deliveryDate": "2022-04-15T00:00:00.000Z",
      "reportingStart": "2020-07-01T00:00:00.000Z",
      "reportingEnd": "2021-03-31T23:59:59.999Z",
      "buyer": {
        "id": "93e399fb-991d-4f86-a315-4a1df8d18aee",
        "name": "Buyer 3",
        "blockchainAddress": null,
        "createdAt": "2022-02-07T15:52:00.419Z",
        "updatedAt": "2022-02-07T15:52:00.419Z"
      },
      "seller": {
        "id": "8c0a45ce-1594-4107-baf0-ce8846b34afd",
        "name": "3Degrees Group, Inc",
        "addressLine1": "235 Montgomery St Suite 320 CA94104 San Francisco US",
        "addressLine2": "",
        "contactPerson": "-",
        "blockchainAddress": null,
        "createdAt": "2022-02-07T15:52:00.419Z",
        "updatedAt": "2022-02-07T15:52:00.419Z"
      },
      "openVolume": "1000000",
      "deliveredVolume": "0",
      "purchases": [],
      "timezoneOffset": 120,
      "filecoinNode": {
        "id": "f01234",
        "buyerId": "93e399fb-991d-4f86-a315-4a1df8d18aee",
        "blockchainAddress": null,
        "createdAt": "2022-02-07T15:52:00.419Z",
        "updatedAt": "2022-02-07T15:52:00.419Z"
      },
      "externalId": null,
      "label": null,
      "createdAt": "2022-05-10T10:09:56.264Z",
      "updatedAt": "2022-05-10T10:09:56.264Z",
      "countryRegionMap": [
        {
          "country": "BE",
          "region": ""
        }
      ],
      "pageUrl": "https://proofs.zerolabs.green/partners/filecoin/contracts/e2e8558c-2316-4631-91f1-10c659a191a2",
      "dataUrl": "https://proofs-api.zerolabs.green/api/partners/filecoin/contracts/e2e8558c-2316-4631-91f1-10c659a191a2"
    },
    {
      "id": "87b80f60-e8f5-4280-8da9-778570bcb0aa",
      "productType": "GO",
      "energySources": [
        "WIND",
        "SOLAR"
      ],
      "contractDate": "2021-11-15T00:00:00.000Z",
      "deliveryDate": "2022-04-15T00:00:00.000Z",
      "reportingStart": "2021-01-01T00:00:00.000Z",
      "reportingEnd": "2021-01-31T23:59:59.999Z",
      "buyer": {
        "id": "93e399fb-991d-4f86-a315-4a1df8d18aee",
        "name": "Buyer 3",
        "blockchainAddress": null,
        "createdAt": "2022-02-07T15:52:00.419Z",
        "updatedAt": "2022-02-07T15:52:00.419Z"
      },
      "seller": {
        "id": "8c0a45ce-1594-4107-baf0-ce8846b34afd",
        "name": "3Degrees Group, Inc",
        "addressLine1": "235 Montgomery St Suite 320 CA94104 San Francisco US",
        "addressLine2": "",
        "contactPerson": "-",
        "blockchainAddress": null,
        "createdAt": "2022-02-07T15:52:00.419Z",
        "updatedAt": "2022-02-07T15:52:00.419Z"
      },
      "openVolume": "3000000",
      "deliveredVolume": "0",
      "purchases": [],
      "timezoneOffset": 120,
      "filecoinNode": {
        "id": "f01234",
        "buyerId": "93e399fb-991d-4f86-a315-4a1df8d18aee",
        "blockchainAddress": null,
        "createdAt": "2022-02-07T15:52:00.419Z",
        "updatedAt": "2022-02-07T15:52:00.419Z"
      },
      "externalId": null,
      "label": null,
      "createdAt": "2022-05-10T10:09:56.499Z",
      "updatedAt": "2022-05-10T10:09:56.499Z",
      "countryRegionMap": [
        {
          "country": "BE",
          "region": ""
        }
      ],
      "pageUrl": "https://proofs.zerolabs.green/partners/filecoin/contracts/87b80f60-e8f5-4280-8da9-778570bcb0aa",
      "dataUrl": "https://proofs-api.zerolabs.green/api/partners/filecoin/contracts/87b80f60-e8f5-4280-8da9-778570bcb0aa"
    },
    {
      "id": "1c40d9d7-5be9-49c5-afac-027f41b97b63",
      "productType": "GO",
      "energySources": [
        "WIND",
        "SOLAR"
      ],
      "contractDate": "2021-11-15T00:00:00.000Z",
      "deliveryDate": "2022-04-15T00:00:00.000Z",
      "reportingStart": "2021-02-01T00:00:00.000Z",
      "reportingEnd": "2021-02-28T23:59:59.999Z",
      "buyer": {
        "id": "93e399fb-991d-4f86-a315-4a1df8d18aee",
        "name": "Buyer 3",
        "blockchainAddress": null,
        "createdAt": "2022-02-07T15:52:00.419Z",
        "updatedAt": "2022-02-07T15:52:00.419Z"
      },
      "seller": {
        "id": "8c0a45ce-1594-4107-baf0-ce8846b34afd",
        "name": "3Degrees Group, Inc",
        "addressLine1": "235 Montgomery St Suite 320 CA94104 San Francisco US",
        "addressLine2": "",
        "contactPerson": "-",
        "blockchainAddress": null,
        "createdAt": "2022-02-07T15:52:00.419Z",
        "updatedAt": "2022-02-07T15:52:00.419Z"
      },
      "openVolume": "12000000",
      "deliveredVolume": "0",
      "purchases": [],
      "timezoneOffset": 120,
      "filecoinNode": {
        "id": "f01234",
        "buyerId": "93e399fb-991d-4f86-a315-4a1df8d18aee",
        "blockchainAddress": null,
        "createdAt": "2022-02-07T15:52:00.419Z",
        "updatedAt": "2022-02-07T15:52:00.419Z"
      },
      "externalId": null,
      "label": null,
      "createdAt": "2022-05-10T10:09:56.514Z",
      "updatedAt": "2022-05-10T10:09:56.514Z",
      "countryRegionMap": [
        {
          "country": "BE",
          "region": ""
        }
      ],
      "pageUrl": "https://proofs.zerolabs.green/partners/filecoin/contracts/1c40d9d7-5be9-49c5-afac-027f41b97b63",
      "dataUrl": "https://proofs-api.zerolabs.green/api/partners/filecoin/contracts/1c40d9d7-5be9-49c5-afac-027f41b97b63"
    },
    {
      "id": "bfcd046f-2f78-4652-b8fd-b1df27c64fd2",
      "productType": "GO",
      "energySources": [
        "WIND",
        "SOLAR"
      ],
      "contractDate": "2021-11-15T00:00:00.000Z",
      "deliveryDate": "2022-04-15T00:00:00.000Z",
      "reportingStart": "2021-03-01T00:00:00.000Z",
      "reportingEnd": "2021-03-31T23:59:59.999Z",
      "buyer": {
        "id": "93e399fb-991d-4f86-a315-4a1df8d18aee",
        "name": "Buyer 3",
        "blockchainAddress": null,
        "createdAt": "2022-02-07T15:52:00.419Z",
        "updatedAt": "2022-02-07T15:52:00.419Z"
      },
      "seller": {
        "id": "8c0a45ce-1594-4107-baf0-ce8846b34afd",
        "name": "3Degrees Group, Inc",
        "addressLine1": "235 Montgomery St Suite 320 CA94104 San Francisco US",
        "addressLine2": "",
        "contactPerson": "-",
        "blockchainAddress": null,
        "createdAt": "2022-02-07T15:52:00.419Z",
        "updatedAt": "2022-02-07T15:52:00.419Z"
      },
      "openVolume": "20000000",
      "deliveredVolume": "0",
      "purchases": [],
      "timezoneOffset": 120,
      "filecoinNode": {
        "id": "f01234",
        "buyerId": "93e399fb-991d-4f86-a315-4a1df8d18aee",
        "blockchainAddress": null,
        "createdAt": "2022-02-07T15:52:00.419Z",
        "updatedAt": "2022-02-07T15:52:00.419Z"
      },
      "externalId": null,
      "label": null,
      "createdAt": "2022-05-10T10:09:56.531Z",
      "updatedAt": "2022-05-10T10:09:56.531Z",
      "countryRegionMap": [
        {
          "country": "BE",
          "region": ""
        }
      ],
      "pageUrl": "https://proofs.zerolabs.green/partners/filecoin/contracts/bfcd046f-2f78-4652-b8fd-b1df27c64fd2",
      "dataUrl": "https://proofs-api.zerolabs.green/api/partners/filecoin/contracts/bfcd046f-2f78-4652-b8fd-b1df27c64fd2"
    },
    {
      "id": "67f6aa92-aab3-4e3a-975d-e056ca8325be",
      "productType": "GO",
      "energySources": [
        "HYDRO"
      ],
      "contractDate": "2021-08-31T00:00:00.000Z",
      "deliveryDate": "2021-08-31T00:00:00.000Z",
      "reportingStart": "2021-01-01T00:00:00.000Z",
      "reportingEnd": "2021-12-31T23:59:59.999Z",
      "buyer": {
        "id": "93e399fb-991d-4f86-a315-4a1df8d18aee",
        "name": "Buyer 3",
        "blockchainAddress": null,
        "createdAt": "2022-02-07T15:52:00.419Z",
        "updatedAt": "2022-02-07T15:52:00.419Z"
      },
      "seller": {
        "id": "8c0a45ce-1594-4107-baf0-ce8846b34afd",
        "name": "3Degrees Group, Inc",
        "addressLine1": "235 Montgomery St Suite 320 CA94104 San Francisco US",
        "addressLine2": "",
        "contactPerson": "-",
        "blockchainAddress": null,
        "createdAt": "2022-02-07T15:52:00.419Z",
        "updatedAt": "2022-02-07T15:52:00.419Z"
      },
      "openVolume": "96000000",
      "deliveredVolume": "0",
      "purchases": [],
      "timezoneOffset": 60,
      "filecoinNode": {
        "id": "f01234",
        "buyerId": "93e399fb-991d-4f86-a315-4a1df8d18aee",
        "blockchainAddress": null,
        "createdAt": "2022-02-07T15:52:00.419Z",
        "updatedAt": "2022-02-07T15:52:00.419Z"
      },
      "externalId": null,
      "label": null,
      "createdAt": "2022-05-10T09:36:01.588Z",
      "updatedAt": "2022-05-10T09:36:01.587Z",
      "countryRegionMap": [
        {
          "country": "NO",
          "region": ""
        }
      ],
      "pageUrl": "https://proofs.zerolabs.green/partners/filecoin/contracts/67f6aa92-aab3-4e3a-975d-e056ca8325be",
      "dataUrl": "https://proofs-api.zerolabs.green/api/partners/filecoin/contracts/67f6aa92-aab3-4e3a-975d-e056ca8325be"
    },
    {
      "id": "dbb6cec0-32b3-4e0b-b725-41143035fbfc",
      "productType": "GO",
      "energySources": [
        "HYDRO"
      ],
      "contractDate": "2021-08-31T00:00:00.000Z",
      "deliveryDate": "2021-08-31T00:00:00.000Z",
      "reportingStart": "2020-01-01T00:00:00.000Z",
      "reportingEnd": "2020-12-31T23:59:59.999Z",
      "buyer": {
        "id": "93e399fb-991d-4f86-a315-4a1df8d18aee",
        "name": "Buyer 3",
        "blockchainAddress": null,
        "createdAt": "2022-02-07T15:52:00.419Z",
        "updatedAt": "2022-02-07T15:52:00.419Z"
      },
      "seller": {
        "id": "8c0a45ce-1594-4107-baf0-ce8846b34afd",
        "name": "3Degrees Group, Inc",
        "addressLine1": "235 Montgomery St Suite 320 CA94104 San Francisco US",
        "addressLine2": "",
        "contactPerson": "-",
        "blockchainAddress": null,
        "createdAt": "2022-02-07T15:52:00.419Z",
        "updatedAt": "2022-02-07T15:52:00.419Z"
      },
      "openVolume": "2000000",
      "deliveredVolume": "0",
      "purchases": [],
      "timezoneOffset": 60,
      "filecoinNode": {
        "id": "f01234",
        "buyerId": "93e399fb-991d-4f86-a315-4a1df8d18aee",
        "blockchainAddress": null,
        "createdAt": "2022-02-07T15:52:00.419Z",
        "updatedAt": "2022-02-07T15:52:00.419Z"
      },
      "externalId": null,
      "label": null,
      "createdAt": "2022-05-10T09:36:01.670Z",
      "updatedAt": "2022-05-10T09:36:01.670Z",
      "countryRegionMap": [
        {
          "country": "NO",
          "region": ""
        }
      ],
      "pageUrl": "https://proofs.zerolabs.green/partners/filecoin/contracts/dbb6cec0-32b3-4e0b-b725-41143035fbfc",
      "dataUrl": "https://proofs-api.zerolabs.green/api/partners/filecoin/contracts/dbb6cec0-32b3-4e0b-b725-41143035fbfc"
    }
  ]
}
```
{% endswagger-response %}
{% endswagger %}
