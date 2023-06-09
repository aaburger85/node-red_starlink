# node-red_starlink
A node-red flow using grpcurl and Dishy GRPC

There are a few things that need to be done prior to importing the flow into node-red. 
1. Install [GRPCurl](https://github.com/fullstorydev/grpcurl) > [Latest Release](https://github.com/fullstorydev/grpcurl/releases/tag/v1.8.7)
2. Ensure the node-red process has access and permissions to execute GRPCurl. This can be done through a few ways, if running in docker, pass the bin file to the node-red install
- one way would be to add the path to GRPCurl to the container via a volume: e.g. `-v /usr/bin/grpcurl:/opt/grpcurl`
3. download the flow.json and import into node-red.
4. Adapt the exec node to use the path available to access the GRPCurl binary from node-red
5. create a link out to an MQTT output and connect the end nodes on the far right to an MQTT broker output connection. (would suggest using Home Assistant as a telemetry processing and consumption engine for testing as the discovery and topics are all created for consumption in HA). 
