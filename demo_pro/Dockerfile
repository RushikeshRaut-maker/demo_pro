FROM  python:3.12-slim

WORKDIR /app

COPY requirements.txt .


RUN pip install --no-cache-dir -r requirements.txt

# Copy project files
COPY . .

# Collect static files (skip if not needed at build time)
# RUN python manage.py collectstatic --noinput

EXPOSE 8000

CMD ["gunicorn", "demo_pro.wsgi:application", "--bind", "0.0.0.0:8000"]