FROM python:3.8

ENV PYTHONDONTWRITEBYTECODE 1
ENV PYTHONUNBUFFERED 1

RUN apt-get update
RUN apt-get install -y build-essential
RUN apt-get install -y libpq-dev

WORKDIR /app/
COPY . /app/

RUN apt-get install python3-pip -y
RUN pip install --upgrade pip

COPY ./requeriments /requeriments
RUN pip install -r /requeriments/production.txt


COPY ./start.sh /start.sh
RUN sed -i 's/\r$//g' /start.sh
RUN chmod +x /start.sh


EXPOSE 8000
RUN chmod +x ./start.sh
CMD ["./start.sh"]
