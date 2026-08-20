FROM python:3.8-slim
WORKDIR /app
RUN apt-get update && apt-get install -y \
    gcc \
    python3-dev \
    libmariadb-dev \
    pkg-config
COPY . .
RUN pip install flask mysqlclient
EXPOSE 5004
CMD ["python", "app.py"]
