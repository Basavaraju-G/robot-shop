FROM quay.io/bgirriam/python:3.6

EXPOSE 8080
USER root

ENV INSTANA_SERVICE_NAME=payment

WORKDIR /app

COPY requirements.txt /app/

RUN pip install -r requirements.txt

COPY *.py /app/
COPY payment.ini /app/

#CMD ["python", "payment.py"]
CMD ["uwsgi", "--ini", "payment.ini"]

