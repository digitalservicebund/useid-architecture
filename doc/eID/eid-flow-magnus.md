## Magnus flow

The following flow displays the "Magnus" eID flow. Magnus depicts the flow which applies for customers who already have an existing eID integration. 
See [this confluence page](https://digitalservicebund.atlassian.net/wiki/spaces/UseID/pages/438829109/Components+and+Flows) for more information.

```plantuml
@startuml
'https://plantuml.com/sequence-diagram

autonumber

user as "User" ->browser: open
browser as "Browser" -> eService: access webapp
eService -> server as "eID Server": start session
eService <-- server: return session identifier
note right: sessionId
eService -> eService: generate tcTokenURL
eService -> widget as "UseID Web-Widget": integrate and send tcTokenURL
note left: tcTokenURL
widget -> backend as "UseID Backend Server": get widget with QR Code
note left: tcTokenURL
backend -> backend: generate QR Code
note left: eIDClientURL
widget <-- backend: return widget
user <-- widget: display widget
user -> smartphone as "Smartphone": open camera
smartphone -> widget: scan QR Code
smartphone <-- widget: return URL to eID Client
note left: eIDClientURL
smartphone -> app as "UseID Mobile App (eID Client)": open
note left: tcTokenURL
app -> eService: get tcToken from tcTokenURL
app <-- eService: return tcToken
note right: tcToken
app -> server: establish connection
app <-- server: return list of requested data
note left: list of requested data
user <-- app: display requested data
user -> app: approve data request
app -> smartphone: access NFC reader
smartphone -> id as "ID card": scan NFC chip
smartphone <-- id: return encrypted identity data
note right: encrypted identity data
app -> server: send encrypted identity data
note right: encrypted identity data
server -> server: decrypt data
note left: encrypted identity data
app <-- server: return success
app -> backend: inform about success
note right: sessionId
backend -> widget: inform about success (via SSE)
note right: sessionId
widget -> browser: redirect to refreshAddress
note right: refreshAddress
browser -> eService: access success page
eService -> server: get identity data
note left: sessionId
eService <-- server: return identity data
note right: decrypted identity data
eService --> browser: refresh page
browser --> user: view page

@enduml
```