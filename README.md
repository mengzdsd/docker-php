# docker-php
Build docker images for php application.

##Tags and `Dockerfile` links
- [`5.6-cli-server` (5.6-cli-server/dockerfile)](https://github.com/mengzyou/docker-php/blob/master/5.6/cli-server/Dockerfile)  

##How to use
###5.6-cli-server
Under your PHP application project directory.  
```bash
docker run -v `pwd`:/srv/app -P -d mengzyou/docker-php:5.6-cli-server  
```  
