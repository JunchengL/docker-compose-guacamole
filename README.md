# docker-compose-guacamole
docker-compose file for guacamole quick start

this will build three containers for using guacamole application:
- guacd: guacd is a daemon process which is installed along with Guacamole and runs in the background, listening for TCP connections from the web application.
- guacamole: web application based on Tomcat
- mysql: database

## How to use
Clone this repo:
```
git clone git@github.com:JunchengL/docker-compose-guacamole.git
cd docker-compose-guacamole
```

Make a init directory to put database initiation script:
```
mkdir init
```

```
cd init
```

```
docker run --rm guacamole/guacamole /opt/guacamole/bin/initdb.sh --mysql > initdb.sql
```

Go back to main directory:
```
cd ..
```

Use docker-compose command to start application:
```
docker-compose up -d
```

Connect to application: 
```
http://DOCKER_HOST:8080/guacamole/
```

User and pwd:
```
guacadmin:guacadmin
```
