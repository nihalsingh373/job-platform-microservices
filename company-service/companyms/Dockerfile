FROM eclipse-temurin:21-jre
WORKDIR /app
COPY target/companyms-0.0.1-SNAPSHOT.jar app.jar
EXPOSE 8080
ENTRYPOINT ["java","-jar","app.jar"]
