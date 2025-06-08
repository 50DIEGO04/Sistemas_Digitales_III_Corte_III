# 🎮 Tarea 9 – Juegos Clásicos en Python con Docker

Este proyecto corresponde a la **Tarea 9** de la asignatura **Sistemas Digitales III**, donde se desarrollaron tres juegos clásicos en Python usando Pygame: **Naves**, **Tanques** y **Tetris**. Cada uno fue estructurado en su propia carpeta, con entorno virtual independiente y contenedor Docker funcional.

---

## 📁 Estructura de Carpetas

```bash
Tarea_9/
├── naves/
│   ├── main.py
│   ├── assets/
│   │   ├── images/
│   │   └── sounds/
│   ├── venv/
│   └── Dockerfile
├── tanques/
│   ├── main.py
│   ├── assets/
│   ├── venv/
│   └── Dockerfile
├── tetris/
│   ├── main.py
│   ├── assets/
│   ├── venv/
│   └── Dockerfile
└── Imagenes/
```

---

## ✅ 1. Activación de entorno virtual y dependencias

Se creó un entorno virtual con `venv` y se instaló `pygame==2.5.2`. En la imagen se puede observar el proceso completo para el juego de naves:

![Activación entorno virtual](Imagenes/Activación_instalación_Venv_naves.png)

---

## ⬇️ 2. Clonación y preparación del código

Se utilizó `sparse-checkout` para clonar solo las carpetas necesarias desde GitHub, evitando descargas innecesarias.

- **Clonación Naves**  
  ![Clonación Naves](Imagenes/Clonación_main.py_Naves.png)

- **Clonación Tanques**  
  ![Clonación Tanques](Imagenes/Clonación_main.py_tanques.png)

- **Clonación Tetris**  
  ![Clonación Tetris](Imagenes/Clonación_main.py_tetris.png)

---

## 🎨 3. Creación de imágenes y sonidos

Para generar las imágenes se utilizó **ImageMagick**, y los sonidos fueron creados con **Sox**.

- **Instalación de herramientas**  
  ![Instalación ImageMagick](Imagenes/Instalación_para_las_imagenes.png)  
  ![Instalación Sox](Imagenes/Instalación_para_los_audios.png)

- **Imágenes Naves**: Se generaron manualmente el jugador, los enemigos y el fondo.  
  ![Imágenes Naves](Imagenes/Creación_de_las_imagenes_naves.png)

- **Imágenes Tanques**: Se usaron rectángulos de distintos colores para el jugador, enemigos y balas.  
  ![Imágenes Tanques](Imagenes/Creacion_de_imagenes_Tanques.png)

- **Imágenes Tetris**: Se usó un degradado para el fondo.  
  ![Imágenes Tetris](Imagenes/Creación_de_la_imagen_Tetris.png)

- **Audios Naves**: Creación del láser y la explosión.  
  ![Audios Naves](Imagenes/Creación_de_los_audio_naves.png)

- **Audios Tanques**: Sonidos simples de prueba para acciones del juego.  
  ![Audios Tanques](Imagenes/Creacion_de_audio_Tanques.png)

---

## 📁 4. Organización de Carpetas

Después de clonar, los archivos se reorganizaron en sus respectivas carpetas (naves, tanques, tetris).

![Organización de carpetas](Imagenes/Creación_Carpetas.png)

---

## ▶️ 5. Verificación de código y ejecución

Se validó el funcionamiento del código con `main.py` dentro de cada carpeta.

- **Movimiento Naves**  
  ![Movimiento Naves](Imagenes/Movimiento_main.py_nave.png)

- **Movimiento Tanques**  
  ![Movimiento Tanques](Imagenes/Movimiento_main.py_tanques.png)

- **Movimiento Tetris**  
  ![Movimiento Tetris](Imagenes/Movimiento_main.py_tetris.png)

- **Vista general del código Naves**  
  ![Código Naves](Imagenes/nano_main.py_naves.png)

- **Vista general del código Tanques**  
  ![Código Tanques](Imagenes/nano_main.py_tanques.png)

- **Vista general del código Tetris**  
  ![Código Tetris](Imagenes/nano_main.py_tetris.png)

- **Juego Naves corriendo**  
  ![Naves corriendo](Imagenes/Juego_corriendo_naves.png)

- **Juego Tanques corriendo**  
  ![Tanques corriendo](Imagenes/Juego_corriendo.png)

- **Juego Tetris corriendo**  
  ![Tetris corriendo](Imagenes/Juego_corriendo_Tetris.png)

---

## 🐳 6. Creación de Dockerfile por juego

Se crearon Dockerfiles específicos por cada juego para contenerizar la aplicación.

- **Dockerfile Naves**  
  ![Dockerfile Naves](Imagenes/Creación_de_Dockerfile_nave.png)

- **Dockerfile Tanques**  
  ![Dockerfile Tanques](Imagenes/Creación_de_Dockerfile_tanques.png)

- **Dockerfile Tetris**  
  ![Dockerfile Tetris](Imagenes/Creación_de_Dockerfile_tetris.png)

---

## 📦 7. Construcción de Imágenes Docker

Cada imagen fue construida correctamente usando `docker build`.

- **Imagen Naves**  
  ![Build Naves](Imagenes/Creación_de_imagen_docker_naves.png)

- **Imagen Tanques**  
  ![Build Tanques](Imagenes/Creación_de_imagen_docker_tanques.png)

- **Imagen Tetris**  
  ![Build Tetris](Imagenes/Creación_de_la_imagen_Tetris.png)

---

## 🚀 8. Ejecución desde contenedor Docker

Se ejecutaron los contenedores con soporte gráfico para ver el juego corriendo desde Docker.

- **Contenedor Naves**  
  ![Contenedor Naves](Imagenes/Imagen_de_docker_corriendo_nave.png)

- **Contenedor Tanques**  
  ![Contenedor Tanques](Imagenes/Imagen_de_docker_corriendo_Tanques.png)

- **Contenedor Tetris**  
  ![Contenedor Tetris](Imagenes/Imagen_de_docker_corriendo_tetris.png)

---

## 🧠 Conclusiones

Esta tarea permitió consolidar:

- La estructura modular de videojuegos en Python.
- La creación de recursos gráficos y sonoros desde cero.
- El uso de entornos virtuales (`venv`).
- La construcción y ejecución de contenedores Docker con interfaz gráfica.

