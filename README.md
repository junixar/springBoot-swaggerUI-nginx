# Getting Started

# build docker image with the SpringBootApplication in it: 
./gradlew bootBuildImage

# start docker container: 
docker run -p 8080:8080 -t docker.io/library/test:0.0.1-SNAPSHOT

# change nginx configuration:

```
server {
        listen       8282;
        
        location / {
            root   html;
            index  index.html index.htm;
            proxy_pass http://localhost:8080;
        }
                
                
```

# call application direct:
http://localhost:8080/demo/test_string

# call application using nginx as a reverse-proxy:
http://localhost:8282/demo/nginx_test_string

# use swagger-ui:
http://localhost:8282/swagger-ui.html



