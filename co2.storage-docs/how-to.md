# ⚒ How-To

## How-To

To use the UI, simply visit [CO2.Storage](https://co2.storage/) and begin testing the functionality. To use the API, install the package with this command:

<mark style="color:green;">`npm i @co2-storage/js-api`</mark>

The API and UI enable users to create new environmental asset templates (or schemas), or clone existing templates. After defining or choosing a template (schema), users can then create individual assets based on these schemas.

CO2.Storage also natively supports wallet connect functionality. The primary reason for this functionality is to associate creators with the schemas and assets themselves. In the future, we’d like CO2.Storage to be governed by a [Data DAO](https://fvm.filecoin.io/), and would like for creators to be rewarded for schema and asset usage.

CO2.Storage supports a rich template creation engine, in both the UI and API, which enables users to quickly define various fields and data types for their schema and assets.

<figure><img src="https://lh4.googleusercontent.com/Zod3SDcFnmHUrvUyLIQJT04nvHxmVQxtAEEwHfCVdljLAGIb4YHvF1D89LWOVPWK-8H3liA6jQ7xKX2dJsVZq4V42LNR-aVpEVXtgDXg5mSnS7XeBDOMoXjemJTYVnAa_c095wkh3Ikm7XvS-S7-EOI" alt=""><figcaption><p>Example Schema on Co2.Storage UI</p></figcaption></figure>

Every time a user defines a schema or asset and creates it, the data is uploaded to Filecoin and IPFS. Once uploaded, the data schema, assets, and relevant details are viewable on the CO2.Storage asset previewer and [IPLD Explorer](https://explore.ipld.io/#/).

Currently, this data is stored on Filecoin/IPFS via [Estuary](https://estuary.tech/). However, in the near future, we will offer alternative storage options built on our own decentralized infrastructure to ensure maximum uptime and timely retrieval. To develop this decentralized infrastructure, we are actively seeking input from Filecoin Storage Providers.&#x20;

If this is of interest to you, please reach out by emailing [green@filecoin.org](mailto:green@filecoin.org).
