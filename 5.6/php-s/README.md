##Description
This image is used for development PHP application, run the application with PHP built-in web server.

##How to use
Under your PHP application project directory.  
```bash
docker run -v `pwd`:/srv/app -P -d mengzyou/docker-php:5.6-php-s  
```  
