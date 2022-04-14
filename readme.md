### PHP web development using docker

Edit the php dockerfile to include php modules

### PHP XDEBUG launch config.


<pre>
{
    "name": "Listen for Xdebug",
    "type": "php",
    "request": "launch",
    "port": 9003,
    "stopOnEntry": true,
    "pathMappings": {
        "/var/www/html/": "${workspaceFolder}/www"
    },
},
</pre>

Path mapping should match docker-compose volume.

xdebug.ini

`xdebug.client_host=192.168.1.15`

IP should be set host ip where the docker container is running. (Use `host.docker.internal` for windows).
If change - have to rebuild the image.

