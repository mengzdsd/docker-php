# docker-php
Build docker images for php application.

##Tags and `Dockerfile` links
- [`5.6-cli-server` (5.6-cli-server/dockerfile)](https://github.com/mengzyou/docker-php/blob/master/5.6/cli-server/Dockerfile)  
- [`5.6-apache-server` (5.6-apache-server/dockerfile)](https://github.com/mengzyou/docker-php/blob/master/5.6/apache-server/Dockerfile)  

##How to use
###5.6-cli-server
Under your PHP application project directory.  
```bash
docker run -v `pwd`:/srv/app -P -d mengzyou/docker-php:5.6-cli-server  
```  

###5.6-apache-server
- Execute `docker run -p 80:80 -d mengzyou/docker-php:5.6-apache-server` and browser the host's IP address using http, you will get the php info.  
- Serving your actual content: `docker run -p 80:80 -v /mysite:/srv/www/htdocs/ -d mengzyou/docker-php:5.6-apache-server`  
