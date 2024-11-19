# Use a lightweight official image
FROM python:3.9-slim

# Set environment variables for better container behavior
ENV PYTHONUNBUFFERED=1 \
    PYTHONDONTWRITEBYTECODE=1

# Create and switch to a non-root user for security
RUN useradd -ms /bin/bash appuser
USER appuser

# Set the working directory inside the container
WORKDIR /app

# Copy only necessary files and minimize layers
COPY --chown=appuser:appuser web_service.py config.txt requirements.txt ./

# Install dependencies
RUN pip install --no-cache-dir -r requirements.txt

# Specify the default command to run the service
CMD ["python", "web_service.py"]
