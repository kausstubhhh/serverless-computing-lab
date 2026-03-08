# Serverless Computing Lab

This project demonstrates a serverless function using **OpenFaaS**.

## Function

Language: Python

File structure:

hello-python/
handler.py
requirements.txt

stack.yaml – deployment configuration

## Deploy

Build function:

faas-cli build -f stack.yaml

Push image:

faas-cli push -f stack.yaml

Deploy function:

faas-cli deploy -f stack.yaml

Invoke function:

faas-cli invoke hello-python
