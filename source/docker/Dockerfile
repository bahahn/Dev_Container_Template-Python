FROM python:3.9-slim

# gcc because of ipykernel on arm...
RUN apt-get update && apt-get install -y gcc && apt-get clean

ENV PIPENV_VENV_IN_PROJECT=1

# Copy Pipfile
COPY Pipfile ./

# Install pipenv
RUN pip install --no-cache-dir pipenv

# Create Pipfile.lock out of Pipfile
RUN pipenv lock && pipenv --clear && pipenv --rm

# Install pipenv in system environment
RUN pipenv sync --system

# Copy all files to /app directory
WORKDIR /app
COPY . .

CMD ["python", "./source/python/main.py"]