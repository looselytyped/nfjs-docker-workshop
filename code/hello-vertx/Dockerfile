FROM openjdk:8u131-jre

RUN apt-get update \
    && apt-get install -y \
       netcat  \
    && apt-get clean

EXPOSE 9000

COPY wait.sh wait.sh
COPY ./build/libs/docker-workshop-0.0.1-SNAPSHOT-fat.jar /var/app.jar

CMD ["java", "-jar", "/var/app.jar"]
