# remote-roku

## How To?
To communicate with a roku device you first need to discover the ip of device on your local network.<br/>
To do that you can make an ssdb request. roku-req.txt contains an example of an ssdb discovery request <br/>
The `ssdb.c` file will help you see ssdb trafic (ssdb might take sometime to respond) <br/>
once you have the ip and port (8060), you can communicate with the device through api end points <br/>


## Example

// returns the apps installed on the device <br/>
curl -X GET http://<ip>:<port>/query/apps <br/>


|> roku ip: https://developer.roku.com/docs/developer-program/discovery/external-control-api.md <br/>

|> Jaku is an example java project taken from the roku repo to discover devices and communicate with the device. <br/>
|> I analyzed the project refactored and documented it for easier read (all important code is located in /src) <br/>
