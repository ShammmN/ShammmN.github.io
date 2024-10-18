## DDoS Attack

```mermaid
sequenceDiagram
participant Attacker
participant BotNet
participant Firewall
participant WebServer
 
Attacker ->> BotNet: sends a command telling botnet to spam the server
BotNet --> Firewall: Spams webserver
note over BotNet,Firewall: The firewall catches these spams, blocking them
BotNet ->> WebServer: The firewall is often unable to bloack all spams
WebServer --> Attacker: The attacker successfully shut down the server 
```
## Documentation
First the attacker will send a command to the botnet to spam the webserver with requests.
Overloading the webserver with requests could cause it to crash due to being overwhelmed. 
The firewall is their to detect that these requests are attacks and spams then block them.
Sometimes however the firewall is unsuccessful in blocking all the spams. 
If enough spams are not blocked and reach the server it can get overwhelmed and crash. 