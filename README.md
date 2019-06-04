# docker-compose-guacamole
docker-compose file for guacamole quick start

this will build three containers for using guacamole 

## How to use
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
