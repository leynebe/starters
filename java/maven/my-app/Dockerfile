FROM openjdk:8u212-jre-alpine3.9

# Copy the artifact to the runtime container
COPY jar/*.jar /run/my-app.jar

# Run the artifact
ENTRYPOINT exec java -jar /run/my-app.jar
