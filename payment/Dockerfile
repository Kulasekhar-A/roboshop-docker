FROM python:3.9-alpine As builder
WORKDIR /app
COPY *.py .
COPY payment.ini .
COPY requirements.txt .
RUN pip install -r requirements.txt

FROM python:3.9-alpine
WORKDIR /app
EXPOSE 8080
COPY --from=builder /app /app/
RUN addgroup -S roboshop && adduser -S roboshop -G roboshop
RUN chown -R roboshop:roboshop /app
USER roboshop
CMD ["payment.ini"]
ENTRYPOINT ["uwsgi","--ini"]

# FROM python:3.9
# EXPOSE 8080
# WORKDIR /app
# COPY *.py .
# COPY payment.ini .
# COPY requirements.txt .
# RUN pip install -r requirements.txt
# CMD ["uwsgi","--ini","payment.ini"]

