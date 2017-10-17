FROM python:latest

RUN apt-get -yq update
RUN apt-get install -y linkchecker
RUN pip install awsie
ENTRYPOINT ["linkchecker"]