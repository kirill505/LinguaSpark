FROM tiangolo/uvicorn-gunicorn:python3.10

RUN mkdir /backend

COPY requirements.txt /backend

WORKDIR /backend

RUN pip install --upgrade pip

RUN pip install -r requirements.txt

COPY . /backend

EXPOSE 8000

CMD ["uvicorn", "server:app", "--host", "0.0.0.0", "--port", "8000"]