FROM python:3.10-slim-buster

COPY . /lab3_python

WORKDIR /lab3_python

RUN pip install --no-cache-dir -r ./requirements/backend.in

CMD ["uvicorn", "spaceship.main:app", "--host=0.0.0.0", "--port=8080"]