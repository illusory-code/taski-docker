FROM python:3.12

WORKDIR /app

# Устанавливаем gunicorn
RUN pip install gunicorn==23.0.0

COPY requirements.txt .

RUN pip install -r requirements.txt --no-cache-dir

COPY . .

# Запускаем Gunicorn вместо development-сервера
CMD ["gunicorn", "--bind", "0.0.0.0:8000", "backend.wsgi"]