FROM openjdk:8u212-jre-alpine3.9

# Copy the artifact to the runtime container
COPY target/app.jar /run/app.jar

# Run the artifact
ENTRYPOINT exec java -jar /run/app.jar
