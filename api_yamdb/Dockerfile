FROM python:3.7-slim

RUN ls -a

RUN mkdir /app

COPY requirements.txt /app

RUN pip3 install -r /app/requirements.txt --no-cache-dir

COPY  ./ /app

WORKDIR app/

RUN ls -a

CMD ["gunicorn", "api_yamdb.wsgi:application", "--bind", "0:8000"] 
