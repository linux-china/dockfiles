Dockerfile for private repository
===============================
Private docker repository with local storage, search and proxy.

### Build
docker  build -t myregistry .

### Run
* docker run --name registrycache -d redis:2.8.17
* docker run -d -p 5000:5000 --link registrycache:registrycache -v /opt/registry/storage:/opt/registry -v /opt/registry/index:/opt/sqlitedb myregistry

### Usage

* docker pull myregistry.com:5000/php:5.6
* docker tag  myregistry.com:5000/php:5.6 php:5.6
