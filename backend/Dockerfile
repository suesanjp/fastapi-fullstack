FROM python:3.11-buster
ENV PYTHONUNBUFFERED=1
WORKDIR /code
COPY . .
RUN pip install poetry && \
  poetry install --without dev
CMD ["poetry", "run", "uvicorn", "app.main:app", "--host", "0.0.0.0", "--reload"]
