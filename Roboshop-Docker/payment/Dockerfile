FROM python:3
EXPOSE 8080
WORKDIR /app
COPY payment.ini .
COPY *.py . 
COPY requirements.txt .
RUN pip install -r requirements.txt
CMD ["uwsgi", "--ini", "payment.ini"]