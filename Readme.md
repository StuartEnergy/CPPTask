# OCPP WebSocket App

## Requirements

* Provide instruction how to compile and launch application
* Implement using modern C++ features
* Unit test is not required but is a plus
* Usage of 3rd party libraries or Linux packages allowed

## Application

* Simple app menu (command line app using `cin/cout` is enough)
* After app starts it should connect to server using WebSocket
* If WebSocket connection was successful app should send `BootNotification`
* App user should be able to start transaction (`StartTransaction`)
* If charge transaction was successful user should be able to stop transaction (`StopTransaction`)

## Additional info

### Documentation

* [OCPP 1.6 Specification - JSON](OCPP1.6Specification-JSON.pdf) - document gives the information required to create a correct interoperable OCPP JSON implementation
* [OCPP 1.6 Specification - Edition](OCPP1.6Specification-Edition.pdf) - document defines the protocol used between a Charge Point and Central System

### Configuration

* OCPP JSON WebSocket URL - `ws://3.125.118.3:8080/steve/websocket/CentralSystemService/(chargeBoxId)`
* chargeBoxId - `[public_1, public_2, public_3]`

### WebSocket headers

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
* `meterStop` - `meterStart` + some value
