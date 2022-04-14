### PHP web development using docker

Edit the php dockerfile to include php modules

### PHP XDEBUG launch config.

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

Path mapping should match docker-compose volume