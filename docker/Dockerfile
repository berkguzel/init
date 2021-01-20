FROM python:3.8-alpine

COPY . /app

WORKDIR /app

RUN pip install -r /app/requirements.txt --no-cache-dir

CMD ["python","main.py"]
