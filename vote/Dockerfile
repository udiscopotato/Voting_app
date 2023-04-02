FROM python:3.11-slim 

RUN apt update

WORKDIR /app

COPY . /app

RUN pip install -r requirements.txt

EXPOSE 80

CMD ["gunicorn","app:app","-b","0.0.0.0:80"]
