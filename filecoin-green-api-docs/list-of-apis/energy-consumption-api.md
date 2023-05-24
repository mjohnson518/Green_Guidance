---
description: >-
  This API provides comprehensive data about Filecoin Storage Providers' energy
  consumption metric.
---

# ⚡ Energy Consumption API

{% hint style="info" %}
**Good to know:** In addition to below there is an Open API documentation available [here](https://api.filecoin.energy/docs/).
{% endhint %}

## Data Model

The Data Model end point is listing all available data models (e.g. Energy intensity, Energy used to seal data, Energy used to store data, etc.).

{% swagger method="get" path="" baseUrl="https://api.filgreen.d.interplanetary.one/models/list" summary="List available API data models" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-response status="200: OK" description="JSON response" %}
```javascript
[
    {
        "id": 0,
        "name": "Energy consumption rate (v1.0.1)",
        "code_name": "TotalEnergyModelv_1_0_1",
        "category": "energy",
        "details": "The total rate of electrical energy use. This is the sum of sealing and storage energy use, multiplied by a [Power Usage Effectiveness](https://en.wikipedia.org/wiki/Power_usage_effectiveness) (PUE) representing overhead energy costs such as cooling and power conversion. Bounds and estimate come from combining the bounds and estimates of sealing and storage energy, as well as different values of estimated PUE.\n\n**Network view:** Total electrical power used by the Filecoin network.\n\n**Storage Provider (SP) view:** Electrical power used by this SP.\n"
    },
    {
        "id": 1,
        "name": "Energy used to seal data (v1.0.1)",
        "code_name": "SealingEnergyModelv_1_0_1",
        "category": "energy",
        "details": "[Sealing](https://spec.filecoin.io/systems/filecoin_mining/sector/sealing/) is the process of generating SNARK proofs for a data sector which will allow an SP to prove that they are continuing to store that data over time, and is one of the components of energy use of the Filecoin network. Energy use due to sealing is estimated by multiplying the increase in storage capacity over a given time period by a constant value as described in the methodology. Bounds and estimate come from different values of this constant.\n\n**Network view:** Total electrical power used to seal data for the entire Filecoin network.\n\n**Storage Provider (SP) view:** Electrical power used by this SP to seal data.\n"
    },
    {
        "id": 2,
        "name": "Energy used to store data (v1.0.1)",
        "code_name": "StorageEnergyModelv_1_0_1",
        "category": "energy",
        "details": "The energy used to store data over time, which is a component of the energy used by the Filecoin network. Storage energy use is estimated by multiplying storage capacity by a constant value. Bounds and estimate come from different values of this constant.\n\n**Network view:** Total electrical power used to store all data on the Filecoin network.\n\n**Storage Provider (SP) view:** Electrical power used by this SP to store data.\n"
    },
    {
        "id": 3,
        "name": "Cumulative Energy Use (v1.0.1)",
        "code_name": "CumulativeEnergyModel_v_1_0_1",
        "category": "energy",
        "details": "Total amount of energy used during a time period in kWh"
    },
    {
        "id": 4,
        "name": "Cumulative renewable energy purchases ",
        "code_name": "RenewableEnergyModel",
        "category": "energy",
        "details": "Cumulative renewable energy certificate (REC) purchases over time"
    },
    {
        "id": 5,
        "name": "Energy Intensity",
        "code_name": "EnergyIntensityModel",
        "category": "energy",
        "details": "\n             **Energy Intensity:** Total electrical power used by the Filecoin network \n             divided by data storage Capacity.\n             "
    },
    {
        "id": 6,
        "name": "Data storage capacity added per day",
        "code_name": "SealedModel",
        "category": "capacity",
        "details": "**Network view:** New data storage capacity added to Filecoin’s decentralized storage network (sealed) per day.\n\n**Storage Provider (SP) view:** The amount of new data storage contributed to the network (sealed) by this SP per day.\n"
    },
    {
        "id": 7,
        "name": "Data storage capacity",
        "code_name": "CapacityModel",
        "category": "capacity",
        "details": "**Network view:** The total amount of data storage capacity contributed to Filecoin’s decentralized storage network, based on on-chain proofs.\n\n**Storage Provider (SP) view:** The amount of data storage contributed by this SP, based on on-chain proofs.\n"
    }
]
```
{% endswagger-response %}
{% endswagger %}

<details>

<summary>Available Data Models</summary>

**Energy Intensity:**\
Total electrical power used by the Filecoin network divided by data storage Capacity.\
<mark style="color:green;">Model:</mark> <mark style="color:green;"></mark><mark style="color:green;">`"id": 0`</mark> <mark style="color:green;"></mark><mark style="color:green;">or</mark> <mark style="color:green;"></mark><mark style="color:green;">`"code_name": "EnergyIntensityModel"`</mark>

**Renewable Energy Ratio:**\
<mark style="color:green;">Model</mark>_<mark style="color:green;">:</mark>_ <mark style="color:green;"></mark><mark style="color:green;">`"id": 1`</mark> <mark style="color:green;"></mark><mark style="color:green;">or</mark> <mark style="color:green;"></mark><mark style="color:green;">`"code_name": "RenewableEnergyRatioModel"`</mark>

**Energy consumption rate (v1.0.1):**\
The total rate of electrical energy use. This is the sum of sealing and storage energy use, multiplied by a Power Usage Effectiveness (PUE) representing overhead energy costs such as cooling and power conversion. Bounds and estimate come from combining the bounds and estimates of sealing and storage energy, as well as different values of estimated PUE.\
_Network view:_ Total electrical power used by the Filecoin network.\
_Storage Provider (SP) view:_ Electrical power used by this SP.\
<mark style="color:green;">Model</mark>_<mark style="color:green;">:</mark>_ <mark style="color:green;"></mark><mark style="color:green;">`"id": 2`</mark> <mark style="color:green;"></mark><mark style="color:green;">or</mark> <mark style="color:green;"></mark><mark style="color:green;">`"code_name": "`</mark><mark style="color:green;">TotalEnergyModelv\_1\_0\_1</mark><mark style="color:green;">`"`</mark>

**Energy used to seal data (v1.0.1):**\
[Sealing](https://spec.filecoin.io/systems/filecoin\_mining/sector/sealing/) is the process of generating SNARK proofs for a data sector which will allow an SP to prove that they are continuing to store that data over time, and is one of the components of energy use of the Filecoin network. Energy use due to sealing is estimated by multiplying the increase in storage capacity over a given time period by a constant value as described in the methodology. Bounds and estimate come from different values of this constant.\
_Network view:_ Total electrical power used to seal data for the entire Filecoin network.\
_Storage Provider (SP) view:_ Electrical power used by this SP to seal data.\
<mark style="color:green;">Model</mark>_<mark style="color:green;">:</mark>_ <mark style="color:green;"></mark><mark style="color:green;">`"id": 3`</mark> <mark style="color:green;"></mark><mark style="color:green;">or</mark> <mark style="color:green;"></mark><mark style="color:green;">`"code_name": "`</mark><mark style="color:green;">SealingEnergyModelv\_1\_0\_1</mark><mark style="color:green;">`"`</mark>

**Energy used to store data (v1.0.1):**\
The energy used to store data over time, which is a component of the energy used by the Filecoin network. Storage energy use is estimated by multiplying storage capacity by a constant value. Bounds and estimate come from different values of this constant.\
_Network view:_ Total electrical power used to store all data on the Filecoin network. _Storage Provider (SP) view:_ Electrical power used by this SP to store data.\
<mark style="color:green;">Model</mark>_<mark style="color:green;">:</mark>_ <mark style="color:green;"></mark><mark style="color:green;">`"id": 4`</mark> <mark style="color:green;"></mark><mark style="color:green;">or</mark> <mark style="color:green;"></mark><mark style="color:green;">`"code_name": "`</mark><mark style="color:green;">StorageEnergyModelv\_1\_0\_1</mark><mark style="color:green;">`"`</mark>

**Cumulative Energy Use (v1.0.1):**\
Total amount of energy used during a time period in kWh.\
<mark style="color:green;">Model</mark>_<mark style="color:green;">:</mark>_ <mark style="color:green;"></mark><mark style="color:green;">`"id": 5`</mark> <mark style="color:green;"></mark><mark style="color:green;">or</mark> <mark style="color:green;"></mark><mark style="color:green;">`"code_name": "`</mark><mark style="color:green;">CumulativeEnergyModel\_v\_1\_0\_1</mark><mark style="color:green;">`"`</mark>

**Cumulative renewable energy purchases:**\
Cumulative renewable energy certificate (REC) purchases over time.\
<mark style="color:green;">Model</mark>_<mark style="color:green;">:</mark>_ <mark style="color:green;"></mark><mark style="color:green;">`"id": 6`</mark> <mark style="color:green;"></mark><mark style="color:green;">or</mark> <mark style="color:green;"></mark><mark style="color:green;">`"code_name": "`</mark><mark style="color:green;">RenewableEnergyModel</mark><mark style="color:green;">`"`</mark>

**Data storage capacity added per day:**\
_Network view:_ New data storage capacity added to Filecoin’s decentralized storage network (sealed) per day.\
_Storage Provider (SP) view:_ The amount of new data storage contributed to the network (sealed) by this SP per day.\
<mark style="color:green;">Model</mark>_<mark style="color:green;">:</mark>_ <mark style="color:green;"></mark><mark style="color:green;">`"id": 7`</mark> <mark style="color:green;"></mark><mark style="color:green;">or</mark> <mark style="color:green;"></mark><mark style="color:green;">`"code_name": "`</mark><mark style="color:green;">SealedModel</mark><mark style="color:green;">`"`</mark>

**Data storage capacity:**\
_Network view:_ The total amount of data storage capacity contributed to Filecoin’s decentralized storage network, based on on-chain proofs.\
_Storage Provider (SP) view:_ The amount of data storage contributed by this SP, based on on-chain proofs.\
<mark style="color:green;">Model</mark>_<mark style="color:green;">:</mark>_ <mark style="color:green;"></mark><mark style="color:green;">`"id": 8`</mark> <mark style="color:green;"></mark><mark style="color:green;">or</mark> <mark style="color:green;"></mark><mark style="color:green;">`"code_name": "`</mark><mark style="color:green;">CapacityModel</mark><mark style="color:green;">`"`</mark>

</details>

### Energy Consumption: Daily, weekly and monthly data granularity

This endpoint provides energy consumption data for selected data model grouped on a daily, weekly or monthly scale.

{% swagger method="get" path="" baseUrl="https://api.filgreen.d.interplanetary.one/models/model" summary="Energy consumption grouped on a daily, weekly and monthly scale for selected model, date range and Storage Provider" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-parameter in="query" name="id*" type="Integer" %}
Id of the data model.

\


(either "id" or associated "code_name" query parameter have to be provided)
{% endswagger-parameter %}

{% swagger-parameter in="query" name="code_name*" type=" " %}
Code name of the data model, see 'Available data models' above.

\


(either "id" or associated "code_name" query parameter have to be provided)
{% endswagger-parameter %}

{% swagger-parameter in="query" name="filter" type=" " %}
Data granulation. Possible values are: "day", "week" or "month".

\


If not provided "day" is considered as default value.
{% endswagger-parameter %}

{% swagger-parameter in="query" name="miner" type="String" %}
Miner Id (e.g. f01234). If not listed data is provided without filtering per miner Id.
{% endswagger-parameter %}

{% swagger-parameter in="query" name="start" type="Date / String" %}
ISO 8601 formatted start date.

\


If not provided data points are listed from the epoch 0.
{% endswagger-parameter %}

{% swagger-parameter in="query" name="end" type="Date / String" %}
ISO 8601 formatted end date.

\


If not provided data points are listed up to the most recent measurement.
{% endswagger-parameter %}

{% swagger-response status="200: OK" description="JSON response" %}
```javascript
{
    "id": "0",
    "code_name": "TotalEnergyModelv_1_0_1",
    "name": "Energy consumption rate (v1.0.1)",
    "category": "energy",
    "x": "time",
    "y": "kW",
    "version": 0,
    "filter": "day",
    "data": [
        {
            "title": "Lower bound",
            "data": [
                {
                    "value": "31894.361954900576",
                    "start_date": "2022-04-29T00:00:00.000Z",
                    "end_date": "2022-04-29T23:59:59.999Z"
                },
                {
                    "value": "31775.267922347760",
                    "start_date": "2022-04-30T00:00:00.000Z",
                    "end_date": "2022-04-30T23:59:59.999Z"
                }
            ]
        },
        {
            "title": "Estimate",
            "data": [
                {
                    "value": "171561.258677004376",
                    "start_date": "2022-04-29T00:00:00.000Z",
                    "end_date": "2022-04-29T23:59:59.999Z"
                },
                {
                    "value": "170551.946689708060",
                    "start_date": "2022-04-30T00:00:00.000Z",
                    "end_date": "2022-04-30T23:59:59.999Z"
                }
            ]
        },
        {
            "title": "Upper bound",
            "data": [
                {
                    "value": "473751.138657113246",
                    "start_date": "2022-04-29T00:00:00.000Z",
                    "end_date": "2022-04-29T23:59:59.999Z"
                },
                {
                    "value": "471916.373850792235",
                    "start_date": "2022-04-30T00:00:00.000Z",
                    "end_date": "2022-04-30T23:59:59.999Z"
                }
            ]
        }
    ]
} // Response
}
```
{% endswagger-response %}
{% endswagger %}

### Energy Consumption: All data points

This endpoint provides all measured energy consumption data points for selected data model.

{% swagger method="get" path="" baseUrl="https://api.filgreen.d.interplanetary.one/models/export" summary="Energy consumption" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-parameter in="query" name="id*" type="Integer" %}
Id of the data model.

\


(either "id" or associated "code_name" query parameter have to be provided)
{% endswagger-parameter %}

{% swagger-parameter in="query" name="code_name*" type=" " %}
Code name of the data model, see 'Available data models' above.

\


(either "id" or associated "code_name" query parameter have to be provided)
{% endswagger-parameter %}

{% swagger-parameter in="query" name="miner" type="String" %}
Miner Id (e.g. f01234). If not listed data is provided without filtering per miner Id.
{% endswagger-parameter %}

{% swagger-parameter in="query" name="start" type="Date / String" %}
ISO 8601 formatted start date.

\


If not provided data points are listed from the epoch 0.
{% endswagger-parameter %}

{% swagger-parameter in="query" name="end" type="Date / String" %}
ISO 8601 formatted end date. If not provided data points are listed up to the most recent measurement.
{% endswagger-parameter %}

{% swagger-parameter in="query" name="offset" type="Integer" %}
Number of data points to skip from the beginning of the record set. Default 0.
{% endswagger-parameter %}

{% swagger-parameter in="query" name="limit" type="Integer" %}
Maximal number of data points to be listed. Default 10000.
{% endswagger-parameter %}

{% swagger-response status="200: OK" description="JSON response" %}
```javascript
{
  "fields": [
    "epoch",
    "total_energy_kW_lower",
    "total_energy_kW_estimate",
    "total_energy_kW_upper",
    "timestamp"
  ],
  "data": [
    {
      "epoch": "1423800",
      "total_energy_kW_lower": "26561.709211124736",
      "total_energy_kW_estimate": "142666.944194007936",
      "total_energy_kW_upper": "394504.605809705056",
      "timestamp": "2022-01-01T00:00:00.000Z"
    },
    {
      "epoch": "1423801",
      "total_energy_kW_lower": "33665.494160344832",
      "total_energy_kW_estimate": "196408.026620076032",
      "total_energy_kW_upper": "502793.474799859072",
      "timestamp": "2022-01-01T00:00:30.000Z"
    },
    {
      "epoch": "1423802",
      "total_energy_kW_lower": "24310.747738816768",
      "total_energy_kW_estimate": "125638.018984010368",
      "total_energy_kW_upper": "360191.320487680928",
      "timestamp": "2022-01-01T00:01:00.000Z"
    },
    {
      "epoch": "1423803",
      "total_energy_kW_lower": "26620.212637369856",
      "total_energy_kW_estimate": "143109.417155747456",
      "total_energy_kW_upper": "395396.401709311776",
      "timestamp": "2022-01-01T00:01:30.000Z"
    },
    {
      "epoch": "1423804",
      "total_energy_kW_lower": "24778.503308768000",
      "total_energy_kW_estimate": "129176.600096249600",
      "total_energy_kW_upper": "367321.696158196800",
      "timestamp": "2022-01-01T00:02:00.000Z"
    },
    {
      "epoch": "1423805",
      "total_energy_kW_lower": "24456.941042341376",
      "total_energy_kW_estimate": "126743.912678130176",
      "total_energy_kW_upper": "362419.851969575296",
      "timestamp": "2022-01-01T00:02:30.000Z"
    },
    {
      "epoch": "1423806",
      "total_energy_kW_lower": "23258.369123417344",
      "total_energy_kW_estimate": "117676.527420118144",
      "total_energy_kW_upper": "344149.023870830624",
      "timestamp": "2022-01-01T00:03:00.000Z"
    },
    {
      "epoch": "1423807",
      "total_energy_kW_lower": "27906.524038613504",
      "total_energy_kW_estimate": "152840.442591807104",
      "total_energy_kW_upper": "415004.693759300384",
      "timestamp": "2022-01-01T00:03:30.000Z"
    },
    {
      "epoch": "1423808",
      "total_energy_kW_lower": "27000.292853051136",
      "total_energy_kW_estimate": "145984.641783342336",
      "total_energy_kW_upper": "401190.255044203456",
      "timestamp": "2022-01-01T00:04:00.000Z"
    },
    {
      "epoch": "1423809",
      "total_energy_kW_lower": "27175.705275236096",
      "total_energy_kW_estimate": "147311.627765050496",
      "total_energy_kW_upper": "403864.205879485216",
      "timestamp": "2022-01-01T00:04:30.000Z"
    }
  ]
}
```
{% endswagger-response %}
{% endswagger %}
