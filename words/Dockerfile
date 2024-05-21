FROM maven:3.9.6-eclipse-temurin-8 as build
COPY . /root
WORKDIR /root
RUN --mount=type=cache,target=/root/.m2 mvn verify
CMD java -jar ./target/words.jar

FROM eclipse-temurin:8u412-b08-jre
RUN adduser --system stefan
USER stefan
COPY --from=build /root/target /home/stefan
EXPOSE 8080
CMD java -jar /root/words.jar