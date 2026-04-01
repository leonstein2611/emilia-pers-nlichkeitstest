FROM eclipse-temurin:17-jdk-jammy
COPY . .
RUN ./mvnw clean package -DskipTests
ENTRYPOINT ["java","-jar","target/quiz-0.0.1-SNAPSHOT.jar"]