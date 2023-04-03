FROM python:3.10-slim-buster

# Dependancies
COPY requirements/backend.in .

RUN pip install --no-cache-dir -r backend.in

#Code
COPY . /lab3_python

WORKDIR /lab3_python

CMD ["uvicorn", "spaceship.main:app", "--host=0.0.0.0", "--port=8080"]