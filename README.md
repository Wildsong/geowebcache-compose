# geowebcache-compose
Geoserver in Docker Compose, set up to work only as a tile cache

## Configure it

I think there will be a configuration file somewhere.
XML yick

## Start it up

docker-compose up -d

Remember, you are really running the service on a Tomcat instance, so it will want the path 
to be complete with the service name, for example, yours might show up at
https://localhost:8080/geowebcache
and mine might show up at
https://geowebcache.wildsong.biz/geowebcache

I can see traffic on port 443 from my browser.
