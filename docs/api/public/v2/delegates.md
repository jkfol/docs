---
title: Public Delegates API
---

# Public Delegates API

## List all delegates

### Endpoint

```
GET /api/delegates
```

### Query Parameters

| Name  | Type | Description                                   | Required |
|-------|:----:|-----------------------------------------------|:--------:|
| page  | int  | The number of the page that will be returned. | :x:      |
| limit | int  | The number of resources per page.             | :x:      |

### Response

```json
{
    "meta": {
        "count": 2,
        "pageCount": 99,
        "totalCount": 197,
        "next": "/v2/delegates?page=2",
        "previous": null,
        "self": "/v2/delegates?page=1",
        "first": "/v2/delegates?page=1",
        "last": "/v2/delegates?page=99"
    },
    "data": [
        {
            "username": "dark_jmc",
            "address": "D5PXQVeJmchVrZFHL7cALZK8mWWzjCaVfz",
            "publicKey": "02a9a0ac34a94f9d27fd9b4b56eb3c565a9a3f61e660f269775fb456f7f3301586",
            "votes": 0,
            "rank": 1,
            "blocks": {
                "produced": 0,
                "missed": 0,
                "last": {
                    "id": "12383884455448354193",
                    "timestamp": {
                        "epoch": 31784600,
                        "unix": 1521885800,
                        "human": "2018-03-24T10:03:20Z"
                    }
                }
            },
            "production": {
                "approval": "0.08",
                "productivity": "0.00"
            },
            "forged": {
                "fees:" 387586557812,
                "rewards": 19779600000000,
                "total": 20167186557812
            }
        }
    ]
}
```

## Retrieve a delegate

### Endpoint

```
GET /api/delegates/{id}
```

### Path Parameters

| Name | Type   | Description                                     | Required           |
|------|:------:|-------------------------------------------------|:------------------:|
| id   | string | The identifier of the delegate to be retrieved. | :white_check_mark: |

### Response

```json
{
    "data": {
        "username": "boldninja",
        "address": "DARiJqhogp2Lu6bxufUFQQMuMyZbxjCydN",
        "publicKey": "022cca9529ec97a772156c152a00aad155ee6708243e65c9d211a589cb5d43234d",
        "votes": 0,
        "rank": 29,
        "blocks": {
            "produced": 0,
            "missed": 0,
            "last": {
                "id": "10652480998435361357",
                "timestamp": {
                    "epoch": 32816112,
                    "unix": 1522917312,
                    "human": "2018-04-05T08:35:12Z"
                }
            }
        },
        "production": {
            "approval": "0.10",
            "productivity": "0.00"
        },
        "forged": {
            "fees:" 387586557812,
            "rewards": 19779600000000,
            "total": 20167186557812
        }
    }
}
```

## List all blocks of a delegate

### Endpoint

```
GET /api/delegates/{id}/blocks
```

### Path Parameters

| Name | Type   | Description                                     | Required           |
|------|:------:|-------------------------------------------------|:------------------:|
| id   | string | The identifier of the delegate to be retrieved. | :white_check_mark: |

### Query Parameters

| Name  | Type | Description                                   | Required |
|-------|:----:|-----------------------------------------------|:--------:|
| page  | int  | The number of the page that will be returned. | :x:      |
| limit | int  | The number of resources per page.             | :x:      |

### Response

```json
{
    "meta": {
        "count": 2,
        "pageCount": 29919,
        "totalCount": 59838,
        "next": "/v2/delegates/boldninja/blocks?page=2",
        "previous": null,
        "self": "/v2/delegates/boldninja/blocks?page=1",
        "first": "/v2/delegates/boldninja/blocks?page=1",
        "last": "/v2/delegates/boldninja/blocks?page=29919"
    },
    "data": [
        {
            "id": "10652480998435361357",
            "version": 0,
            "height": 3035318,
            "previous": "12548322724277171379",
            "forged": {
                "reward": 200000000,
                "fee": 0,
                "total": 200000000,
                "amount": 0
            },
            "payload": {
                "hash": "e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855",
                "length": 0
            },
            "generator": {
                "username": "boldninja",
                "address": "DARiJqhogp2Lu6bxufUFQQMuMyZbxjCydN",
                "publicKey": "022cca9529ec97a772156c152a00aad155ee6708243e65c9d211a589cb5d43234d"
            },
            "signature": "3044022034e754a3ff70adba6323517e1297c6a9f30176df2ac589661e9206fe60a203120220182c38da201fee20e803bb7725fe9618d6707547e6d7b757d4108f546934fe1c",
            "transactions": 0,
            "timestamp": {
                "epoch": 32816112,
                "unix": 1522917312,
                "human": "2018-04-05T08:35:12Z"
            }
        }
    ]
}
```

