---
description: This API provides relation in between Filecoin Miner IDs and Peer IDs.
---

# ↔ Filecoin Miner ID <-> Peer ID relation API

{% hint style="info" %}
**Good to know:** In addition to below there is an Open API documentation available [here](https://green.filecoin.space/swagger/minerid-peerid/).
{% endhint %}

### Find Peer IDs for provided Miner IDs

By passing in the comma delimited list of Miner Ids, you can search for related Peer Ids in the system.

{% swagger method="get" path="/peer_id" baseUrl="https://green.filecoin.space/minerid-peerid/api/v1" summary="Get Filecoin storage providers' Peer IDs for supplied list of comma separated Miner IDs" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-parameter in="query" name="miner_id" type="String" %}
Comma separated list of miner IDs
{% endswagger-parameter %}

{% swagger-response status="200: OK" description="JSON response" %}
```javascript
[
  {
    "Head": 1908194,
    "MinerId": "f01234",
    "PeerId": "12D3KooWPWJemjphGa2pANr6j7HCaLyjUvCroHyTJsATY6TaCFAF",
    "Multiaddrs": [
      "BI2KQBQGXcE="
    ]
  }
]
```
{% endswagger-response %}
{% endswagger %}

### Find Miner IDs for provided Peer IDs

By passing in the comma delimited list of Peer Ids, you can search for related Miner Ids in the system.

{% swagger method="get" path="/miner_id" baseUrl="https://green.filecoin.space/minerid-peerid/api/v1" summary="Get Filecoin storage providers' Miner IDs for supplied list of comma separated Peer IDs" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-parameter in="query" name="peer_id" type="String" %}
Comma separated list of peer IDs
{% endswagger-parameter %}

{% swagger-response status="200: OK" description="JSON response" %}
```javascript
[
  {
    "Head": 1908194,
    "MinerId": "f01234",
    "PeerId": "12D3KooWPWJemjphGa2pANr6j7HCaLyjUvCroHyTJsATY6TaCFAF",
    "Multiaddrs": [
      "BI2KQBQGXcE="
    ]
  }
]
```
{% endswagger-response %}
{% endswagger %}
