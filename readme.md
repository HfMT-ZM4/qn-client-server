# qn-client-server

## What's qn-client-server?
The qn.Client and qn.Server is a client-server pair written in java for network connectivite within the [Max](http://www.cycling74.com).
The classes use NIO to communicate both over TCP and UDP.

This code is written by Mathias Josefson by commission from Georg Hajdu.

## Compatibility
Written in Java8 and tested on Max version  8.1.5

Older Version compatibility:
- Possible but not verified

## Content
### Java externals:
- qn.Client: The client used for communicating with the server.
- qn.Server: The server used for accepting client connections and to communicate with clients.


## Installation:
Use Max 8's package manager or Drag the folder in one of Max's supported package folder.

## Logging
Logback is used for logging. The included logback.xml is already packaged in the jar-file and used. 
To override this configuration in the file max.java.config.txt specify the following:
max.jvm.option -Dlogback.configurationFile=<PATH_TO_FILE>
For example: 
/Users/Shared/Max\ 8/Packages/qn-client-server/logback.xml
Note that the space needs to be escaped.

## Local Auto-discovery
This is experimental functionality. If indented to be used the following configuration is needed:
max.jvm.option -Djava.net.preferIPv4Stack=true

## Overriding Version
For test purposes it is possible to override the version by setting: max.jvm.option -DQN_CLIENT_SERVER_VERSION=2.0.0.10