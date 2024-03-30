
## Pull the following docker images 
```bash
docker pull poridhi/codeserver-node:v1.1
docker pull poridhi/codeserver-python:v1.2
```


## Run the server container
```bash
docker run -it -p 8080:8080 poridhi/codeserver-node
docker run -it -p 7080:8080 poridhi/codeserver-python
```


## Build and Run the proxy-server 
```bash
docker build -t proxy-server .
docker run -it -p 8080:8080 proxy-server
```