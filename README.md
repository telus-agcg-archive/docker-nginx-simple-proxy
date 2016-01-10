# NGINX Simple Proxy

Ever need a simple static proxy and didn't want to mess around nginx configuration? Look no further! This NGINX image image allows for you to set an environment variable as a static proxy.

# Usage

Fire up a container with an environment variable set to the URL you want to proxy to.

```sh
docker run \
  -p 80:80 \
  -e NGINX_PROXY_URL=http://www.google.com \
  technekes/nginx-simple-proxy
```

```sh
$ curl http://localhost:80
```

```html
<HTML><HEAD><meta http-equiv="content-type" content="text/html;charset=utf-8">
<TITLE>302 Moved</TITLE></HEAD><BODY>
<H1>302 Moved</H1>
The document has moved
<A HREF="http://www.google.com/">here</A>.
</BODY></HTML>
```
