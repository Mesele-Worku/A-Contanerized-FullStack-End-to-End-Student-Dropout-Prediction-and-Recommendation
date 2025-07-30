FROM python:3.11-slim

WORKDIR /app

# Install dependencies to build xgboost
RUN apt-get update && apt-get install -y \
    build-essential \
    cmake \
    git \
    curl \
    && rm -rf /var/lib/apt/lists/*

COPY requirements.txt .

RUN pip install --default-timeout=300 --no-cache-dir -r requirements.txt -i https://pypi.org/simple

COPY . .

ENV PYTHONUNBUFFERED=1

CMD ["python", "sagemaker_model.py"]
