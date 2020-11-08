# Product

## JSON Example
```json
{
  "version": "0.0.1",
  "type": "https//openmarketplace.org/spec/types/product",
  "product": {
    "information": {
      "id": 1,
      "name": "einfachIOTA Magazin - IOTA in der Industrie",
      "description": "Das zweite einfachIOTA Magazin mit dem Motto: IOTA in der Industrie.",
      "image": "/products/eimag_v2_de.png",
      "categories": [ "Magazine", "eiMag"],
      "price": {
          "amount": 9.00,
          "currency": "EUR"
      }
    }
  }
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
            "version": "0.0.1",
            "type": "https//openmarketplace.org/spec/types/product",
            "product": {
                "information": {
                    "id": 1,
                    "name": "einfachIOTA Magazin - IOTA in der Industrie",
                    "description": "Das zweite einfachIOTA Magazin mit dem Motto: IOTA in der Industrie.",
                    "image": "/products/eimag_v2_de.png",
                    "categories": [
                        "Magazine",
                        "eiMag"
                    ],
                    "price": {
                        "amount": 9.0,
                        "currency": "EUR"
                    }
                }
            }
        }
    ],
    "required": [
        "version",
        "type",
        "product"
    ],
    "properties": {
        "version": {
            "$id": "#/properties/version",
            "type": "string",
            "title": "The version schema",
            "description": "An explanation about the purpose of this instance.",
            "default": "",
            "examples": [
                "0.0.1"
            ]
        },
        "type": {
            "$id": "#/properties/type",
            "type": "string",
            "title": "The type schema",
            "description": "An explanation about the purpose of this instance.",
            "default": "",
            "examples": [
                "https//openmarketplace.org/spec/types/product"
            ]
        },
        "product": {
            "$id": "#/properties/product",
            "type": "object",
            "title": "The product schema",
            "description": "An explanation about the purpose of this instance.",
            "default": {},
            "examples": [
                {
                    "information": {
                        "id": 1,
                        "name": "einfachIOTA Magazin - IOTA in der Industrie",
                        "description": "Das zweite einfachIOTA Magazin mit dem Motto: IOTA in der Industrie.",
                        "image": "/products/eimag_v2_de.png",
                        "categories": [
                            "Magazine",
                            "eiMag"
                        ],
                        "price": {
                            "amount": 9.0,
                            "currency": "EUR"
                        }
                    }
                }
            ],
            "required": [
                "information"
            ],
            "properties": {
                "information": {
                    "$id": "#/properties/product/properties/information",
                    "type": "object",
                    "title": "The information schema",
                    "description": "An explanation about the purpose of this instance.",
                    "default": {},
                    "examples": [
                        {
                            "id": 1,
                            "name": "einfachIOTA Magazin - IOTA in der Industrie",
                            "description": "Das zweite einfachIOTA Magazin mit dem Motto: IOTA in der Industrie.",
                            "image": "/products/eimag_v2_de.png",
                            "categories": [
                                "Magazine",
                                "eiMag"
                            ],
                            "price": {
                                "amount": 9.0,
                                "currency": "EUR"
                            }
                        }
                    ],
                    "required": [
                        "id",
                        "name",
                        "description",
                        "image",
                        "categories",
                        "price"
                    ],
                    "properties": {
                        "id": {
                            "$id": "#/properties/product/properties/information/properties/id",
                            "type": "integer",
                            "title": "The id schema",
                            "description": "An explanation about the purpose of this instance.",
                            "default": 0,
                            "examples": [
                                1
                            ]
                        },
                        "name": {
                            "$id": "#/properties/product/properties/information/properties/name",
                            "type": "string",
                            "title": "The name schema",
                            "description": "An explanation about the purpose of this instance.",
                            "default": "",
                            "examples": [
                                "einfachIOTA Magazin - IOTA in der Industrie"
                            ]
                        },
                        "description": {
                            "$id": "#/properties/product/properties/information/properties/description",
                            "type": "string",
                            "title": "The description schema",
                            "description": "An explanation about the purpose of this instance.",
                            "default": "",
                            "examples": [
                                "Das zweite einfachIOTA Magazin mit dem Motto: IOTA in der Industrie."
                            ]
                        },
                        "image": {
                            "$id": "#/properties/product/properties/information/properties/image",
                            "type": "string",
                            "title": "The image schema",
                            "description": "An explanation about the purpose of this instance.",
                            "default": "",
                            "examples": [
                                "/products/eimag_v2_de.png"
                            ]
                        },
                        "categories": {
                            "$id": "#/properties/product/properties/information/properties/categories",
                            "type": "array",
                            "title": "The categories schema",
                            "description": "An explanation about the purpose of this instance.",
                            "default": [],
                            "examples": [
                                [
                                    "Magazine",
                                    "eiMag"
                                ]
                            ],
                            "additionalItems": true,
                            "items": {
                                "$id": "#/properties/product/properties/information/properties/categories/items",
                                "anyOf": [
                                    {
                                        "$id": "#/properties/product/properties/information/properties/categories/items/anyOf/0",
                                        "type": "string",
                                        "title": "The first anyOf schema",
                                        "description": "An explanation about the purpose of this instance.",
                                        "default": "",
                                        "examples": [
                                            "Magazine",
                                            "eiMag"
                                        ]
                                    }
                                ]
                            }
                        },
                        "price": {
                            "$id": "#/properties/product/properties/information/properties/price",
                            "type": "object",
                            "title": "The price schema",
                            "description": "An explanation about the purpose of this instance.",
                            "default": {},
                            "examples": [
                                {
                                    "amount": 9.0,
                                    "currency": "EUR"
                                }
                            ],
                            "required": [
                                "amount",
                                "currency"
                            ],
                            "properties": {
                                "amount": {
                                    "$id": "#/properties/product/properties/information/properties/price/properties/amount",
                                    "type": "number",
                                    "title": "The amount schema",
                                    "description": "An explanation about the purpose of this instance.",
                                    "default": 0.0,
                                    "examples": [
                                        9.0
                                    ]
                                },
                                "currency": {
                                    "$id": "#/properties/product/properties/information/properties/price/properties/currency",
                                    "type": "string",
                                    "title": "The currency schema",
                                    "description": "An explanation about the purpose of this instance.",
                                    "default": "",
                                    "examples": [
                                        "EUR"
                                    ]
                                }
                            },
                            "additionalProperties": true
                        }
                    },
                    "additionalProperties": true
                }
            },
            "additionalProperties": true
        }
    },
    "additionalProperties": true
}
```