FROM openjdk:8-jdk-alpine
RUN  apk update && apk upgrade && apk add netcat-openbsd
RUN mkdir -p /usr/local/eurekasvr
RUN echo $JAVA_HOME
ADD @project.build.finalName@.jar /usr/local/eurekasvr/
ADD run.sh run.sh
RUN chmod +x run.sh
CMD ./run.sh