FROM python:3.9 

ENV PIPENV_VENV_IN_PROJECT=1

# Copy Pipfile
COPY Pipfile ./

# Install pipenv
RUN pip install pipenv

# Create Pipfile.lock out of Pipfile
RUN pipenv lock

# Install pipenv in system environment
RUN pipenv sync --system

# Copy all files to /app directory
WORKDIR /app
COPY . .

CMD ["python", "./source/python/main.py"]