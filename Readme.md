# OCPP Websocket App

## Requirements

* Provide instuction how to compile and launch application
* Implement using modern C++ features
* Unit test is not required but is a plus
* Usage of 3rd party libraries or linux packages allowed

## Application

* Simple app menu (commant line app using `cin/cout` is enough)
* After app starts it shoud connect to server using websocket
* If websocket connection was successfull aop should send `BootNotification`
* App user should be able to start transaction (`StartTransaction`)
* If charge tracsaction was successfull user should be able to stop transaction (`StopTransaction`)

## Additional info

### Websocket headers

* `Sec-WebSocket-Key` - not required
* `Sec-WebSocket-Protocol` - `"ocpp1.6"`
* `Sec-WebSocket-Version` - `"13"`

### BootNotification properties

* Use your own

### StartTransaction properties

* `connectorId` - `1`
* `idTag` - use random string, generated on app start
* `meterStart` - use random number

### StopTransaction properties

* `idTag` - Same tag as in `StartTransaction`
* `idTag` - Same tag as in `StartTransaction`
* `meterStop` - `meterStart` from `StartTransaction` + some value
