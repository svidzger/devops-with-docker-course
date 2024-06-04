## Exercises 1.9-1.10

### 1.9

`touch text.log`

`docker run -v "$(pwd)/text.log:/usr/src/app/text.log" devopsdockeruh/simple-web-service`


### 1.10

`docker run --rm -p 8080:8080 web-server`

http://localhost:8080/