## List all voters of a delegate

### Endpoint

```
GET /api/delegates/{id}/voters
```

### Path Parameters

| Name | Type   | Description                                     | Required           |
|------|:------:|-------------------------------------------------|:------------------:|
| id   | string | The identifier of the delegate to be retrieved. | :white_check_mark: |

### Query Parameters

| Name  | Type | Description                                   | Required |
|-------|:----:|-----------------------------------------------|:--------:|
| page  | int  | The number of the page that will be returned. | :x:      |
| limit | int  | The number of resources per page.             | :x:      |

### Response

```json
{
    "meta": {
        "count": 2,
        "pageCount": 10,
        "totalCount": 19,
        "next": "/v2/delegates/boldninja/voters?page=2",
        "previous": null,
        "self": "/v2/delegates/boldninja/voters?page=1",
        "first": "/v2/delegates/boldninja/voters?page=1",
        "last": "/v2/delegates/boldninja/voters?page=10"
    },
    "data": [
        {
            "address": "D5mbS6mpP5UheuciNscpDLgC127kYjRtkK",
            "publicKey": "03f7e0b1ab14985990416f72ed0b206c20b9efa35156e4528c8ff749fa0eea5d5a",
            "username": null,
            "secondPublicKey": null,
            "balance": 400000000,
            "isDelegate": false
        }
    ]
}
```

## List all voter balances of a delegate

### Endpoint

```
GET /api/delegates/{id}/voters/balances
```

### Path Parameters

| Name | Type   | Description                                     | Required           |
|------|:------:|-------------------------------------------------|:------------------:|
| id   | string | The identifier of the delegate to be retrieved. | :white_check_mark: |

### Response

```json
{
    "data": 
        {
            "DKahhVFVJfqCcCmaQHuYzAVFKcWjBu5i6Z": 830302556723, 
            "DG92jj4vUW7SyxzM1VzkmQWMmgBGZVhrjb": 546053124588,
            "DN8nGwcNbE3YcnZYFp8uvvc9z4WWDbytWK": 35723441610, 
            "DMzBk3g7ThVQPYmpYDTHBHiqYuTtZ9WdM3": 3223337074367
        }
}
```

## Search for a delegate

### Endpoint

```
POST /api/delegates/search
```

### Path Parameters

| Name     | Type   | Description                                     | Required           |
| -------  |:------:|-------------------------------------------------|:------------------:|
| username | string | The username of the delegate to be retrieved.   | :white_check_mark: |

### Query Parameters

| Name  | Type | Description                                   | Required |
|-------|:----:|-----------------------------------------------|:--------:|
| page  | int  | The number of the page that will be returned. | :x:      |
| limit | int  | The number of resources per page.             | :x:      |

### Response

```json
{
    "meta": {
        "count": 1, 
        "pageCount": 1, 
        "totalCount": 1, 
        "next": null, 
        "previous": null, 
        "self": "/api/v2/delegates/search?limit=100&page=1", 
        "first": "/api/v2/delegates/search?limit=100&page=1", 
        "last": "/api/v2/delegates/search?limit=100&page=1"
   }, 
   "data": [
        {
            "username": "darkgalp", 
            "address": "DMzBk3g7ThVQPYmpYDTHBHiqYuTtZ9WdM3", 
            "publicKey": "037997a6553ea8073eb199e9f5ff23b8f0892e79433ef35e13966e0a12849d02e3", 
            "votes": 4635816197288, 
            "rank": 24, 
            "blocks": {
                "produced": 20903, 
                "missed": 297, 
                "last": {
                    "id": "13446764355635039339", 
                    "height": 1087121, 
                    "timestamp": {
                        "epoch": 56387658, 
                        "unix": 1546488858, 
                        "human": "2019-01-03T04:14:18.000Z"
                        }
                 }
            }, 
            "production": {
                "approval": 0.04, 
                "productivity": 98.6
            }, 
            "forged": {
                "fees": 246004413320, 
                "rewards": 4142200000000, 
                "totat": 4388204413320
            }
        }
    ]
}
```
