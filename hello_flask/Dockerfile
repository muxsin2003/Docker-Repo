FROM python:3.8-slim
WORKDIR /app
RUN apt-get update && apt-get install -y \
    pkg-config \
    default-libmysqlclient-dev \
    build-essential \
    && rm -rf /var/lib/apt/lists/*
COPY . .
RUN pip install flask mysqlclient
EXPOSE 5004
CMD ["python", "app.py"]
