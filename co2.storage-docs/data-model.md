---
description: The data model described here is compliant with transform.storage v1.0.0.
---

# ⚙ Data Model

The goal of CO2.Storage is to store environmental asset data along with explicit information on its data type, making it easy to transform or compare data between different assets. Both the underlying data and the assets themselves are stored as [IPLD DAGs](https://proto.school/course/ipld).&#x20;

Below, every rectangle corresponds to an IPLD object with its own CID. Every arrow corresponds to an attribute of that object, labeled with the attribute name.

For a video overview and demo of the data model below, see the second half of the February 2022 [Filecoin Green Virtual Meetup](https://www.youtube.com/watch?v=y76SP7tObas\&t=2071s).

## Type Data Model

<figure><img src="../.gitbook/assets/Screenshot 2023-02-22 at 5.44.54 PM.png" alt=""><figcaption><p>The type data model</p></figcaption></figure>

An example of this data model is <mark style="color:blue;">**Type**</mark>: [bafyreidav…](https://explore.ipld.io/#/explore/bafyreidavm5scus7dg75e2iu3ki5xc6onrbnrjyv4f7josvln2uwmo7p3u) / **Schema**: [bafyreihxmr3…](https://explore.ipld.io/#/explore/bafyreihxmr3djalvov5wbwyyk2jjswvbvirkmfhea5p6bynr7h7z7fqokm)

Types are stored using the data model above. The type block contains some metadata about the type, along with a schema defining that type. The fields included in the type block are:

* **cid**: this is the CID corresponding to a JSON-schema defining the data type, shown in the schematic above
* **name**: a short label for this type
* **version**: version of the transform.storage protocol, in this case "1.0.0"
* **base** (optional): if this was cloned from another type, base is the CID of that type
* **parent** (optional): null for v1.0.0
* **creator** (optional): wallet creating this type
* **reference** (optional): null for v1.0.0
* **timestamp** (optional): UTC timestamp when this type was created
* **description** (optional): longer label for this type

## Asset Data Model

<figure><img src="../.gitbook/assets/Screenshot 2023-02-22 at 6.03.19 PM.png" alt=""><figcaption><p>The Asset data model</p></figcaption></figure>

An example of this data model is <mark style="color:green;">**Asset:**</mark> [bafyreidzoai4…](https://explore.ipld.io/#/explore/bafyreidzoai4dm53ga6lb3mq6axt2s64uxh5x7zw4ey46rygt3jnwaw2mu) / <mark style="color:blue;">**Type:**</mark> [bafyreidav…](https://explore.ipld.io/#/explore/bafyreidavm5scus7dg75e2iu3ki5xc6onrbnrjyv4f7josvln2uwmo7p3u) / **Data:** [bafyreictxcw…](https://explore.ipld.io/#/explore/bafyreictxcwwmiymlp56zmkmk4dzdctvh645riqn2dvog44niu5hvo7nrm)

As shown above, assets link data in a payload to the datatype associated with that data. The asset itself contains some additional metadata. Its attributes are:

* **cid**: this is the CID of the actual data we are describing; the 'payload' of the asset data
* **name**: a short label for this asset
* **version**: version of the transform.storage protocol, in this case "1.0.0"
* **parent** (optional): null for v1.0.0
* **creator** (optional): wallet creating this asset
* **timestamp** (optional): UTC timestamp when this asset was created
* **description** (optional): longer label for this asset
