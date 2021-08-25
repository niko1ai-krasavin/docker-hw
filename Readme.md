### Using docker-compose.yml

Use a command like the following to start the registry container:
```
docker run -d -p 5000:5000 --restart=always --name registry registry:2
```

Create images from "apache" and "nginx" directories:
```
docker build -t localhost:5000/my_nginx:1.0 -t localhost:5000/my_nginx:latest .
docker build -t localhost:5000/my_apache:1.0 -t localhost:5000/my_apache:latest .
```

Save these images in the local registry:
```
docker push localhost:5000/my_nginx:latest
docker push localhost:5000/my_apache:latest
```

Run the docker-compose file for execution:
```
docker-compose up
```

Check the work and...

Terminate it with the command:

```
docker-compose down -v
```