# ‼ Questions

## How do I get template fields to display in a given order?

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

## Troubleshooting

This project should be considered an alpha release. The [Filecoin Green](https://green.filecoin.io/) team is actively working on this project and welcomes contributions from the community.\
\
Should any problems arise, please reach out by emailing [green@filecoin.org](mailto:green@filecoin.org).
