FROM python:3.8

COPY . /app

RUN pip install -r /app/requirements.txt

EXPOSE 5000/tcp

CMD python /app/app.py


## build with:
# docker build -t freddo256/pxl .

## push
# docker push freddo256/pxl:latest

## run with:
# docker run -dp 5000:5000 hello-flask
