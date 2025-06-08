FROM python:3.8-slim

WORKDIR /app

COPY . /app

RUN pip install --no-cache-dir -r requirements.txt \
 && apt-get update \
 && apt-get install -y python3-tk python3-dev libsdl2-dev libsdl-image1.2-dev libsdl-mixer1.2-dev libsdl-ttf2.0-dev libsmpeg-dev libportmidi-dev libavformat-dev libswscale-dev libfreetype6-dev libjpeg-dev libpng-dev


CMD ["python", "main.py"]
