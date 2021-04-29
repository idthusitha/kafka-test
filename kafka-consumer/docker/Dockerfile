FROM adoptopenjdk/openjdk11:latest
VOLUME /tmp
ADD kafka-consumer-latest.jar app.jar
EXPOSE 5006
ENV JAVA_OPTS="-agentlib:jdwp=transport=dt_socket,server=y,suspend=n,address=5006 -Djava.security.egd=file:/dev/./urandom"
ENTRYPOINT java $JAVA_OPTS -jar /app.jar