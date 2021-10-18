FROM python:3.8

COPY . /app

RUN pip install -r /app/requirements.txt

EXPOSE 5000/tcp

CMD python /app/app.py