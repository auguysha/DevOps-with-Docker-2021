#
#
FROM maven:3-openjdk-11 AS build

EXPOSE 8080

WORKDIR /usr/src/app

COPY . .

RUN mvn -f /usr/src/app/pom.xml clean package
#
#
FROM openjdk:11-jre

COPY --from=build /usr/src/app/target/greeting-0.0.1-SNAPSHOT.jar /usr/local/lib/greeting.jar

ENTRYPOINT ["java","-jar","/usr/local/lib/greeting.jar"]

