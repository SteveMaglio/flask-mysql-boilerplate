###########################################
# Dockerfile for a simple python 


# Working from Python version 3.9
FROM python:3.9-alpine

# setting the working directory inside the container to /code
WORKDIR /code

#apk = homebrew for linux based docker containers
RUN apk add gcc musl-dev python3-dev libffi-dev openssl-dev

# copying the requirements.txt file from the host system to
# inside the container
COPY src/requirements.txt requirements.txt

# install requirements inside the container using pip
# requirements.txt automatically installs required libraries
RUN pip install -r requirements.txt

# expose port 4000 from the container
EXPOSE 4000

# tell the container to run the flask application
# CMD ["python", "src/app.py"]
# Bash/terminal translation
CMD ["python", "app.py"]

