FROM python:3.7.3-stretch

## Step 1:
# Create a working directory

WORKDIR /app
## Step 2:
# Copy source code to working directory

COPY . app.py /app/
## Step 3:
# Install packages from requirements.txt
# hadolint ignore=DL3013

RUN pip install --upgrade pip  --no-cache-dir  &&\
    pip install --trusted-host pypi.python.org --requirement requirements.txt  --no-cache-dir
## Step 4:
# Expose port 80
EXPOSE 80
## Step 5:
# Run app.py at container launch
CMD [ "python", "app.py" ]