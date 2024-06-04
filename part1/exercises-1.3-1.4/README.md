## Exercises 1.3-1.4

### 1.3

1. `docker run -d -it --name secret devopsdockeruh/simple-web-service:ubuntu`

2. `docker exec -it secret bash`

3. `tail -f ./text.log`

Secret message is: 'You can find the source code here: https://github.com/docker-hy'

### 1.4

`docker run -it ubuntu sh -c 'apt-get update && apt-get install -y curl && while true; do echo "Input website:"; read website; echo "Searching.."; sleep 1; curl http://$website; done'
`