---
description: SP_EVP_Data_V1.0.0 - last updated on 08/28/23
---

# 💡 Energy Validation Process (EVP) Schema

Below is the data schema for the SP Energy Validation Process (EVP). This schema can also be found here: [**Green Score Schema**](https://form.co2.storage/bafyreihpuneh55psvm35v6fv4hh36suid4dtyqprqjfbum6joxqu3rgkji).

```
[
  [
    "Record Type",
    {
      "type": "string",
      "value": "Electricity and Water data for Green Score",
      "mandatory": true
    }
  ],
  [
    "Record Version",
    {
      "type": "string",
      "value": "1.0.0",
      "mandatory": true
    }
  ],
  [
    "EVP Version",
    {
      "type": "string",
      "value": "4.0.0",
      "mandatory": true
    }
  ],
  [
    "Storage Provider Name",
    {
      "type": "string",
      "mandatory": false,
      "placeholder": "SP Name (not mandatory)"
    }
  ],
  [
    "Country",
    {
      "type": "string",
      "mandatory": true,
      "placeholder": "Country Code (ISO 3166 Alpha-code-2)"
    }
  ],
  [
    "City",
    {
      "type": "string",
      "mandatory": false,
      "placeholder": "City (not mandatory)"
    }
  ],
  [
    "ZIP or Location Code",
    {
      "type": "string",
      "mandatory": false,
      "placeholder": "ZIP or Location Code (not mandatory)"
    }
  ],
  [
    "minerIDs",
    {
      "type": "string",
      "mandatory": true,
      "placeholder": "f01199442, f01199430, f01201327, f01207045, f01208862"
    }
  ],
  [
    "Water Accounting Period Start",
    {
      "type": "date",
      "mandatory": true
    }
  ],
  [
    "Water Accounting Period End",
    {
      "type": "date",
      "mandatory": true
    }
  ],
  [
    "Water Consumed (L)",
    {
      "min": 0,
      "type": "float",
      "value": 0,
      "mandatory": true,
      "fractionDigits": 3
    }
  ],
  [
    "Electricity Accounting Period Start",
    {
      "type": "date",
      "mandatory": true
    }
  ],
  [
    "Electricity Accounting Period End",
    {
      "type": "date",
      "mandatory": true
    }
  ],
  [
    "SP Delivered Electricity (kWh)",
    {
      "min": -1000000000000,
      "type": "float",
      "value": 0,
      "mandatory": true
    }
  ],
  [
    "SP Returned Electricity (kWh)",
    {
      "min": -1000000000000,
      "type": "float",
      "value": 0,
      "mandatory": true
    }
  ],
  [
    "SP Net Electricity Consumed from Grid (kWh)",
    {
      "min": -1000000000000,
      "type": "float",
      "value": 0,
      "mandatory": true
    }
  ],
  [
    "SP Electricity not used to power Filecoin network (kWh)",
    {
      "min": -1000000000000,
      "type": "float",
      "mandatory": true
    }
  ],
  [
    "SP Onsite Renewable Energy Produced (kWh)",
    {
      "min": -1000000000000,
      "type": "float",
      "value": 0,
      "mandatory": true
    }
  ],
  [
    "Onsite Renewable Electricity Type",
    {
      "min": 0,
      "type": "string",
      "mandatory": true,
      "placeholder": "Rooftop Solar"
    }
  ],
  [
    "Total Electricity Used for Filecoin Operations (kWh)",
    {
      "min": -1000000000000,
      "type": "float",
      "value": 0,
      "mandatory": true
    }
  ],
  [
    "Electricity Notes (optional)",
    {
      "type": "string",
      "mandatory": false
    }
  ],
  [
    "Renewable Electricity Purchased (kWh)",
    {
      "min": -1000000000000,
      "type": "float",
      "value": 0,
      "mandatory": true
    }
  ],
  [
    "Renewable Electricity Purchased Source",
    {
      "type": "string",
      "mandatory": false,
      "placeholder": "Example: Solar PV RECs registered on EnergyWeb"
    }
  ],
  [
    "Renewable Electricity Purchased Documentation (Optional)",
    {
      "type": "documents",
      "mandatory": false
    }
  ],
  [
    "SP Average Raw Byte Data Storage Capacity over Reporting Time Period (PiB)",
    {
      "type": "float",
      "mandatory": true,
      "fractionDigits": 6
    }
  ],
  [
    "Network Average Raw Byte Data Storage Capacity over Reporting Time Period (PiB)",
    {
      "type": "float",
      "mandatory": true,
      "fractionDigits": 3
    }
  ],
  [
    "SP Scope 2 Emissions for Reporting Period (kg CO2e)",
    {
      "min": 0,
      "type": "float",
      "mandatory": true
    }
  ],
  [
    "Network Electricity Use for Reporting Period (kWh)",
    {
      "min": 0,
      "type": "float",
      "mandatory": true
    }
  ],
  [
    "Network Renewable Energy Purchases (kWh)",
    {
      "min": 0,
      "type": "float",
      "mandatory": true
    }
  ],
  [
    "Global Average Grid Emissions Factor (gCO2e/kWh)",
    {
      "min": 0,
      "type": "int",
      "value": 436,
      "mandatory": true
    }
  ],
  [
    "Global Average Grid Emissions Factor Source",
    {
      "min": 0,
      "type": "string",
      "value": "https://ourworldindata.org/grapher/carbon-intensity-electricity?tab=table",
      "mandatory": true
    }
  ],
  [
    "Network Scope 2 Emissions for Reporting Period (kg CO2e)",
    {
      "min": 0,
      "type": "float",
      "mandatory": true
    }
  ],
  [
    "Emissions Score",
    {
      "max": 1,
      "min": 0,
      "type": "float",
      "mandatory": true,
      "fractionDigits": 3
    }
  ],
  [
    "SP Marginal Emissions for Reporting Period (kg CO2e)",
    {
      "min": 0,
      "type": "float",
      "mandatory": true
    }
  ],
  [
    "Network Marginal Emissions for Reporting Period (kg CO2e)",
    {
      "min": 0,
      "type": "float",
      "mandatory": true
    }
  ],
  [
    "Global Average Marginal Emissions Factor (gCO2e/kWh)",
    {
      "min": 0,
      "type": "float",
      "value": 614.98,
      "mandatory": true
    }
  ],
  [
    "Global Average Marginal Emissions Factor Source",
    {
      "min": 0,
      "type": "string",
      "value": "https://unfccc.int/sites/default/files/resource/IFI%20Default%20Grid%20Factors%202021%20v3.1_unfccc.xlsx",
      "mandatory": true
    }
  ],
  [
    "Location Score",
    {
      "max": 1,
      "min": 0,
      "type": "float",
      "mandatory": true,
      "fractionDigits": 3
    }
  ],
  [
    "Location Information (5%)",
    {
      "type": "array",
      "options": [
        "No data (0%)",
        "Self Reported by SP (15%)",
        "Reported on Utility Bill or other third-party document (65%)",
        "Address reported on two third-party documents and all information matches (100%)"
      ],
      "multiple": false,
      "mandatory": true
    }
  ],
  [
    "minerIDs Information (4%)",
    {
      "type": "array",
      "options": [
        "No data (0%)",
        "Self Reported by SP (25%)",
        "SP verifies list is complete (50%)",
        "Auditor verifies no discrepancies (100%)"
      ],
      "multiple": false,
      "mandatory": true
    }
  ],
  [
    "Hardware Information (6%)",
    {
      "type": "array",
      "options": [
        "No data (0%)",
        "Self Reported by SP (30%)",
        "Receipts and attestation documents provided to verify claims (85%)",
        "Photo and video evidence provided to further verify claims (100%)"
      ],
      "multiple": false,
      "mandatory": true
    }
  ],
  [
    "Water Use Information (5%)",
    {
      "type": "array",
      "options": [
        "No data (0%)",
        "Monthly Utility Bill (100%)"
      ],
      "multiple": false,
      "mandatory": true
    }
  ],
  [
    "Energy Use Information (80%)",
    {
      "type": "array",
      "options": [
        "No data (0%)",
        "Power Bill (40%)",
        "Granular Information (75%)",
        "Power bill matches granular (100%)"
      ],
      "multiple": false,
      "mandatory": true
    }
  ],
  [
    "Confidence Score Version",
    {
      "type": "string",
      "value": "2.0.0",
      "mandatory": true
    }
  ],
  [
    "Confidence Score",
    {
      "max": 1,
      "min": 0,
      "type": "float",
      "mandatory": true,
      "fractionDigits": 3
    }
  ],
  [
    "Green Score",
    {
      "min": 0,
      "type": "float",
      "mandatory": true,
      "fractionDigits": 3
    }
  ],
  [
    "Green Score Version",
    {
      "type": "string",
      "value": "2.0.0",
      "mandatory": true
    }
  ],
  [
    "Notes on Data Sources",
    {
      "type": "text",
      "mandatory": true,
      "placeholder": "what data formats and sources were available? (monthly power bills, smart meter readings, estimates, etc.)"
    }
  ],
  [
    "CID of Previous Asset (if any)",
    {
      "type": "string",
      "mandatory": false,
      "placeholder": "bafyreidibetvivf4vvxieukcsq474tcyvxcn4y5hlwsrwz2alj52xiyo5i"
    }
  ]
]
```
