FROM maven:alpine AS builder

COPY pom.xml .
RUN mvn verify

COPY src src
RUN mvn verify

FROM openjdk:8-jre-alpine

COPY --from=builder /target /target
COPY static static
CMD exec java -Xmx8m -Xms8m -jar target/words.jar
