FROM python:3.9
WORKDIR /app
COPY *.py .
COPY payment.ini .
COPY requirements.text .
ENV CART_HOST=cart \
    CART_PORT=8080 \
    USER_HOST=user \
    USER_PORT=8080 \
    AMQP_HOST=rabbitmq \
    AMQP_USER=roboshop \
    AMQP_PASS=roboshop123
CMD ["uswgi","--ini","payment.ini"]

