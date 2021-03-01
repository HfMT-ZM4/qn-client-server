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

>  //If true, then data will be sent as raw bytes, as is done by sadam.tcpServer/sadam.tcpClient.<br/>
    protected boolean raw_bytes = false;<br/>
    //The CharSet to use when encoding data sent and received.<br/>
    protected String charset = "UTF-8";<br/>
    //The size of the buffer used.<br/>
    protected int buffer_size = 65536;<br/>
    //The size of the network buffer used.<br/>
    protected int network_buffer_size = 1048576;<br/>
    //Set if keep-alive should be used<br/>
    protected boolean keep_alive = true;<br/>
    //Set if keep-alive interval in seconds<br/>
    protected int keep_alive_interval_seconds = 30;<br/>
    //Set if keep-alive delay in seconds<br/>
    protected int keep_alive_delay_seconds = 0;<br/>
    //Set inactivity threshold for server taking down connection.<br/>
    protected int inactivity_threshold_seconds = 120;<br/>
    //Set to true and the client will try to reconnect when connection is lost.<br/>
    protected boolean reconnect = true;<br/>
    //Set to true and the client will disconnect completely after a given number of reconnect attempts.<br/>
    protected boolean keep_alive_disconnect = true;<br/>
    //Blocking timeout on the network<br/>
    protected int block_timeout_millis = 15;<br/>
    //Sends TimeStamps on every message.<br/>
    protected boolean send_timestamps = false;<br/>
    //Verbose logging is done<br/>
    protected boolean verbose = false;<br/>
    //Output is done over the high_priority outlet<br/>
    protected boolean high_priority = false;<br/>
    //Debugging is done.<br/>
    protected boolean debug = false;<br/>
    //includes the address in data when forwarded to max<br/>
    protected boolean include_address_in_data = false;<br/>
    //starts the udp client.<br/>
    protected boolean include_udp_protocol = false;<br/>
    //Name used for logging in.<br/>
    protected String name = null;<br/>
    //If udp is sent to other client is can be forwarded via server.<br/>
    protected boolean forward_udp_via_server = true;<br/>
    //The possibility to not forward data between clients.<br/>
    protected boolean forward_disabled = true;<br/>
    //The possibility to not include data to the client sending to all other clients<br/>
    protected boolean exclude_self_in_others = false;<br/>
    //Use multicast for publish and receive server address<br/>
    protected boolean multicast = false;<br/>
    //The multicast address<br/>
    protected String multicast_address = "228.5.6.7";<br/>
    //The multicast port<br/>
    protected int multicast_port = 6789;<br/>
    //Set if keep-alive delay in seconds<br/>
    protected int logoff_timeout_seconds = 1;<br/>
