# 🎮 Tarea 9 – Juegos Clásicos en Python con Docker

Este proyecto corresponde a la Tarea 9 de la asignatura **Sistemas Digitales III**, en el cual se desarrollaron tres juegos clásicos (Naves, Tanques y Tetris) utilizando **Python con Pygame** y se empaquetaron usando **Docker**.

---

## 📁 Estructura del Proyecto

```plaintext
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

## ✅ 1. Activación del entorno virtual

Se crearon entornos virtuales independientes por juego usando `python3 -m venv`.

![Activación Venv](./Imagenes/Activación_instalación_Venv.png)

---

## 🧩 2. Clonación de los juegos desde GitHub

Se utilizó **sparse-checkout** para clonar solo las carpetas requeridas desde GitHub.

### Naves
![Clonación Naves](./Imagenes/Clonación_main.py_Naves.png)

### Tanques
![Clonación Tanques](./Imagenes/Clonación_main.py_tanques.png)

### Tetris
![Clonación Tetris](./Imagenes/Clonación_main.py_tetris.png)

---

## 🖼️ 3. Creación de imágenes y sonidos

Se empleó **ImageMagick** para generar imágenes y **sox** para crear sonidos de efectos.

### Instalación de paquetes:
![Instalación ImageMagick y sox](./Imagenes/Instalación para las imagenes.png)
![Instalación formatos de audio](./Imagenes/Instalación para los audios .png)

### Imágenes del juego Naves:
![Imágenes Naves](./Imagenes/Creación de las imagenes naves.png)

### Sonidos del juego Naves:
![Sonidos Naves](./Imagenes/Creación de los audio naves.png)

### Imágenes del juego Tanques:
![Imágenes Tanques](./Imagenes/Creacion de imagenes Tanques.png)

### Sonido del juego Tanques:
![Sonidos Tanques](./Imagenes/Creacion de audio Tanques.png)

### Imagen Tetris:
![Imagen Tetris](./Imagenes/Creación de la imagen Tetris.png)

---

## 📦 4. Organización de carpetas

Se reubicaron correctamente los archivos fuente a sus carpetas correspondientes.

![Creación Carpetas](./Imagenes/Creación_Carpetas.png)
![Entorno Virtual](./Imagenes/Creación_Entorno_Virtual.png)

---

## 🧪 5. Verificación del código

Los tres juegos fueron verificados y corren correctamente desde su entorno.

### Nave:
![Juego Naves](./Imagenes/Codigo del juego corriendo naves.png)

### Tanques:
![Juego Tanques](./Imagenes/Codigo del juego corriendo tanques.png)

### Tetris:
![Juego Tetris](./Imagenes/Codigo del juego corriendo tetris.png)

---

## 🐳 6. Dockerfile por juego

Cada juego cuenta con su `Dockerfile` propio para crear imágenes portables.

### Naves:
![Dockerfile Naves](./Imagenes/Creación de Dockerfile_nave.png)

### Tanques:
![Dockerfile Tanques](./Imagenes/Creación de Dockerfile _ tanques.png)

### Tetris:
![Dockerfile Tetris](./Imagenes/Creación de Dockerfile_tetris.png)

---

## 🛠️ 7. Creación de imágenes Docker

Se construyeron las imágenes Docker para cada juego:

### Imagen de Naves:
![Imagen Docker Naves](./Imagenes/Creación de imagen docker naves.png)

### Imagen de Tanques:
![Imagen Docker Tanques](./Imagenes/Creación de imagen docker tanques.png)

### Imagen de Tetris:
![Imagen Docker Tetris](./Imagenes/Creación de la imagen Tetris.png)

---

## ▶️ 8. Ejecución desde contenedores

Cada juego fue ejecutado desde Docker. Se solucionaron errores comunes como:

- Variables de entorno `XDG_RUNTIME_DIR`
- Error con `mixer not initialized`
- Permisos de acceso al entorno gráfico

### Juego Naves
![Juego corriendo Naves](./Imagenes/Juego corriendo naves.png)
![Finalizando Naves](./Imagenes/Juego finalizado.png)

### Juego Tanques
![Juego corriendo Tanques](./Imagenes/Juego corriendo.png)

### Juego Tetris
![Juego corriendo Tetris](./Imagenes/Juego corriendo Tetris.png)

---

## 🧠 9. Código fuente y lógica

Incluye estructura, imágenes y sonidos cargados correctamente.

### Naves:
![main.py Naves](./Imagenes/nano_main.py_naves.png)

### Tanques:
![main.py Tanques](./Imagenes/nano_main.py_tanques.png)

### Tetris:
![main.py Tetris](./Imagenes/nano_main.py_tetris.png)

---

## 📌 Conclusiones

- Se consolidó el uso de entornos virtuales y su aislamiento.
- Se manejaron herramientas como `git sparse-checkout`, `ImageMagick` y `sox`.
- Se empaquetaron tres juegos completos usando Docker, solucionando problemas reales de dependencias y sonido.
- Se logró ejecutar gráficamente Pygame dentro de contenedores con recursos de sistema compartidos.

---