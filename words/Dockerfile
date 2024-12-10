
FROM maven:alpine AS compiler
COPY  pom.xml .
RUN mvn verify

COPY src src
RUN mvn verify

FROM openjdk:8-jre-alpine
COPY --from=compiler /target/ target

CMD exec java -jar /target/*.jar

