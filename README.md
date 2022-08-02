# SSL Front-End Proxy With Automatic Free Certificate Management

Based on the upstream docker image, this one allows multiple proxy (or locations in general)

Adds another volume, "custom", where you have to put a custom.conf file which will be read by nginx. All proxy parameters are already set, your custom.conf can look something like this:

```
location /myserver {  proxy_pass http://172.17.0.1:8080/someserver; }
location /myfiles/ {  proxy_pass http://172.17.0.1:8888/nextcloud; }
```

Image doesn't have STSH, for the rest is identical to upstream

