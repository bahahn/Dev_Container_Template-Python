FROM python:3.9 

# RUN pip install --no-cache-dir --upgrade pip && \
#     pip install --no-cache-dir numpy pandas matplotlib tqdm

ENV PIPENV_VENV_IN_PROJECT=1

# Install & use pipenv
COPY Pipfile ./
RUN pip install pipenv
RUN pipenv lock
RUN pipenv sync --system

WORKDIR /app
COPY . .

CMD ["python", "./source/python/main.py"]