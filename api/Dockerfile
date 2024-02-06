FROM python:3.12.1-bullseye

RUN apt-get update && apt-get install -y \
    build-essential git curl

RUN pip install poetry && poetry config virtualenvs.create false

COPY ./api/pyproject.toml ./poetry.lock* ./
RUN poetry install

WORKDIR /opt/mnt
