# 🧑💻 Getting Started

## Getting Started

CO2.Storage maps inputs to base data schemas [(IPLD DAGs)](https://ipld.io/) for off-chain data (like metadata, images, attestation documents, and other assets) to promote the development of standard data schemas for environmental assets.

With IPLD DAGs, data is content addressed using IPFS, meaning the URI pointing to a piece of data (“ipfs://…”) is completely unique to that data (using a [content identifier](https://docs.ipfs.io/concepts/content-addressing/) , or CID). CIDs can be used for environmental assets and metadata to ensure the asset forever actually refers to the intended data (eliminating things like double counting, and making it trustlessly verifiable what content an asset is associated with). These standard, content addressed, data schemas will also enable more seamless cross-referencing for missing data and meta-analysis of different assets/credits, as well as help expedite the development of new forms of methodologies, supply, and marketplaces.

CO2.Storgae currently has a [feature rich UI](https://co2.storage/) and a [Javascript API](https://www.npmjs.com/package/@co2-storage/js-api). Additionally, we’ll soon release a Go API and Go Indexer. CO2.Storage currently supports multiple data types, including:

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
