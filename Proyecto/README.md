
# Chatbot DeepSeek en Pepper 🤖💬

Este repositorio documenta la implementación de un sistema conversacional integrado en el robot humanoide **Pepper**, utilizando la **API de DeepSeek** para generar respuestas mediante procesamiento de lenguaje natural. El sistema se compone de dos elementos principales:

- Un **servidor Flask** alojado dentro de un contenedor **Docker**.
- Un **cliente Python** ejecutado directamente en Pepper, encargado de capturar voz, enviarla al servidor y reproducir la respuesta generada.

---

## 🧠 Objetivo del proyecto

Integrar un chatbot basado en DeepSeek en el robot Pepper, de forma que sea capaz de:

1. Capturar comandos por voz.
2. Enviar el mensaje a un servidor externo.
3. Recibir y reproducir una respuesta generada por la API.
4. Ejecutarse de forma portátil, mediante contenedores Docker.

---

## 📁 Estructura del Proyecto

PepperChatBot/
├── client/
│ └── cliente_pepper.py
├── server/
│ ├── server.py
│ ├── requirements.txt
│ └── Dockerfile


---

## ⚙️ Requisitos previos

- Python 3.8+
- Pepper con SDK NAOqi accesible por SSH
- Docker instalado en el PC
- Conexión de red entre Pepper y el PC

---

## 🧰 Instalación y configuración

### 1. Crear entorno virtual

```bash
python3 -m venv PepperChatBot
source PepperChatBot/bin/activate

2. Instalar dependencias


pip install -r requirements.txt

Servidor Flask con DeepSeek

from naoqi import ALProxy
import requests
import time

PEPPER_IP = "192.168.1.100"  # Reemplaza con la IP de tu robot
SERVER_IP = "192.168.1.101"  # Reemplaza con la IP del servidor

tts = ALProxy("ALTextToSpeech", PEPPER_IP, 9559)
speech_recognition = ALProxy("ALSpeechRecognition", PEPPER_IP, 9559)

speech_recognition.setLanguage("English")
vocabulary = ["hello", "bye", "how", "you"]
speech_recognition.setVocabulary(vocabulary, False)

mic = ALProxy("ALAudioDevice", PEPPER_IP, 9559)
speech_recognition.subscribe("MyApplication")

tts.say("I am ready to talk.")

while True:
    time.sleep(1)
    # Simulación de escucha continua
    # En producción se captura con callbacks
    heard = input("Type the recognized word (simulación): ")
    if heard:
        response = requests.post(
            f"http://{SERVER_IP}:9559/chat",
            json={"message": heard}
        ).json()
        tts.say(response['reply'])

Accede a Pepper vía SSH:

ssh nao@<IP_PEPPER>
Sube el script cliente_pepper.py y ejecútalo:

python cliente_pepper.py
Verifica que el contenedor esté corriendo:

docker ps

Prueba manual desde terminal (opcional):

curl -X POST http://localhost:9559/chat -H "Content-Type: application/json" -d '{"message": "hello"}
