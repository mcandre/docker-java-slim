# docker-java-slim - a slim Docker container having Java

# DOCKER HUB

https://registry.hub.docker.com/u/mcandre/docker-java-slim/

# ABOUT

docker-java-slim is a container for running Java classes, made smaller with a few techniques:

* Replace [ubuntu](https://registry.hub.docker.com/_/ubuntu/) with [alpine](https://registry.hub.docker.com/_/alpine/).
* Replace [Oracle JDK](http://www.oracle.com/technetwork/java/javase/downloads/jre7-downloads-1880261.html) with [OpenJDK](http://openjdk.java.net/).
* Drop [JDK](http://www.oracle.com/technetwork/java/javase/downloads/jdk7-downloads-1880260.html) for [JRE](http://www.oracle.com/technetwork/java/javase/downloads/jre7-downloads-1880261.html).
* Replace graphical JRE with [headless JRE](http://packages.ubuntu.com/search?keywords=openjdk-7-jre-headless&searchon=names).

# EXAMPLE

```
$ make
docker run --rm mcandre/docker-java-slim java -version
java version "1.7.0_75"
OpenJDK Runtime Environment (IcedTea 2.5.4) (Alpine 7.75.2.5.4-r0)
OpenJDK 64-Bit Server VM (build 24.75-b04, mixed mode)
docker images | grep mcandre/docker-java-slim | awk '{ print $(NF-1), $NF }'
122.7 MB
```

# REQUIREMENTS

* [Docker](https://www.docker.com/)

## Optional

* [make](http://www.gnu.org/software/make/)
* [Node.js](https://nodejs.org/en/) (for dockerlint)
