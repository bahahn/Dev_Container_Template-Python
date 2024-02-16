FROM python:3.9 

RUN pip install --no-cache-dir --upgrade pip && \
    pip install --no-cache-dir numpy pandas matplotlib tqdm

WORKDIR /app

COPY . .

CMD ["python", "./source/python/main.py"]