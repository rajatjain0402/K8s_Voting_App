FROM python:3.9-slim

WORKDIR /app

# dependencies install
COPY requirements.txt .
RUN pip install --no-cache-dir -r requirements.txt

# code copy
COPY . .

CMD ["python", "worker.py"]