# Use Python official image
FROM python:3.11-slim

# Set working directory inside the container
WORKDIR /app

# Copy dependencies file first
COPY requirements.txt .

# Install dependencies
RUN pip install --no-cache-dir -r requirements.txt

# Copy the rest of the code
COPY . .

# Open port 8000 to outside world
EXPOSE 8000

# Run the backend
CMD ["uvicorn", "main:app", "--host", "0.0.0.0", "--port", "8000", "--reload"]
