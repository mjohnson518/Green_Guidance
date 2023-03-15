# 🧐 About

## About

[CO2.Storage](https://co2.storage) is a decentralized storage solution for structured data based on content addressed data schemas. CO2.Storage primarily focuses on structured data for environmental assets, such as Renewable Energy Credits, Carbon Offsets, and geospatial datasets.  This focus stems from our realization that the budding Refi space, and tokenized carbon credits in particular, would benefit from the development of standard data schemas for environmental assets.

This project should be considered pre-alpha and is not yet ready for production use. The [Filecoin Green](https://green.filecoin.io/) team is actively working on this project and welcomes contributions from the community.

We are seeking input to encourage standardization and reduce fragmentation of data schemas across the Refi space. To publicly discuss and crowd-source data schemas for CO2.Storage, please visit: [CO2.Storage Schemas Repo](https://github.com/protocol/co2\_storage\_schemas).

We are also actively seeking input on features from industry participants and interested parties. Please provide your contact information if you'd like to receive updates: [CO2.Storage Updates Form](https://forms.gle/CS5tY4kpsajpiTGV7).

Data made available through CO2.storage is provided by users, and not verified by Filecoin Green.

## Data Primitives

CO2.Storage maps inputs to base data schemas [(IPLD DAGs)](https://ipld.io/) for off-chain data (like metadata, images, attestation documents, and other assets) to promote the development of standard data schemas for environmental assets.

With IPLD DAGs, data is content addressed using IPFS, meaning the URI pointing to a piece of data (“ipfs://…”) is completely unique to that data (using a [content identifier](https://docs.ipfs.io/concepts/content-addressing/) , or CID). CIDs can be used for environmental assets and metadata to ensure the asset forever actually refers to the intended data (eliminating things like double counting, and making it trustlessly verifiable what content an asset is associated with). These standard, content addressed, data schemas will also enable more seamless cross-referencing for missing data and meta-analysis of different assets/credits, as well as help expedite the development of new forms of methodologies, supply, and marketplaces.

CO2.Storage currently has a [feature rich UI](https://co2.storage/) and a [Javascript API](https://www.npmjs.com/package/@co2-storage/js-api). Additionally, we’ll soon release a Go API and Go Indexer. CO2.Storage currently supports multiple data types, including:

\-> <mark style="color:green;">`int, integer`</mark>

\-> <mark style="color:green;">`decimal, float`</mark>

\-> <mark style="color:green;">`str, string`</mark>

\-> <mark style="color:green;">`txt, text, textarea`</mark>

\-> <mark style="color:green;">`bool, boolean`</mark>

\-> <mark style="color:green;">`date (single date)`</mark>

\-> <mark style="color:green;">`dates (multiple dates)`</mark>

\-> <mark style="color:green;">`datetime (single datetime)`</mark>

\-> <mark style="color:green;">`datetimes (multiple datetimes)`</mark>

\-> <mark style="color:green;">`daterange (date range)`</mark>

\-> <mark style="color:green;">`datetimerange (datetime range)`</mark>

\-> <mark style="color:green;">`array (lists)`</mark>

\-> <mark style="color:green;">`images (Images)`</mark>

\-> <mark style="color:green;">`documents (Documents)`</mark>

These data types correspond to the [Form Element case statements here](https://github.com/protocol/co2-storage/blob/main/client/web/src/mixins/form-elements/update-form.js). If your schema requires data types that are not currently supported, please request for a new data type by emailing [green@filecoin.org](mailto:green@filecoin.org).
