# node-red_starlink
A node-red flow using grpcurl and Dishy GRPC

There are a few things that need to be done prior to importing the flow into node-red. 
1. Install [GRPCurl](https://github.com/fullstorydev/grpcurl)
2. Ensure the node-red process has access and permissions to execute GRPCurl. This can be done through a few ways, if running in docker, pass the bin file to the node-red install
3. download the flow.json and import into node-red.
4. Adapt the exec node to use the path available to access the GRPCurl binary from node-red
5. create a link out to an MQTT output and connect the end nodes to an MQTT broker. (would suggest using Home Assistant as a telemetry processing and consumption engine. 
