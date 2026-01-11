# Install python 3.12
FROM python:3.12-slim

# Set working directory
WORKDIR /app

# Copy project files
COPY . .

# Install uv
RUN pip install uv

# Install dependencies
RUN uv sync

# App runs on port 8000
EXPOSE 8000

# Start FastAPI
CMD ["uv", "run", "fastapi", "dev", "main.py", "--host", "0.0.0.0"]
