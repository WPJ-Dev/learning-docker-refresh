FROM python:3.14.2

COPY requirements.txt /app/requirements.txt
COPY webapp.py /app/webapp.py

WORKDIR /app

RUN pip3 install -r requirements.txt

ENTRYPOINT [ "python" ]
CMD [ "webapp.py" ]