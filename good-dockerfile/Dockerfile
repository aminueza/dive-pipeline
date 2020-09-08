FROM python:3.8.3-alpine3.11

COPY requirements.txt /tmp/

RUN pip install -r /tmp/requirements.txt

RUN adduser -D diveuser
WORKDIR /home/diveuser
USER diveuser

COPY fibonacci.py .

ENTRYPOINT [ "python", "./fibonacci.py" ]
CMD ["10"]
