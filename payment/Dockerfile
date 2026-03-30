FROM python:3.9
EXPOSE 8080
WORKDIR /app
COPY *.py .
COPY payment.ini .
COPY requirements.txt .
RUN pip install -r requirements.txt
CMD ["uwsgi","--ini","payment.ini"]

