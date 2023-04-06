FROM maven:3.8.4-openjdk-17-slim AS build

WORKDIR /lab3_java

#Dependency
COPY pom.xml .

RUN mvn dependency:go-offline

#Code
COPY src/ /lab3_java/src/

RUN mvn package -DskipTests

FROM openjdk:17-slim

WORKDIR /lab3_java

COPY --from=build /lab3_java/target/lab3-0.0.1-SNAPSHOT.jar /lab3_java/app.jar

EXPOSE 8080

CMD ["java", "-jar", "app.jar"]


