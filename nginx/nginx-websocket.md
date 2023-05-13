# Nginx for Websocket

Reference: [WebSocket proxying](https://nginx.org/en/docs/http/websocket.html)

**Example**: use a path-based URL like `www.domain.com/ws` to access your WebSocket server, instead of a subdomain.

```nginx
server {
    listen 80;
    server_name www.domain.com;

    location /ws {
        proxy_pass http://127.0.0.1:8765;
        proxy_http_version 1.1;
        proxy_set_header Upgrade $http_upgrade;
        proxy_set_header Connection "upgrade";
    }
}
```

This configuration file tells Nginx to listen on port 80 for requests to `www.domain.com`. When a request comes in with a path of `/ws`, Nginx will forward it to the WebSocket server running on `127.0.0.1:8765`.

The `proxy_http_version` directive tells Nginx to use HTTP/1.1 when proxying the request, and the `proxy_set_header` directives tell Nginx to upgrade the connection to a WebSocket connection.

Note that you will need to update your WebSocket client code to use the correct URL when connecting to the WebSocket server. In this case, the URL would be `ws://www.domain.com/ws`.