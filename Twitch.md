# Twitch API Methods

The base of Twitch related calls is `http://localhost:7777/twitch`.

## Hype Train related

Methods relating to Hype Trains!

### Methods

### Get Hype Train

For getting the current state of the user's hype train.

#### Call

`GET /twitch/hypetrain/`

#### No active hype train response

Where active signifies if there currently is an active hype train.

```json
{
  "status": "OK",
  "data": {
    "active": false,
    "level": 0,
    "progress": 0
  }
}
```

#### Active hype train response

Where active signifies if there currently is an active hype train, level is your current train level and process is the percentage of your progress towards the next level.

```json
{
  "status": "OK",
  "data": {
    "active": true,
    "level": 1,
    "progress": 50
  }
}
```

### Note

After the Hype Train Ended trigger is fired in Aitum, the data will persist from the hype train for 2500ms to allow your application to pull data.
It is cleared after that time.


## Poll related

Methods relating to Polls!

### Methods

### Get Poll

For getting the current state of the user's poll.

#### Call

`GET /twitch/poll/`

#### No active poll response

Where active signifies if there currently is an active poll.

```json
{
  "status": "OK",
  "data": {
    "active": false,
    "title": null,
    "choices": []
  }
}
```

#### Active poll response

Where active signifies if there currently is an active poll.

```json
{
  "status": "OK",
  "data": {
    "active": true,
    "title": "This is a really cool poll title!",
    "choices": [
      {
        "text": "Here's an answer",
        "votes": 69
      },
      {
        "text": "Here's another answer",
        "votes": 420
      }
    ]
  }
}
```
