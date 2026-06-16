# Define a base stage that uses the official python runtime base image
FROM python:3.9-slim

WORKDIR /app

# dependencies copy alag (cache optimization)
COPY requirements.txt .

RUN pip install --no-cache-dir -r requirements.txt \
    && pip install gunicorn

# baaki code copy
COPY . .

EXPOSE 80

CMD ["gunicorn", "app:app", "--bind", "0.0.0.0:80"]