FROM continuumio/miniconda3

WORKDIR /code

# Create the environment:
COPY ./environment.yml ./
RUN conda env create -f environment.yml

COPY ./src ./src

# # Make RUN commands use the new environment:
RUN echo "conda activate main" >> ~/.bashrc
SHELL ["/bin/bash", "--login", "-c"]

# # Demonstrate the environment is activated:
# RUN echo "Make sure pandas is installed:"
# RUN python -c "import pandas"

# CMD ["conda", "run", "-n", "main", "python3", "src/run.py"]
