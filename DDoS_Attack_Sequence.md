sequenceDiagram
box darkred Bad Guys
participant Attacker
participant BotNet
end

box darkblue Organization
participant WebServer
participant Firewall
end

 Firewall <<->> WebServer: Protects and Filters traffic
Note over BotNet,WebServer: Can be connected through employees<br>downloading malicous sofware
BotNet -x Firewall: Uses polymorphic malware to change its appearance and get past
Attacker ->> BotNet: Creates commands to <br>send to WebServer
BotNet ->> WebServer: Floods with a bunch of traffic<br>to prevent others from access
Note left of WebServer: Can cause it to crash
