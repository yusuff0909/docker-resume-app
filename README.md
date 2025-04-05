# Flask Resume App

## Ubuntu Deployment
```bash
# Install dependencies
sudo apt update
sudo apt install python3 python3-pip

# Create project directory
mkdir devops-portfolio
cd devops-portfolio

# Create virtual environment
python3 -m venv venv
source venv/bin/activate

# Install requirements
pip install -r requirements.txt

# Run the app
export FLASK_APP=app.py
python -m flask run --host=0.0.0.0 --port=5000
```

## Alpine Linux Deployment
```bash
# Install dependencies
apk update
apk add python3 py3-pip

# Create project directory
mkdir devops-portfolio
cd devops-portfolio

# Create virtual environment
python3 -m venv venv
source venv/bin/activate

# Install requirements
pip install -r requirements.txt

# Run the app
export FLASK_APP=app.py
python -m flask run --host=0.0.0.0 --port=5000
```

## Red Hat Enterprise Linux Deployment
```bash
# Install dependencies
sudo dnf update
sudo dnf install python3 python3-pip

# Create project directory
mkdir devops-portfolio
cd devops-portfolio

# Create virtual environment
python3 -m venv venv
source venv/bin/activate

# Install requirements
pip install -r requirements.txt

# Run the app
export FLASK_APP=app.py
python -m flask run --host=0.0.0.0 --port=5000
```

## Amazon Linux 2 Deployment
```bash
# Install dependencies
sudo yum update
sudo yum install python3 python3-pip

# Create project directory
mkdir devops-portfolio
cd devops-portfolio

# Create virtual environment
python3 -m venv venv
source venv/bin/activate

# Install requirements
pip install -r requirements.txt

# Run the app
export FLASK_APP=app.py
python -m flask run --host=0.0.0.0 --port=5000
```

## Docker Deployment
```bash
# Build the Docker image
docker build -t flask-resume-app .

# Run the container
docker run -d -p 5000:5000 flask-resume-app
```

## Dockerfile
Create a file named `Dockerfile` with the following content:
```dockerfile
FROM python:3.9-slim

WORKDIR /app

COPY . .

RUN pip install --no-cache-dir -r requirements.txt

EXPOSE 5000

ENV FLASK_APP=app.py

CMD ["python", "-m", "flask", "run", "--host=0.0.0.0", "--port=5000"]
```
