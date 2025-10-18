# Dockerfile for Python Flask App
FROM python:3.11-slim

WORKDIR /app

# Copy dependency list and install
COPY requirements.txt .
RUN pip install --no-cache-dir -r requirements.txt

# Copy all project files
COPY . .

# Expose port (Flask default 5000)
EXPOSE 5000

# Run the Flask app
CMD ["python", "app.py"]

