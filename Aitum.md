# Aitum API Methods

The base of Aitum related calls is `http://localhost:7777/aitum`.

## Rule related

Methods relating to Aitum's rules!

### Methods

### Get Rules

For getting a list of rules and their IDs.

#### Call

`GET /aitum/rules/`

#### Successful Response

Keys in the response refer to their name within Aitum, and the value as their internal ID.

```json
{
  "status": "OK",
  "data": {
    "Test": "TqpYRQEcpXv5hdux"
  }
}
```

### Trigger Rule

For triggering a rule in Aitum by its ID.

#### Call

`GET /aitum/rules/:ruleid`

#### Successful Response

Nothing interesting returned, but this indicates a successful run.

```json
{
  "status": "OK",
  "data": "OK"
}
```

## State related

Methods relating to Aitum's state system!

### Methods

### Get State Variables

For getting a list of state variables and their attached information.

#### Call

`GET /aitum/state/`

#### Successful Response

An array of state variables.

Type values are as follows:

| Type    | Value |
|---------|-------|
| Integer | 0     |
| Float   | 1     |
| String  | 2     |
| Boolean | 3     |


```json
{
  "status": "OK",
  "data": [
    {
      "_id": "Zw1cP6R3wrHVA0gZ",
      "name": "test3",
      "type": 2,
      "value": "asdasd"
    },
    {
      "_id": "o89r2sVwAYufiGnt",
      "name": "test",
      "type": 2,
      "value": "123"
    }
  ]
}
```