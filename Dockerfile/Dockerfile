# Use the latest version of Ubuntu
FROM ubuntu:latest

# Update the system and install Python 3.10 and pip
RUN apt-get update -y && \
    apt-get install -y software-properties-common && \
    add-apt-repository ppa:deadsnakes/ppa && \
    apt-get install -y python3.10 python3-pip && \
    apt install python3.10-venv -y

# Your other dependencies go here
# For example, if you need numpy, you would do:
RUN pip3 install numpy
RUN pip3 install pandas
RUN pip3 install matplotlib
RUN pip3 install torch torchvision torchaudio --index-url https://download.pytorch.org/whl/cpu

# Set the working directory in the container
WORKDIR /app

# Copy the current directory contents into the container at /app
COPY . /app

# Make port 80 available to the world outside this container
EXPOSE 80
# to build: wsl docker build . -t python_env
# wsl docker run -it --name my_container python_env:v1.0 /bin/bash
# wsl docker exec -it docker.io/library/python_env /bin/bash
