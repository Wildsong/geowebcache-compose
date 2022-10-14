# geowebcache-compose

GeoWebCache in Docker Compose, set up to work only as a tile cache
This is a stripped-down version of [geoserver-compose](https://github.com/Wildsong/geoserver-compose), which includes a raft of other tools and plugins.

I am trying to replace MapProxy.

[Docs on GeoWebCache](https://www.geowebcache.org/docs/current/index.html) and its parent project, [GeoServer](https://docs.geoserver.org/)

[Source code](https://github.com/GeoWebCache/geowebcache) on the current snapshot

## TO DO

I want to be able to specify where the blobstore is written but
for now, it's in /tmp/defaultCache so just stick a volume there to make it persistent.

Default login will be geowebcache/secured. It's in the XML.
In /usr/local/tomcat/webapps/geowebcache/WEB-INF/users.properties.
You should fix this.

## Configure it

I think there will be a configuration files somewhere that need hacking.
XML yick!
I think they will end up in your geoserver volume in the 'gwc' subdirectory.

Edit your docker-compose.yml
Possibly edit your .env file?

## Build an image

    docker-compose build

## Start it up

    docker-compose up -d

The sample hello app should be visible, at http://localhost:8080/sample or http://cc-testmaps:8080/sample

Remember, you are really running the service on a Tomcat instance, so it will want the path 
to be complete with the service name, for example, yours might show up at
http://localhost:8080/geowebcache
and mine might show up at
http://cc-testmaps:8080/geowebcache

You should see a "Welcome to GeoWebCache" page there.


Is this README sketchy enough for you? At least I wrote one.
I'm learning.
Geoserver is a big project.

