# base Docker image that we will build on
FROM python:3.13.11-slim

# install uv
COPY --from=ghcr.io/astral-sh/uv:latest /uv /bin/ 

# set working directory in the container
WORKDIR /code
# get the code and dependencies into the container
COPY pyproject.toml .python-version uv.lock ./

# install dependencies with uv
RUN uv sync --frozen

# copy the script to the container. 1st name is source file, 2nd is destination
COPY ingest_data.py .

ENTRYPOINT ["uv","run","python","ingest_data.py"]