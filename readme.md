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

## Defaults
>   //The CharSet to use when encoding data sent and received.<br/>
    protected String __charset = "UTF-8";__<br/>
    //The size of the buffer used.<br/>
    protected int __buffer_size = 65536__;<br/>
    //The size of the network buffer used.<br/>
    protected int __network_buffer_size = 1048576__;<br/>
    //Set if keep-alive should be used<br/>
    protected boolean __keep_alive = true__;<br/>
    //Set if keep-alive interval in seconds<br/>
    protected int __keep_alive_interval_seconds = 30__;<br/>
    //Set if keep-alive delay in seconds<br/>
    protected int __keep_alive_delay_seconds = 0__;<br/>
    //Set inactivity threshold for server taking down connection.<br/>
    protected int __inactivity_threshold_seconds = 120__;<br/>
    //Set to true and the client will try to reconnect when connection is lost.<br/>
    protected boolean __reconnect = true__;<br/>
    //Set to true and the client will disconnect completely after a given number of reconnect attempts.<br/>
    protected boolean __keep_alive_disconnect = true__;<br/>
    //Blocking timeout on the network<br/>
    protected int __block_timeout_millis = 15__;<br/>
    //Sends TimeStamps on every message.<br/>
    protected boolean __send_timestamps = false__;<br/>
    //Verbose logging is done<br/>
    protected boolean __verbose = false__;<br/>
    //Output is done over the high_priority outlet<br/>
    protected boolean __high_priority = false__;<br/>
    //Debugging is done.<br/>
    protected boolean __debug = false__;<br/>
    //includes the address in data when forwarded to max<br/>
    protected boolean __include_address_in_data = false__;<br/>
    //starts the udp client.<br/>
    protected boolean __include_udp_protocol = false__;<br/>
    //Name used for logging in.<br/>
    protected String __name = null__;<br/>
    //If udp is sent to other client is can be forwarded via server.<br/>
    protected boolean __forward_udp_via_server = true__;<br/>
    //The possibility to not forward data between clients.<br/>
    protected boolean __forward_disabled = true__;<br/>
    //The possibility to not include data to the client sending to all other clients<br/>
    protected boolean __exclude_self_in_others = false__;<br/>
    //Use multicast for publish and receive server address<br/>
    protected boolean __multicast = false__;<br/>
    //The multicast address<br/>
    protected String __multicast_address = "228.5.6.7"__;<br/>
    //The multicast port<br/>
    protected int __multicast_port = 6789__;<br/>
    //Set if keep-alive delay in seconds<br/>
    protected int __logoff_timeout_seconds = 1__;<br/>
