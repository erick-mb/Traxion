# Predicción de Renuncia de Empleados

Este proyecto es una aplicación web construida con Flask para predecir si un empleado tiene alta probabilidad de renunciar. Utiliza un modelo de Machine Learning entrenado con XGBoost y se ejecuta en un contenedor Docker.

---

## 🛠️ **Requisitos Previos**

- Tener **Docker Desktop** instalado. (Nota: la computadora deberá de tener habilitado la opción de Virtualización en la BIOS)
- Conexión a Internet para descargar las dependencias necesarias.
- Una vez armado el contenedor, la imagaen se puede ejecutar offline.

## 📁 **Estructura del Proyecto**
```
📂 Docker/
│── app.py                    # Archivo principal de la aplicación Flask
│── mejor_modelo_xgb.pkl       # Modelo entrenado con XGBoost para la predicción de renuncias
│── scaler.pkl                # Scaler utilizado para normalizar los datos antes de la predicción
│── requirements.txt          # Lista de dependencias necesarias
│── Dockerfile                # Archivo para construir la imagen Docker
└── templates/
    └── index.html            # Plantilla HTML principal para la aplicación

```

---

## 🔧 **Instrucciones de Ejecución**

### **1. Descargar y Descomprimir el Proyecto**
Descargar el archivo Docker.zip (incluido en el repositorio) y descomprimirlo en una carpeta de tu preferencia.

### **2. Obtener la ruta de la carpeta descargada y construir la Imagen Docker**

Abrir Docker Desktop y acceder a la terminal. Luego, navegar al directorio donde se descomprimió el proyecto.

Construir la imagen de Docker usando el siguiente comando:
```
cd 'Insertar la ruta del directorio donde se descomprimió la carpeta'
docker build -t prediccion-renuncia-app .
```

### **3. Armar el contenedor**
```
docker build -t prediccion-renuncia-app .
```

### **4. Ejecutar el contenedor**
```
docker run -p 5000:5000 --name prediccion_app prediccion-renuncia-app
```

## 🚀 **Acceder a la aplicación**

Abrir el navegador y acceder:
```
http://localhost:5000
```

Si estás usando **Docker Desktop**, también puedes gestionar el contenedor desde la interfaz gráfica.


## 🛑 **Detener el contenedor**
```bash
docker stop prediccion_app
```


## 🔄 **Reiniciar el contenedor**
```bash
docker start prediccion_app
```

## 📦 **Dependencias y Librerías**
Las versiones de las principales librerías usadas son:

- XGBoost: 2.1.4
- Pandas: 2.2.2
- Flask: 3.1.0

Están especificadas en el archivo `requirements.txt`.
