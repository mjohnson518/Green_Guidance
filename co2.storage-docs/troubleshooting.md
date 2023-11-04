# ‼ FAQ

### How do I get template fields to display in a given order?

The default is to define your template schema as an unordered object, using curly brackets `{` :

```json
{
  "fieldA": {
    "type": "string",
    "required": true
  },
  "fieldB": {
    "type": "string",
    "required": true
  }
  ...
}
```

In the situation above, fields are not ordered. If you want fields to have an order, use an array instead of an object:

```json
[
  { 
    "field1": {
      "type": "string",
      "required": true
    }
  },
  { 
    "field2": {
      "type": "string",
      "required": true
    }
  }
  ...
]
```

In this case, the fields are ordered as an array: `[ field1, field2, ..]`

You can also implement arrays of arrays, if you prefer this style:

```json
[
  [ 
    "field1", {
      "type": "string",
      "required": true
    }
  ],
  ...
]
```

See the [Template Author's Guide](template-authors-guide.md) for more info on how to write templates.

### How does CO2.Storage deal with large files?

As of [v1.2.28](https://www.npmjs.com/package/@co2-storage/js-api), primitives of the `documents` and `images` types (see [Template Author's Guide](template-authors-guide.md)) are uploaded as file streams. Slices of these steams are uploaded to IPFS and assembled as IPLD DAGs.&#x20;

For working with large files using the UI, we recommend using the Chrome, Opera or Edge browsers. These browsers support `window.showSaveFilePicker()` which allows file streams.

### Authentication Error

```
code: 500,
message: 'Error whilst requesting "privateKeyToAccount" method. InvalidPrivateKeyError: Invalid Private Key, Not a valid string or uint8Array'
```

Make sure your PK starts with `0x` as described [here](setting-up-the-cli.md#set-up-environment-variables).



### Troubleshooting

This project should be considered an alpha release. The [Filecoin Green](https://green.filecoin.io/) team is actively working on this project and welcomes contributions from the community.\
\
Should any problems arise, please reach out by emailing [green@filecoin.org](mailto:green@filecoin.org).
