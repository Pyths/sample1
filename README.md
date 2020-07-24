# sample1
Commands to run in terminal:
```shell
nano Dockerfile
```
Copy/Past in Dockerfile: (image openjdk:8u111-jdk-alpine taken from Docker Hub)

FROM openjdk:8u111-jdk-alpine 
WORKDIR app
COPY target/sample1-1.0.jar .
EXPOSE 8099
ENTRYPOINT ["java", "-jar", "sample1-1.0.jar"]

Build image:

```shell
sudo docker build -t sample1:1.0 .
```

Run image:

```shell
sudo docker run -p 8099:8099 sample1:1.0
```
