### 1. Build docker image

``` bash
docker build -t enodation/sample-web-page .
```

### 2. Check whether docker image is created or not

``` bash
docker images
```

### 3. Run container server

``` bash
docker run -d -p 80:80 enodation/sample-web-page:latest
```

### 4. Inspect the containers running in the system

``` bash
docker ps
```

### 5. Login to docker hub

``` bash
docker login -u sanppatil
```

### 6. Push image to docker hub

``` bash
docker push enodation/sample-web-page
```
