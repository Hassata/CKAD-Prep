# Scenario: Creating a Custom Web Application Image

## Objective

This scenario is designed to test your ability to containerize a web application using Docker. You will write a Dockerfile to package a simple Flask application, build the image, and run it locally.

## Application Setup

1.  **Download the Application**:
    *   This scenario uses the [Simple Flask App (basic-app)](https://github.com/pallets/flask/tree/main/examples/basic-app) from the official Flask examples.
    *   Navigate to the link above. You need the `app.py` file from that example.
    *   Create a file named `app.py` inside the current directory (`scenarios/custom-image-flask-app/`) and paste the content of the `app.py` from the `basic-app` example into it.

    *Alternatively, you can clone the entire `flask` repository and copy the `basic-app/app.py` file into this directory.*

2.  **Examine `app.py`**:
    *   This simple Flask application typically runs on port 5000.

## Steps to Containerize

1.  **Create/Review the `Dockerfile`**:
    *   The `Dockerfile` in this directory is designed to package the `app.py` you just created.
    *   It uses a Python base image, copies your `app.py`, installs Flask, exposes port 5000, and defines the command to run the application.
2.  **Build the Docker image**:
    *   Open your terminal in this directory (`scenarios/custom-image-flask-app/`).
    *   Use the `docker build` command to create an image from your Dockerfile. For example:
        ```bash
        docker build -t custom-flask-app:v1 .
        ```
3.  **Run the Docker container**:
    *   Use the `docker run` command to start a container from your image.
    *   Map port 5000 on your host to port 5000 in the container. For example:
        ```bash
        docker run -p 5000:5000 custom-flask-app:v1
        ```
4.  **Verify the application**:
    *   Open your web browser and navigate to `http://localhost:5000`.
    *   You should see the "Hello, World!" message from the Flask basic application. You can also use `curl http://localhost:5000`.

## Expected Outcome

*   A `Dockerfile` that successfully builds a container image for the provided `app.py`.
*   The Docker image can be built without errors.
*   A Docker container can be started from the image.
*   The Flask application is accessible at `http://localhost:5000` and functions as expected.