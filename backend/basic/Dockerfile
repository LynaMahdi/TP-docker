# Étape 1 : build
FROM eclipse-temurin:23-jdk-alpine AS build
WORKDIR /app
COPY Main.java .
RUN javac Main.java

# Étape 2 : runtime
FROM eclipse-temurin:23-jre-alpine
WORKDIR /app
COPY --from=build /app/Main.class .
CMD ["java", "Main"]
