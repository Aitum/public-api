# Aitum Public API

Documentation for [Aitum's](https://aitum.tv) Public API.

## Things of note

The public API will only run on your main Aitum instance, not on any workers (although this may change in the future).

These docs will be updated alongside new production releases of Aitum.

The API port is currently not configurable.

There is no authentication currently. **These calls are NOT intended to be made accessible outside your local network.**

As this API grows, there will be more additions that could put your local machine and network at risk of attack or RCE.

## Usage methodology

As Aitum is an event driven application, this API is intended to be used alongside existing functionality inside Aitum.

For example, using the Twitch Hype Train method as an example, a third party application would have no indication that a hype train had started.
This is where Aitum should be used to 'notify' the third party app that a change has occurred, be it via HTTP GET or other means (using shell exec).
Once the third party app receives this notification, it should then make an API call and grab the relevant information.


## Getting Started

The API base endpoint is `http://localhost:7777/`. 

For users of [Insomnia](https://insomnia.rest), you can import our API methods [here](api.json).

## Calls

- [Aitum](Aitum.md)
- [Twitch](Twitch.md)

## Response format

All responses will return in the following JSON form:

```json
{
  "status": "OK",
  "data": {}
}
```
