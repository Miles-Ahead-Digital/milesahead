FROM openjdk:12.0.2

EXPOSE 8888

RUN yum install jq -y

ADD ./target/*.jar app.jar

ENTRYPOINT ["java","-jar","/app.jar"]
