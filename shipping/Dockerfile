FROM maven:3.8.8
WORKDIR /app
COPY pom.xml .
RUN mvn clean package
COPY java .
COPY resources .
ENV CART_ENDPOINT=cart:8080 \
    DB_HOST=mysql
CMD [ "java", "-jar","shipping.jar"]