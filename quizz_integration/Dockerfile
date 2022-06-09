FROM python:3.8

ENV PYTHONDONTWRITEBYTECODE=1
ENV PYTHONUNBUFFERED=1

WORKDIR /app
COPY . /app
RUN pip install poetry
RUN poetry export -o requirements.txt
RUN pip install -r requirements.txt

RUN chmod +x ./entrypoint.sh
ENTRYPOINT ./entrypoint.sh
