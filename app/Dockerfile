"""
The Dockerfile defines an application’s image content via one or more
build commands that configure that image. Once built, you can run the image in a container

This Dockerfile starts with a Python 3 parent image.
The parent image is modified by adding a new code directory.
The parent image is further modified by installing the Python requirements defined in the requirements.txt file.
"""
# pull official base image
FROM python:3.6.8-alpine

# set working directory
WORKDIR /usr/src/app

# set environment variables
ENV PYTHONDONTWRITEBYTECODE 1
ENV PYTHONUNBUFFERED 1

# install dependencies
RUN pip install --upgrade pip
COPY ./requirements.txt .
RUN pip install -r requirements.txt

# copy project
COPY . .