# Flask Application

This project is a simple Flask web application that serves a home page using an HTML template.

## Project Structure

```
flask-app
├── app.py
├── templates
│   └── index.html
├── requirements.txt
├── Dockerfile
└── README.md
```

## Requirements

To run this application, you need to have the following installed:

- Python 3.x
- Flask

You can install the required dependencies using the following command:

```
pip install -r requirements.txt
```

## Running the Application

To run the Flask application locally, execute the following command:

```
python app.py
```

The application will be accessible at `http://localhost:5000`.

## Docker

To build and run the Docker image for this application, follow these steps:

1. Build the Docker image:

   ```
   docker build -t flask-app .
   ```

2. Run the Docker container:

   ```
   docker run -p 5000:5000 flask-app
   ```

The application will be accessible at `http://localhost:5000` from your web browser.