#
# Build stage
#
FROM maven:3.8-openjdk-11 AS build
workdir /app1
copy . .
RUN mvn clean install -DskipTests
#
# Package stage
#
FROM openjdk:11-jre-slim
COPY --from=build /app1/target/springboot2-jpa-crud-example-0.0.1-SNAPSHOT.jar demo.jar
EXPOSE 81
ENTRYPOINT ["java","-jar","demo.jar"]
