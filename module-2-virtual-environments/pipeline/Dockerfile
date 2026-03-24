# base Docker image that we will build on
FROM python:3.13.11-slim

RUN pip install pandas pyarrow

WORKDIR /code
COPY pipeline.py .
