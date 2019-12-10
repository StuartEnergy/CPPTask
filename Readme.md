# Task

## Requirements

* Provide instuction how to compile and launch application
* Implement using modern C++ features
* Unit test is not required but is a plus
* Usage of 3rd party libraries or linux pachages allowed

## Application

* Simple app menu (commant line app using `cin/cout` is enougth)
* After app starts it shoud connect to server using websocket
* If websocket connection was successfull aop should send `BootNotification`
* App user should be able to start transaction (`StartTransaction`)
* If charge tracsaction was successfull user should be able to stop transaction (`StopTransaction`)
* App should display 

## Additional info

### Websocket headers

* `Sec-WebSocket-Key` - not required
* `Sec-WebSocket-Protocol` - `"ocpp1.6"`
* `Sec-WebSocket-Version` - `"13"`

### BootNotification properties

* Use your own

### BootNotification properties

* Use your own
