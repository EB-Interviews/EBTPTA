# Use an official Python runtime as a parent image
FROM python:3.13-slim

# Set the working directory in the container
WORKDIR /hello

# Copy the setup.py into the container at /hello
COPY setup.py .

# Install any needed dependencies
RUN pip install .

# Copy the /hello (app code) into container /hello dir
COPY hello/ ./hello/

# Make port 5000 available to the world outside this container
EXPOSE 5000

# Define env var
ENV FLASK_APP=hello

# Run python app when the container launches
CMD ["flask", "run", "--host=0.0.0.0", "--port", "5000"]
