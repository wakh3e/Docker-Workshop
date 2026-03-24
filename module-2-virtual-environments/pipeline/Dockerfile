# base Docker image that we will build on
FROM python:3.13.11-slim

# set up our image by installing prerequisites; pandas in this case
RUN pip install pandas pyarrow

# set up the working directory inside the container
WORKDIR /code
# copy the script to the container. 1st name is source file, 2nd is destination
COPY pipeline.py .
