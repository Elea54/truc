FROM eclipse-temurin:23-jdk-alpine AS build

WORKDIR /usr/src/app

COPY Main.java .

RUN javac Main.java

FROM eclipse-temurin:23-jre-alpine

COPY --from=build /usr/src/app/Main.class .

CMD ["java", "Main"]