FROM maven:3.9-eclipse-temurin-21

WORKDIR /app

COPY pom.xml .
COPY src ./src

RUN mvn -B -DskipTests package

EXPOSE 8080

CMD ["java", "-jar", "target/spring-mini-0.0.1-SNAPSHOT.jar"]
