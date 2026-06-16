# Define a base stage that uses the official python runtime base image
FROM python:3.11-slim AS base

WORKDIR /app

copy requirements.txt

RUN pip install --no-cache-dir -r requirements.txt && pip install gunicorn

COPY . .

EXPOSE 80

CMD ["gunicorn", "app:app", "--bind", "0.0.0.0:80"]
