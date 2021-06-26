FROM python:3.7

ENV PYTHONUNBUFFERED 1
ENV SECRET_KEY 1234

WORKDIR /code

COPY requirements.txt /code/

RUN apt update && apt install -y \
    graphviz-dev  && \ 
    pip install -r requirements.txt \

COPY . /code/

CMD ["python", "manage.py", "runserver", "0.0.0.0:8000"]