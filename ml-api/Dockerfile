FROM python:3.11-slim
WORKDIR /app
COPY requirements.txt .
RUN pip install --default-timeout=300 --no-cache-dir -r requirements.txt -i https://pypi.org/simple
COPY . .
ENV PYTHONUNBUFFERED=1
EXPOSE 5000
CMD ["python", "sagemaker_model.py"]
