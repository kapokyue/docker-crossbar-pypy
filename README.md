# Crossbar Router
This is a simple docker container that will initialize a crossbar router with a static website running on it.

Start the container and you should be able to go to

    http://<ip_address>:8080
    
And you will see a web page that just says

    Server is running
    
WebSocket url should be

    ws://<ip_address>:8080/ws

The default realm is "realm1" and there is no authentication.

[Autobahn|JS](http://autobahn.ws/js/) is already installed in the page, you can use it to debug.

```javascript
AUTOBAHN_DEBUG = true;
var conn = new autobahn.Connection({
         url: 'ws://<ip_address>/ws',
         realm: 'realm1'
});
```

## License
MIT