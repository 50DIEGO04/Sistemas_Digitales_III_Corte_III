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

Se creó un entorno virtual por juego y se instaló `pygame==2.5.2`.

![Activación entorno virtual](Imagenes/Activación_instalación_Venv naves.png)

---

## ⬇️ 2. Clonación y preparación del código

Se utilizó `sparse-checkout` para clonar solo las carpetas requeridas desde GitHub.

- **Naves**  
  ![Clonación Naves](Imagenes/Clonación_main.py_Naves.png)

- **Tanques**  
  ![Clonación Tanques](Imagenes/Clonación_main.py_tanques.png)

- **Tetris**  
  ![Clonación Tetris](Imagenes/Clonación_main.py_tetris.png)

---

## 🎨 3. Creación de imágenes y sonidos

Las imágenes fueron creadas con **ImageMagick** y los sonidos con **Sox**.

- **Instalaciones**  
  ![Instalación imágenes](Imagenes/Instalación_para_las_imagenes.png)  
  ![Instalación audios](Imagenes/Instalación_para_los_audios .png)

- **Imágenes**  
  ![Imágenes Naves](Imagenes/Creación_de_las_imagenes_naves.png)  
  ![Imágenes Tanques](Imagenes/Creacion_de_imagenes_Tanques.png)  
  ![Imágenes Tetris](Imagenes/Creación_de_la_imagen_Tetris.png)

- **Audios**  
  ![Audios Naves](Imagenes/Creación_de_los_audio_naves.png)  
  ![Audios Tanques](Imagenes/Creacion_de_audio_Tanques.png)

---

## 📁 4. Organización de Carpetas

Se reubicaron correctamente los archivos y recursos multimedia.

![Carpetas](Imagenes/Creación_Carpetas.png)

---

## ▶️ 5. Verificación de código y ejecución

Cada juego fue ejecutado exitosamente desde su entorno virtual.

- **Movimiento en Código Naves**  
  ![Movimiento Naves](Imagenes/Movimiento_main.py_nave.png)

- **Movimiento Tanques**  
  ![Movimiento Tanques](Imagenes/Movimiento_main.py_tanques.png)

- **Movimiento Tetris**  
  ![Movimiento Tetris](Imagenes/Movimiento_main.py_tetris.png)

- **Vista de Código Naves**  
  ![Código Naves](Imagenes/nano_main.py_naves.png)

- **Vista de Código Tanques**  
  ![Código Tanques](Imagenes/nano_main.py_tanques.png)

- **Vista de Código Tetris**  
  ![Código Tetris](Imagenes/nano_main.py_tetris.png)

- **Ejecución Naves**  
  ![Juego Naves](Imagenes/Juego_corriendo_naves.png)

- **Ejecución Tanques**  
  ![Juego Tanques](Imagenes/Juego_corriendo_Tanques.png)

- **Ejecución Tetris**  
  ![Juego Tetris](Imagenes/Juego_corriendo_Tetris.png)

---

## 🐳 6. Creación de Dockerfile por juego

- **Dockerfile Naves**  
  ![Dockerfile Naves](Imagenes/Creación_de_Dockerfile_nave.png)

- **Dockerfile Tanques**  
  ![Dockerfile Tanques](Imagenes/Creación_de_Dockerfile_tanques.png)

- **Dockerfile Tetris**  
  ![Dockerfile Tetris](Imagenes/Creación_de_Dockerfile_tetris.png)

---

## 📦 7. Construcción de Imágenes Docker

Cada imagen Docker fue construida exitosamente.

- **Naves**  
  ![Imagen Naves](Imagenes/Creación_de_imagen_docker_naves.png)

- **Tanques**  
  ![Imagen Tanques](Imagenes/Creación_de_imagen_docker_tanques.png)

- **Tetris**  
  ![Imagen Tetris](Imagenes/Creación_de_la_imagen_Tetris.png)

---

## 🚀 8. Ejecución desde contenedor Docker

Cada contenedor fue ejecutado y el juego funcionó correctamente.

- **Contenedor Naves**  
  ![Naves Docker](Imagenes/Imagen_de_docker_corriendo_nave.png)

- **Contenedor Tanques**  
  ![Tanques Docker](Imagenes/Imagen_de_docker_corriendo_Tanques.png)

- **Contenedor Tetris**  
  ![Tetris Docker](Imagenes/Imagen_de_docker_corriendo_tetris.png)

---

## 🧠 Conclusiones

Esta tarea permitió consolidar:

- La organización modular de proyectos en Python.
- La creación manual de recursos gráficos y sonoros.
- El uso de `venv` para entornos aislados.
- La construcción de contenedores Docker con interfaz gráfica (`pygame`).
- La ejecución portátil y estandarizada de videojuegos.

