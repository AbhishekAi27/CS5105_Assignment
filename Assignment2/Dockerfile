# Dockerfile
FROM python:3.11-slim

# set workdir
WORKDIR /app

# copy requirements and app
COPY requirements.txt ./requirements.txt
RUN pip install --no-cache-dir -r requirements.txt

COPY . /app

# Expose streamlit port
EXPOSE 8501

# default command for streamlit
CMD ["streamlit", "run", "app.py", "--server.port=8501", "--server.address=0.0.0.0"]
