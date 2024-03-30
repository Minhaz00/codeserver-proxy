
### 1. Pull the following docker images 
```bash
docker pull poridhi/codeserver-node:v1.1
```
```bash
docker pull poridhi/codeserver-python:v1.2
```


### 2. Run the code-server containers
```bash
docker run -it -p 7080:8080 poridhi/codeserver-python
```

```bash
docker run -it -p 8080:8080 poridhi/codeserver-node
```


### 3. Build a docker image of the proxy-server and then 

```bash
docker build -t proxy-server .
```
### 4. Run a container based on that image

```bash
docker run -it -p 8080:8080 proxy-server
```

### 5. Check the codeserver

i. Visit http://localhost:8080/?folder=/app to check the node code-server </br>
ii. Visit http://localhost:7080/?folder=/app to check the python code-server

### 6. Finally visit the following links to check the proxy server
Visit: http://localhost:8000/node/?folder=/app 
</br>
This will redirect to node code-server
</br>


Visit: http://localhost:8000/python/?folder=/app 
</br>
This will redirect to python code-server

