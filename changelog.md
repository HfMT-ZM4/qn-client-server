 #Changelog
 ## 2020-08-03: Version 2.0.0.5
 # Added - Names are now checked for only alphanumeric characters.
 # Added - Client can now use the send_all to all other clients (including self).
 # Changed - no min version on the OS versions in package. 
 
 ## 2020-07-31: Version 2.0.0.4
 # Added - UDP communication
 # Added - client to client communication
 # Added - Server listen on all interfaces
 # Changed - code refactored
 # Fixed - bugs from previous versions
 # Fixed - stability of keep-alives
 # Fixed - shutdown of server.
 
 ## 2018-01-18: Version 1.0.0.1
 # Added - Symbols are maintained when sending. (MJ) 
 # Added - new line between items for all sending (not only buffered sending). (MJ)
 # Added - Configurable to output in high/low priority - attribute high_priority (true/false) (MJ)
 # Added - If no hostname is given then the host ip is taken (not localhost) (MJ)
 # Changed - block_timeout_seconds is changed to block_timeout_millis (MJ)
 # Changed - Timestamp separator token is now ":::" instead of ":" (MJ)
 ## 2017-07-02: Version 1.0.0.0
 # Added - First version, sending different formats, buffered sending, and client keep-alive+reconnect (MJ)
 #
 #