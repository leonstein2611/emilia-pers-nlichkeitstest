# 1. Schritt: Bauen mit Maven und Java 17
FROM maven:3.8.4-openjdk-17 AS build
COPY . .
RUN mvn clean package -DskipTests

# 2. Schritt: Ausführen mit einem stabilen Java 17 Image
FROM eclipse-temurin:17-jre-jammy
# Wir holen die Datei aus dem Build-Ordner
COPY --from=build /target/*.jar app.jar
EXPOSE 8080
# Startbefehl
ENTRYPOINT ["java", "-jar", "app.jar"]