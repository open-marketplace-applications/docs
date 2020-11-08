# Shop

This specification describes a decentralized shop model. 

The Shop is simply a signet file with all kinds of information about the shop, like name, product list, and the owner. This file can be hosted on a decentralized network. That means it doesn't need to be deployed to on a server. Hosting a file is much cheaper than running a whole program. The file gets read and interpreted by the user. 

Users can discover new shops in marketplaces. 

For some services like sending a Mail or accept Paypal or Stripe, the shop needs to interact with a backend, to handle the logic.

## Object
```javascript=
{
    // Unique shop id
    id: String,
    // Owner of the shop as DID
    owner: String,
    // Name of the shop
    name: String
    // This url returns a list off all products as json
    product_list_url: String
    categories: Array
}
```


## JSON Example

```json
{
    "id": "950371f9-34a4-49dd-9d55-31160e2d1caf",
    "name": "A Sample Shop",
    "owner": "did:iota:shopowner",
    "product_list_url": "https://openmarketplace.org/shops/950371f9-34a4-49dd-9d55-31160e2d1caf",
    "categories": [
        "books",
        "magazines"
    ]
}
```

## JSON Schema
```json
{
    "$schema": "http://json-schema.org/draft-07/schema",
    "$id": "http://example.com/example.json",
    "type": "object",
    "title": "The root schema",
    "description": "The root schema comprises the entire JSON document.",
    "default": {},
    "examples": [
        {
            "id": "950371f9-34a4-49dd-9d55-31160e2d1caf",
            "name": "A Sample Shop",
            "owner": "did:iota:shopowner",
            "product_list_url": "https://openmarketplace.org/shops/950371f9-34a4-49dd-9d55-31160e2d1caf",
            "categories": [
                "books",
                "magazines"
            ]
        }
    ],
    "required": [
        "id",
        "name",
        "owner",
        "product_list_url",
        "categories"
    ],
    "properties": {
        "id": {
            "$id": "#/properties/id",
            "type": "string",
            "title": "The id schema",
            "description": "A Unique shop id",
            "default": "",
            "examples": [
                "950371f9-34a4-49dd-9d55-31160e2d1caf"
            ]
        },
        "name": {
            "$id": "#/properties/name",
            "type": "string",
            "title": "The name schema",
            "description": "Name of the shop",
            "default": "",
            "examples": [
                "A Sample Shop"
            ]
        },
        "owner": {
            "$id": "#/properties/owner",
            "type": "string",
            "title": "The owner schema",
            "description": "Owner of the shop as DID",
            "default": "",
            "examples": [
                "did:iota:shopowner"
            ]
        },
        "product_list_url": {
            "$id": "#/properties/product_list_url",
            "type": "string",
            "title": "The product_list_url schema",
            "description": "This url returns a list off all products as json.",
            "default": "",
            "examples": [
                "https://openmarketplace.org/shops/950371f9-34a4-49dd-9d55-31160e2d1caf"
            ]
        },
        "categories": {
            "$id": "#/properties/categories",
            "type": "array",
            "title": "The categories schema",
            "description": "List of categories, which describes the shop.",
            "default": [],
            "examples": [
                [
                    "books",
                    "magazines"
                ]
            ],
            "additionalItems": true,
            "items": {
                "$id": "#/properties/categories/items",
                "anyOf": [
                    {
                        "$id": "#/properties/categories/items/anyOf/0",
                        "type": "string",
                        "title": "The first anyOf schema",
                        "description": "An explanation about the purpose of this instance.",
                        "default": "",
                        "examples": [
                            "books",
                            "magazines"
                        ]
                    }
                ]
            }
        }
    },
    "additionalProperties": true
}
```
