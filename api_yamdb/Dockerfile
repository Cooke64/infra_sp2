FROM python:3.7-slim
LABEL owner="michael.soldatkin@gmail.com"

WORKDIR /app

COPY ..

RUN python -m pip install --upgrade pip
RUN pip3 install -r /requirements.txt --no-cache-dir

CMD ["gunicorn", "api_yamdb.wsgi:application", "--bind", "0:8000"]