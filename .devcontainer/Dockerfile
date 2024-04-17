FROM continuumio/miniconda3

WORKDIR /code

# Create the environment:
COPY ./environment.yml ./
RUN conda env create -f environment.yml

COPY ./src ./src

# Make RUN commands use the new environment:
RUN echo "conda activate main" >> ~/.bashrc
SHELL ["/bin/bash", "--login", "-c"]
