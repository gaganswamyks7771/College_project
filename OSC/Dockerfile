# Use lightweight Python base
FROM python:3.10-slim

WORKDIR /app

# Copy requirements and install dependencies
COPY OSC/requirements.txt .

RUN pip install --no-cache-dir -r requirements.txt

# Copy the Flask app
COPY OSC /app/OSC

# Expose port
EXPOSE 8000

# Run with gunicorn (production)
CMD ["gunicorn", "--bind", "0.0.0.0:8000", "OSC.app:app"]
