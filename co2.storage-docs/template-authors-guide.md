---
description: Guide for writing content-addressed data types using CO2.Storage
---

# ✍ Template Author's Guide

Templates are central to the [data model](https://filecoin-green.gitbook.io/filecoin-green-documentation/co2.storage-docs/data-model) of CO2.Storage. By content addressing not only the underlying data but its type, we are able to ensure that code will run on the data we feed it as well as rapidly gather data from different sources. Templates are what allows us to do that.

## Index

1. [Writing a Schema with the UI](template-authors-guide.md#writing-a-schema-with-the-ui)
2. [List of Primitive Types](template-authors-guide.md#list-of-primitive-types)
3. [Optional Fields](template-authors-guide.md#optional-fields)
4. [Select from Predefined Elements](template-authors-guide.md#select-from-predefined-elements)
5. [Nested Schemas](template-authors-guide.md#nested-schemas)

## Writing a Schema with the UI

1\) To manually author a template using the CO2.Storage UI, go to the [Templates](https://www.co2.storage/templates) page and log in to the site using your wallet.

2\) Make sure that you have selected the correct indexing chain in the upper left hand side of the page. This functions as your workspace, and is the data structure that the service uses to index all of the templates and data added.

You should see a page like this, where I've chosen the "sandbox" indexing chain:

<figure><img src="../.gitbook/assets/Screenshot 2023-06-07 at 4.56.36 PM.png" alt=""><figcaption></figcaption></figure>

3\) If you want to modify an existing template, select it from the list by clicking on its name. If you want to start from scratch, click "Create New Template".&#x20;

4\) This will open up an editor where you can view and modify your template. If you create a new template, the editor should look like this:

<figure><img src="../.gitbook/assets/Screenshot 2023-06-07 at 2.58.21 PM (1).png" alt=""><figcaption></figcaption></figure>

At the top we have the Template Metadata, which correspond to the **name**, **base**, and **description** fields in the [Type Data Model](https://filecoin-green.gitbook.io/filecoin-green-documentation/co2.storage-docs/data-model) for the template we will create. Of these fields, only **name** is required.

At the bottom, we have the Schema Editor which is where we will add a new schema. This corresponds to the **cid** field of the [Type Data Model](https://filecoin-green.gitbook.io/filecoin-green-documentation/co2.storage-docs/data-model), and is where the meat of the template is defined.

5\) Type or paste in your schema. While you are working, your code will be automatically checked and a preview will appear at the right hand side:

<figure><img src="../.gitbook/assets/Screenshot 2023-06-07 at 3.09.54 PM.png" alt=""><figcaption></figcaption></figure>

6\) If you want your schema to contain fields in no particular order, make it an object and structure it like this:

```json
{
    "Field Name" : {
        "type" : "<Primitive Type>"
        <options>
    },
    ...
}
```

7\) If you want your schema to contain fields in a specific order, make it an array and structure it like this:

```json
[
    {
        "Field Name" : {
            "type" : "<Primitive Type>"
            <options>
        }
    },
    ...
]
```

8\) When you are done, hit "Create". Your template will be created and will be ready to be used.

## List of Primitive Types

Transform.storage schemas are similar to JSON or IPLD schemas, but have a more extensive set of primitive types.&#x20;

{% hint style="info" %}
All primitive types must appear in double quotes and in lower case within your schema.
{% endhint %}

* **int** or **integer**: an integer number
* **decimal** or **float**: floating point decimal
* **str** or **string**: string, with input as a single line box
* **txt** or **text** or **textarea**: string, with input as a large box
* **bool** or **boolean**: boolean (true or false) value
* **date** or **dates**: a date
* **datetime** or **datetimes**: date with a timestamp
* **daterange**: range with start and end dates
* **datetimerange**: range with start and end timestamps
* **list** or **array**: choice of one or more predetermined elements. There are additional options reserved for this primitive; see [Select from Predefined Elements](template-authors-guide.md#select-from-predefined-elements).
* **documents**: allows user to upload a file
* **images**: allows user to upload an image file
* **bacalhau-url-dataset**: a dataset for Bacalhau downloaded from a URL
* **bacalhau-custom-docker-job-with-url-inputs**: a function for Bacalhau with inputs downloaded from a URL
* **bacalhau-custom-docker-job-with-cid-inputs**: a function for Bacalhau with inputs based on a CID
* **bacalhau-custom-docker-job-without-inputs**: a function for Bacalhau&#x20;
* **json**: allows the user to input JSON data
* **cid**: a content address retrievable through IPFS
* **ipld-link**: a hash link retrievable through IPLD
* **template** or **schema**: use the CID of a Transform.Storage schema to create a nested structure. See [Nested Schemas](template-authors-guide.md#nested-schemas) below.
* **template-list** or **schema-list**: create a nested structure with more than one entry for a given subschema. See [Nested Schemas](template-authors-guide.md#nested-schemas) below.

## Optional Fields

Add optional fields to an element in your template schema for additional control.

**mandatory**: set to **true** / **false** based on whether this field is required

**value**: give your field a default value

As an example of these options in use, see [this template](https://www.co2.storage/templates/bafyreihgvw3qb57gw3pm4y6avrhiydft7eq22bhuet2f5kpcv52ab6afeu) with the schema:

```json
{
  "My Field": {
    "type": "string",
    "value": "Default Value",
    "mandatory": true
  }
}
```

## Select from Predefined Elements

Using the primitive type **list** or **array** allows you to give the user one or multiple predefined options to choose from. To set these options, add a field called **options** and give it an array (see example).

By default, the type allows only one option to be selected. To allow multiple options, add the optional field "multiple":true

For an example, look at [this template](https://www.co2.storage/templates/bafyreifr34d5qqj4n4g5qaiomn5avuhdct62dwioqzn2w6goltusjxrkwq) with the schema:

```json
{
  "Multiple Select": {
    "type": "array",
    "options":["Option 1", "Option 2", "Option 3"],
    "multiple":true
  }
}
```

## Nested Schemas

Say you have two cars in your garage, and a set of details you need to know about each car that you have already written a template for. By using a nested schema, you can re-use that template without having to hard code the details for each car.

You can copy the schema address of the [car template](https://www.co2.storage/templates/bafyreibvwvz4d66njv7n435i3sfnxu3mg2ipsxiit7wk6puwcw7h5zkfuu) by finding it in your CO2.Storage template browser and copy the upper CID:

<figure><img src="../.gitbook/assets/Screenshot 2023-06-07 at 4.40.11 PM.png" alt=""><figcaption></figcaption></figure>

The lower CID is the [template](data-model.md).

You can then use the schema CIT in a field of a new Template with the type **template** or **schema**. As an example, see this [garage template](https://www.co2.storage/templates/bafyreibdimefxwqr6455fopzm75jdictupe3oxptofpiaeiypzg5trqvmq) with the schema:

```json
{
  "First Car": {
    "type": "schema",
    "value": "bafyreidoknru24e7p24plnxnqnuyg2skji5zwni2acdk6d4l3ywqky2bka"
  },
  "Second Car": {
    "type": "schema",
    "value": "bafyreidoknru24e7p24plnxnqnuyg2skji5zwni2acdk6d4l3ywqky2bka"
  }
}
```

What if you want a user to be able to add multiple instances of a subschema, but you're not sure how many? Say there is an inventory of cars being managed and any number would be valid. Then you can use the types **template-list** or **schema-list**.&#x20;

This is shown in [this example](https://www.co2.storage/templates/bafyreig7mygcj553guquno5ghkd5iougswot3nv7huwn6r6vzt5sknvvse), with the schema code:

```json
{
  "Cars": {
    "type": "schema-list",
    "value": "bafyreidoknru24e7p24plnxnqnuyg2skji5zwni2acdk6d4l3ywqky2bka"
  }
}
```

The UI now allows a user to add as many instances as they would like, with the (+) and (-) buttons as shown. Any number of car instances greater than or equal to one will give a valid instance of this template type.

<figure><img src="../.gitbook/assets/Screenshot 2023-06-07 at 4.50.45 PM.png" alt=""><figcaption></figcaption></figure>
