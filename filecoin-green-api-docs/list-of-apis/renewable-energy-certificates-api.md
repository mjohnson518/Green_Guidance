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
  "recsTotal": 0,
  "transactions": []
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
