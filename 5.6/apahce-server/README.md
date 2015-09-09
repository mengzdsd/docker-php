# docker-apache-php
Build a docker opensuse image which include apache&amp;php.  

#### Packages version
- apache2          2.4.16 
- apache2-prefork  2.4.16
- apache2-utils    2.4.16
- apache2-mod_php5 5.6.9
- php5             5.6.9
  
#### Usage
- Execute `docker run -p 80:80 -d mengzyou/docker-php:5.6-apache-server` and browser the host's IP address using http, you will get the php info.  
- Serving your actual content: `docker run -p 80:80 -v /mysite:/srv/www/htdocs/ -d mengzyou/docker-php:5.6-apache-server`
