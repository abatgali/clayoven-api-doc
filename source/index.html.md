---
title: API Reference

toc_footers:
  # - <a href='#'>Sign Up for a Developer Key</a>
  # - <a href='https://github.com/slatedocs/slate'>Documentation Powered by Slate</a>

includes:
  - errors

search: true

code_clipboard: true

meta:
  - name: Clay Oven API
    content: Documentation for the Clay Oven API
---

# Introduction

Welcome to the Clay Oven API! You can access our endpoints to get information on various menu items, orders, and users in our database.

# Menu

## Get all items

> The request returns JSON structured like this:

```json
[
  {
    "itemID": 1,
    "name": "Samosa",
    "price": 4.99,
    "description": "Crispy turnovers stuffed with spiced potatoes.",
    "glutenFree": false,
    "veganPrep": false
  },
  {
    "itemID": 2,
    "name": "Paneer Pakora",
    "price": 4.99,
    "description": "Deep fried garbanzo beans batter mix stuffed with Indian homemade cheese.",
    "glutenFree": false,
    "veganPrep": false
  }
]
```

This endpoint retrieves all menu items.

### HTTP Request

`GET http://clayovenindy.com/api/items`

<!-- ### Query Parameters

Parameter | Default | Description
--------- | ------- | -----------
include_cats | false | If set to true, the result will also include cats.
available | true | If set to false, the result will include kittens that have already been adopted. -->

## Get items of a specific category

> The request returns JSON structured like this:

```json
[
  {
    "id": 1,
    "category" : "Appetizers",
    "items": 
    [
      {
        "itemID": 1,
        "name": "Samosa",
        "price": 4.99,
        "description": "Crispy turnovers stuffed with spiced potatoes.",
        "glutenFree": false,
        "veganPrep": false
      },
      {
        "itemID": 2,
        "name": "Paneer Pakora",
        "price": 4.99,
        "description": "Deep fried garbanzo beans batter mix stuffed with Indian homemade cheese.",
        "glutenFree": false,
        "veganPrep": false
      }
    ]
  }
]
```

This endpoint retrieves all items in a given category.

### URL Parameters

Parameter | Description
--------- | -----------
id | The id of the category

### HTTP Request

`GET http://clayovenindy.com/api/categories/{id}/items`



<!-- ### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of the menu item to retrieve -->

## Get a specific item


> The request returns JSON structured like this:

```json
{
    "itemID": 2,
    "name": "Paneer Pakora",
    "price": 4.99,
    "description": "Deep fried garbanzo beans batter mix stuffed with Indian homemade cheese.",
    "glutenFree": false,
    "veganPrep": false
}
```

This endpoint retrieves a specific menu item.

### HTTP Request

`GET http://clayovenindy.com/api/items/{id}`

### URL Parameters

Parameter | Description
--------- | -----------
id | The id of the menu item to retrieve

## Get all categories


> The request returns JSON structured like this:

```json
[
  {
    "id": 1,
    "category" : "Appetizers"
  },
  {
    "id": 2,
    "category" : "Biryanis"
  },
  {
    "id": 3,
    "category" : "Seafood"
  },
  {
    "id": 4,
    "category" : "Desserts"
  }
]
```

This endpoint retrieves all categories.

### HTTP Request

`GET http://clayovenindy.com/api/categories`


# Orders

# Users
