# ─── Stage 1: Build ────────────────────────────────────────────────────────────
FROM maven:3.9.6-eclipse-temurin-11 AS builder

WORKDIR /app

# Copy project files
COPY pom.xml .
COPY src ./src

# Build the fat JAR (skipping tests for speed)
RUN mvn clean package -DskipTests

# ─── Stage 2: Run ──────────────────────────────────────────────────────────────
FROM eclipse-temurin:11-jre-alpine

WORKDIR /app

# Copy the built JAR from Stage 1
COPY --from=builder /app/target/bus-management-system.jar .

# Run the application
ENTRYPOINT ["java", "-jar", "bus-management-system.jar"]
