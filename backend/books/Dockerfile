FROM MAVEN: 3.9.8-opensdk-22 AS build
COPY . .
RUN nvm clean Package

FROM openjdk:17
EXPOSE 8761
COPY --from=build /target/eureka-0.0.1-SNAPSHOT.jar app.jar
ENTRYPOINT ["java", "-jar", "app.jar"]