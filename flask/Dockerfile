FROM python:3.7-slim-stretch

RUN export DEBIAN_FRONTEND=noninteractive && apt-get update && apt-get install -y make
RUN apt-get -y install tesseract-ocr && apt-get -y install tesseract-ocr-fra
RUN apt install -y libsm6 libxext6

COPY . /flask
WORKDIR /flask

RUN mkdir /uploads

RUN pip install -r requirements.txt
EXPOSE 5000
CMD ["python3","-m","flask","run","--host=0.0.0.0"]
