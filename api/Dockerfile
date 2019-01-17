FROM openjdk:8-jre


VOLUME ["/hygieia/logs"]

RUN mkdir /hygieia/config

EXPOSE 8080

ENV PROP_FILE /hygieia/config/dashboard.properties

WORKDIR /hygieia

COPY target/*.jar /hygieia
COPY dashboard.properties /hygieia/config/
CMD java -Djava.security.egd=file:/dev/./urandom -jar *.jar --spring.config.location=$PROP_FILE

