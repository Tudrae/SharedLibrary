# Flask Application new

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


To build and run the Docker image for this application, follow these steps:

1. Build the Docker image:

   docker build -t flask-app .

2. Run the Docker container:

   
   docker run -p 5000:5000 flask-app
The application will be accessible at `http://localhost:5000` from your web browser.
 
the deploy to kubenet section in deploy.yml file define as disable if you whant it to work on 
remote machin you need to replace it with the following phars:
name: Deploy to Kubernetes
  run: |
    kubectl apply -f flask-app/k3s/deployment.yaml
    kubectl apply -f flask-app/k3s/service.yaml
also in the kubeconfig within the remote machin you need also to point to the local k3s clusi
I think to do use the git action is the hardest way....
