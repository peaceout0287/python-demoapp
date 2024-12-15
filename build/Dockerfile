FROM python:3.9-slim-buster

LABEL Name="Python Flask Demo App" Version=1.4.2
LABEL org.opencontainers.image.source = "https://github.com/benc-uk/python-demoapp"

# Set the working directory
WORKDIR /app

# Copy the application files
COPY src/requirements.txt .
COPY src/ .

# Install dependencies
RUN pip install --no-cache-dir -r requirements.txt

# Expose the application port
EXPOSE 5000

# Start the Gunicorn server
CMD ["gunicorn", "-b", "0.0.0.0:5000", "run:app"]
