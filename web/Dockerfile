FROM python:3.8.5-slim-buster

COPY . /

RUN pip install -r requirements.txt
RUN python start.py
RUN python train.py
ENTRYPOINT ["/runserver.sh"]