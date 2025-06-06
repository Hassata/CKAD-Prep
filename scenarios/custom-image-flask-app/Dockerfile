# Use an official Python runtime as a parent image
FROM python:3.9-slim

# Set the working directory in the container
WORKDIR /app

# Copy the application files from the host to the container at /app
# This assumes the user has downloaded the 'basic-app' (e.g., app.py)
# into the 'scenarios/custom-image-flask-app/' directory where this Dockerfile is.
COPY . .

# Install Flask
RUN pip install Flask

# Make port 5000 available to the world outside this container
EXPOSE 5000

# Define environment variable for Flask.
# The user should ensure their Flask app's main file is named 'app.py'
# and is in the root of what's copied.
ENV FLASK_APP=app.py

# Run app.py when the container launches
CMD ["flask", "run", "--host=0.0.0.0"]