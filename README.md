# Serverless Computing Lab – OpenFaaS Function

This project demonstrates serverless computing using OpenFaaS. A Python-based function is created, containerised using Docker, and deployed using the OpenFaaS framework.

The goal of this lab is to understand how Function-as-a-Service (FaaS) platforms allow developers to run code without managing servers or infrastructure.

--------------------------------------------------

FUNCTION IMPLEMENTATION

The function logic is implemented inside the file:

hello-python/handler.py

Example function:

def handle(event, context):
    return "Hello from OpenFaaS!"

This function receives an event and returns a simple response message when invoked.

--------------------------------------------------

PREREQUISITES

The following tools must be installed before deploying the function:

Docker
OpenFaaS (faasd)
faas-cli
Python 3
Git

--------------------------------------------------

DEPLOYMENT WORKFLOW

The OpenFaaS deployment process follows these steps.

1. Build the function container

faas-cli build -f stack.yaml

This command builds the Docker image for the function.

2. Push the image to a container registry

faas-cli push -f stack.yaml

This uploads the function image to the configured Docker registry.

3. Deploy the function to OpenFaaS

faas-cli deploy -f stack.yaml

This registers the function with the OpenFaaS gateway and makes it available for invocation.

4. Invoke the function

faas-cli invoke hello-python

Example output:

Hello from OpenFaaS!

--------------------------------------------------

ACCESS VIA BROWSER

Once deployed, the function can be accessed through the OpenFaaS gateway using the browser.

http://<VM_PUBLIC_IP>:8080/function/hello-python

--------------------------------------------------

TECHNOLOGIES USED

OpenFaaS  
Docker  
Python  
Azure Virtual Machine (Ubuntu 22.04)  
Git & GitHub  

--------------------------------------------------

KEY CONCEPTS DEMONSTRATED

Serverless computing  
Function-as-a-Service (FaaS)  
Containerised serverless functions  
OpenFaaS deployment workflow  
Docker container build and deployment  

--------------------------------------------------

AUTHOR

Kaustubh Kaushal  
Cloud Computing Lab
