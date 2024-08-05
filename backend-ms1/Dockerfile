# Use a lightweight Alpine OpenJDK runtime as a base image
FROM openjdk:17


# Copy the packaged JAR file from the build stage
COPY target/*.jar app.jar

COPY zyn/ssl/localhost/keystore.p12 ssl/localhost/keystore.p12
COPY zyn/ssl/prod/keystore.p12 ssl/prod/keystore.p12

# Expose the port
EXPOSE 8036

# Define the command to run the application
CMD ["java", "-jar", "app.jar"]
