# Allow IPv4 Forwarding In NodeJS CreateServer
When the node server is running, typing the url: `ip.address:port#` could not make a connect due to the port # is Listening under `tcp6` instead of `tcp`. </br>
To make the port listening using IPv4, the createserver method needs to be modified:
```javascript
http.createServer(function(req, res){
  //Handler code
}).listen(portNumber,"0.0.0.0");
```
By adding `"0.0.0.0"`in listen(), it allows IPv4 forwarding, thus entering the url:`ip.address:port#` will function correctly.
