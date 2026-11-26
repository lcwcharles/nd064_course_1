FROM python:3.9
LABEL maintainer="Charles Lee"

# Set working directory
WORKDIR /app

# Copy application files
COPY ./techtrends .

# Install Python dependencies
RUN pip install --no-cache-dir -r requirements.txt

# Initialize database with predefined posts
RUN python init_db.py

# Expose application port
EXPOSE 3111

# Start the TechTrends application
CMD ["python", "app.py"]